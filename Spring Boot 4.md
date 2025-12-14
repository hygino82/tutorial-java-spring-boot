# Ecossistema Spring Framework

O **Spring Framework** constitui um amplo ecossistema de ferramentas voltadas ao desenvolvimento de aplicações Java modernas, com foco em produtividade, modularidade e boas práticas de engenharia de software.

## Criação de Projetos

A forma mais comum de iniciar um projeto Spring é por meio do **Spring Initializr**, disponível em:

- [https://start.spring.io/](https://start.spring.io/)
    

Atualmente:

- **Spring Framework** encontra-se na versão **7**
    
- **Spring Boot** encontra-se na versão **4**
    

Essas versões refletem a evolução da plataforma, com forte alinhamento às versões mais recentes do Java.

## Linguagens Suportadas

Ao criar um projeto Spring Boot, é possível escolher entre as seguintes linguagens:

- **Java**
    
- **Kotlin**
    
- **Groovy**
    

Todas essas linguagens são executadas sobre a **Java Virtual Machine (JVM)**, o que garante interoperabilidade, portabilidade e acesso ao ecossistema Java.

## Versões do JDK

O Spring Boot permite selecionar a versão do **JDK** a ser utilizada no projeto.

- Versão mínima suportada: **Java 17**
    
- Versão mais recente disponível: **Java 25**
    

As versões **17**, **21** e **25** são classificadas como **LTS (Long-Term Support)**, ou seja, recebem suporte estendido e são recomendadas para ambientes produtivos.

## Ferramentas de Build

Para gerenciamento de dependências e automação do build, o Spring Boot oferece suporte nativo às seguintes ferramentas:

- **Maven**
    
- **Gradle**
    

Ao gerar o projeto pelo Spring Initializr, já é incluída uma versão embarcada (wrapper) da ferramenta escolhida, não sendo obrigatória a instalação global no sistema.

Entretanto, caso deseje instalar manualmente, os downloads oficiais estão disponíveis em:

- Maven: [https://maven.apache.org/download.cgi](https://maven.apache.org/download.cgi)
    
- Gradle: [https://gradle.org/install/](https://gradle.org/install/)
    

## Instalação via SDKMAN

Uma alternativa prática para instalar e gerenciar múltiplas versões do **JDK**, **Maven** e **Gradle** é o **SDKMAN**, especialmente em sistemas Linux e macOS.

Instalação do SDKMAN:

```bash
curl -s "https://get.sdkman.io" | bash
```

Após a instalação, é possível instalar as ferramentas desejadas com comandos simples, como:

```bash
sdk install java 21.0.9-amzn
sdk install maven 3.9.11
sdk install gradle 9.2.1
```

O uso do SDKMAN facilita a alternância entre versões e contribui para um ambiente de desenvolvimento mais organizado e produtivo.

## Dependências Comuns do Spring Boot

Ao criar um projeto **Spring Boot**, é possível adicionar dependências que estendem as funcionalidades da aplicação conforme o tipo de sistema a ser desenvolvido. A seguir estão algumas das dependências mais comumente utilizadas:

### Spring Web

A dependência **Spring Web** é utilizada para a criação de aplicações web e serviços **RESTful**. Ela fornece suporte a:

- Criação de APIs REST
    
- Uso de controladores com `@RestController`
    
- Mapeamento de requisições HTTP (`GET`, `POST`, `PUT`, `DELETE`, etc.)
    

### Spring Data JPA

O **Spring Data JPA** é utilizado para realizar a persistência de dados em **bancos de dados relacionais** de forma simplificada.

Normalmente, essa dependência é utilizada em conjunto com:

- Um banco de dados relacional, como:
    
    - MySQL
        
    - H2
        
    - PostgreSQL
        
- O respectivo **driver JDBC** do banco escolhido
    

O Spring Data JPA reduz significativamente a quantidade de código necessária para acesso a dados, abstraindo a implementação de repositórios.

### Lombok

O **Lombok** é uma biblioteca que tem como objetivo reduzir o chamado _boilerplate code_.

Com ele, é possível gerar automaticamente:

- Getters e setters
    
- Construtores
    
- Métodos `equals`, `hashCode` e `toString`
    

Tudo isso por meio de anotações, como `@Getter`, `@Setter`, `@Data`, entre outras.

### Spring Boot DevTools

O **Spring Boot DevTools** é uma dependência voltada exclusivamente para o ambiente de desenvolvimento.

Ela permite, entre outras funcionalidades:

- **Auto reload** da aplicação sempre que alterações no código são detectadas
    
- Melhoria na produtividade durante o desenvolvimento
    

Essa dependência não deve ser utilizada em ambientes de produção.

### Validation

A dependência **Validation** é utilizada para validar dados de entrada da aplicação.

Ela permite definir regras de validação por meio de anotações, como:

- `@NotNull`
    
- `@NotBlank`
    
- `@Size`
    
- `@Email`
    

Essas validações são amplamente utilizadas em objetos de transferência de dados (DataTransferObjects) e entidades para garantir a integridade dos dados.
