```xml
<dependency> <groupId>org.modelmapper</groupId> <artifactId>modelmapper</artifactId> <version>3.2.4</version> </dependency>
```
Para utilizar em um projeto Spring Boot o ModelMapper devemos criar uma classe de configuração.
```java
@Configuration
public ModelMapperConfig{
	@Bean
	public ModelMapper getMapper(){
	return new ModelMapper();
	}
}
```
Para utilizar utilizamos a injeção de dependência via construtor e chamamos o método map(entrada, classe de destino).

```java
@Service
public final class GameService{
private final GameRepository gameRepository;
private final ModelMapper mapper;

	public GameService(
		ModelMapper mapper, 
		GameRepository gameRepository){
			this.mapper = mapper;
			this.gameRepository = gameRepository;
	}
	
	@Transactional(readonly = true)
	public List<GameDTO> findAll(){
		final var result = gameRepository.findAll();
		
		return restul.stream()
			.map(g -> mapper.map(g, GameDTO.class))
			.toList();
	}
}```


Atualmente o ModelMapper não suporta record se precisar utilizar record use [[MapStruct]] ao invés do ModelMapper. 