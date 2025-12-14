**Instalação do JDK – opções e verificação**

Fontes de download

|Distribuição|Link de download|
|---|---|
|**Amazon Corretto**|[https://aws.amazon.com/pt/corretto/](https://l.meta.ai/?u=https%3A%2F%2Faws.amazon.com%2Fpt%2Fcorretto%2F&h=AT1uH6XeAiuOR_GFb7V4ZfAgQF8m_nrf30Oiq4XYQt3OV87sIL9NBl5-fa0wLpUkw1l6ysS9M4e2x9eioEIaVmrlgrQS3KWqA27P-HwWkKBYYshwjRCaHceNAOAcMfm_52s9Hq5ZPIRe0A)|
|**Zulu JDK** (Azul)|[https://www.azul.com/downloads/?package=jdk#zulu](https://l.meta.ai/?u=https%3A%2F%2Fwww.azul.com%2Fdownloads%2F%3Fpackage%3Djdk%23zulu&h=AT1uH6XeAiuOR_GFb7V4ZfAgQF8m_nrf30Oiq4XYQt3OV87sIL9NBl5-fa0wLpUkw1l6ysS9M4e2x9eioEIaVmrlgrQS3KWqA27P-HwWkKBYYshwjRCaHceNAOAcMfm_52s9Hq5ZPIRe0A)|
|**Oracle JDK**|[https://www.oracle.com/br/java/technologies/downloads/](https://l.meta.ai/?u=https%3A%2F%2Fwww.oracle.com%2Fbr%2Fjava%2Ftechnologies%2Fdownloads%2F&h=AT1uH6XeAiuOR_GFb7V4ZfAgQF8m_nrf30Oiq4XYQt3OV87sIL9NBl5-fa0wLpUkw1l6ysS9M4e2x9eioEIaVmrlgrQS3KWqA27P-HwWkKBYYshwjRCaHceNAOAcMfm_52s9Hq5ZPIRe0A)|
|**Temurin** (Adoptium)|[https://adoptium.net/pt-BR/temurin](https://l.meta.ai/?u=https%3A%2F%2Fadoptium.net%2Fpt-BR%2Ftemurin&h=AT1uH6XeAiuOR_GFb7V4ZfAgQF8m_nrf30Oiq4XYQt3OV87sIL9NBl5-fa0wLpUkw1l6ysS9M4e2x9eioEIaVmrlgrQS3KWqA27P-HwWkKBYYshwjRCaHceNAOAcMfm_52s9Hq5ZPIRe0A)|
|**OpenJDK**|[https://openjdk.org/](https://l.meta.ai/?u=https%3A%2F%2Fopenjdk.org%2F&h=AT1uH6XeAiuOR_GFb7V4ZfAgQF8m_nrf30Oiq4XYQt3OV87sIL9NBl5-fa0wLpUkw1l6ysS9M4e2x9eioEIaVmrlgrQS3KWqA27P-HwWkKBYYshwjRCaHceNAOAcMfm_52s9Hq5ZPIRe0A)|
|**Microsoft JDK**|[https://www.microsoft.com/openjdk](https://l.meta.ai/?u=https%3A%2F%2Fwww.microsoft.com%2Fopenjdk&h=AT1uH6XeAiuOR_GFb7V4ZfAgQF8m_nrf30Oiq4XYQt3OV87sIL9NBl5-fa0wLpUkw1l6ysS9M4e2x9eioEIaVmrlgrQS3KWqA27P-HwWkKBYYshwjRCaHceNAOAcMfm_52s9Hq5ZPIRe0A)|

Como instalar

- **Escolha a versão** que melhor atende ao seu projeto (LTS ou não‑LTS).

- **Baixe o pacote** para o seu sistema operacional (Linux, Windows ou macOS).

- **Execute o instalador** ou descompacte o arquivo em um diretório de sua preferência.

- **Configure o PATH** (se necessário) para que o `java` e o `javac` sejam encontrados no terminal.

> _Dica:_ você também pode gerenciar múltiplas versões com o [[SDKMAN]].

Bash

```
java -version
```

O comando deve exibir a versão do Java que acabou de ser instalada.