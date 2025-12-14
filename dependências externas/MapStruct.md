## Configuração do MapStruct (Maven)

```xml
<properties>
    <org.mapstruct.version>1.6.3</org.mapstruct.version>
</properties>

<dependencies>
    <dependency>
        <groupId>org.mapstruct</groupId>
        <artifactId>mapstruct</artifactId>
        <version>${org.mapstruct.version}</version>
    </dependency>
</dependencies>

<build>
    <plugins>
        <plugin>
            <groupId>org.apache.maven.plugins</groupId>
            <artifactId>maven-compiler-plugin</artifactId>
            <version>3.8.1</version>
            <configuration>
                <source>1.8</source>
                <target>1.8</target>
                <annotationProcessorPaths>
                    <path>
                        <groupId>org.mapstruct</groupId>
                        <artifactId>mapstruct-processor</artifactId>
                        <version>${org.mapstruct.version}</version>
                    </path>
                    <!-- outros processors, se houver -->
                </annotationProcessorPaths>
            </configuration>
        </plugin>
    </plugins>
</build>```
Para utilizar o MapStruct devemos criar uma interface contendo as assinaturas dos métodos a serem mapeados, as implementações serão criadas automática durante a fase de compilação.
```java
@Mapper
public interface ConsoleMapper {

ConsoleMapper INSTANCE = Mappers.getMapper(ConsoleMapper.class);
  
ConsoleMinDto convertoToConsoleMinDto(Console console);

ConsoleDto convertoToConsoleDto(Console console);

}```

Caso seja utilizada em um projeto Java sem Spring Boot chamamos o mapper com. o uso de 
``` java 
ConsoleMapper.INSTANCE.convertoToConsoleDto(result);
```

Em um projeto Java com Spring Boot
```java 
@Mapper(componentModel = "spring")
public interface BookMapper {
    ResponseBookDetailsDto toBookResponse(Book book);

    Book toBookEntity(RequestBookDto dto);

    ResponseBookDto toBookMinResponse(Book entity);
}```
Para utilizar usamos injeção de dependência cia construtor.
```java
@Service
public class BookService {

    private final BookRepository bookRepository;
    private final BookMapper bookMapper;

    public BookService( BookRepository bookRepository, 
					    BookMapper bookMapper) {
        this.bookRepository = bookRepository;
        this.bookMapper = bookMapper;
    }
}```
