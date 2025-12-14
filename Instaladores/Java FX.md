A partir do JDK 9 o JavaFX deixou de vir embutido. O SDKMAN não oferece um pacote “javafx”; ele só gerencia distribuições do JDK. Para colocar o JavaFX no seu projeto, use uma dessas opções:

- **Maven** – adicione o artefato OpenJFX ao `pom.xml`

XML

```
<dependency>
    <groupId>org.openjfx</groupId>
    <artifactId>javafx-controls</artifactId>
    <version>22</version>
</dependency>
<dependency>
    <groupId>org.openjfx</groupId>
    <artifactId>javafx-fxml</artifactId>
    <version>22</version>
</dependency>

<build>
    <plugins>
        <plugin>
            <groupId>org.openjfx</groupId>
            <artifactId>javafx-maven-plugin</artifactId>
            <version>0.0.8</version>
            <configuration>
                <mainClass>seu.pacote.Main</mainClass>
            </configuration>
        </plugin>
    </plugins>
</build>
```

- **Gradle** – inclua a dependência no `build.gradle`

Groovy

```
implementation 'org.openjfx:javafx-controls:22'
```

- **Download direto** – baixe o SDK no site da Gluon  
    [https://gluonhq.com/products/javafx/](https://gluonhq.com/products/javafx/)  
    Descompacte e aponte a variável de ambiente `PATH_TO_FX` para a pasta `lib` do SDK.

- **Scene Builder** – ferramenta visual para editar arquivos FXML  
    [https://gluonhq.com/products/scene-builder/](https://gluonhq.com/products/scene-builder/)  
    Instale o aplicativo (Windows / macOS / Linux) e abra seus arquivos `.fxml` diretamente nele ou no IDE.