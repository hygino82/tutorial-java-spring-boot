**Maven**

- **Baixe o binário**

- Acesse o site oficial [https://maven.apache.org/download.cgi](https://l.meta.ai/?u=https%3A%2F%2Fmaven.apache.org%2Fdownload.cgi&h=AT1uH6XeAiuOR_GFb7V4ZfAgQF8m_nrf30Oiq4XYQt3OV87sIL9NBl5-fa0wLpUkw1l6ysS9M4e2x9eioEIaVmrlgrQS3KWqA27P-HwWkKBYYshwjRCaHceNAOAcMfm_52s9Hq5ZPIRe0A) e escolha o arquivo `apache-maven-*.bin.tar.gz` (Linux/macOS) ou `apache-maven-*.bin.zip` (Windows).

- **Descompacte**

- Linux/macOS: `tar xzvf apache-maven-*.bin.tar.gz -C /opt` (ou outro diretório).

- Windows: extraia o zip em `C:\apache-maven`.

- **Configure as variáveis de ambiente**

- Linux/macOS: adicione `export PATH=/opt/apache-maven/bin:$PATH` ao seu `~/.bashrc` ou `~/.zshrc`.

- Windows: em _Variáveis de Ambiente_ → _Path_ adicione `C:\apache-maven\bin`.

- **Verifique**

- Abra um terminal e digite `mvn -v`. Você deverá ver a versão do Maven e do Java .

**Gradle**

- **Baixe a distribuição**

- Vá para [https://gradle.org/releases/](https://l.meta.ai/?u=https%3A%2F%2Fgradle.org%2Freleases%2F&h=AT1uH6XeAiuOR_GFb7V4ZfAgQF8m_nrf30Oiq4XYQt3OV87sIL9NBl5-fa0wLpUkw1l6ysS9M4e2x9eioEIaVmrlgrQS3KWqA27P-HwWkKBYYshwjRCaHceNAOAcMfm_52s9Hq5ZPIRe0A) e baixe o `gradle-*.bin.zip` (binário) ou o `gradle-*.all.zip` se quiser docs e fontes.

- **Descompacte**

- Linux/macOS: `unzip gradle-*.bin.zip -d /opt/gradle`.

- Windows: extraia para `C:\Gradle`.

- **Adicione ao PATH**

- Linux/macOS: `export PATH=/opt/gradle/gradle-*/bin:$PATH`.

- Windows: adicione `C:\Gradle\gradle-*\bin` ao _Path_ nas variáveis de sistema.

- **Teste a instalação**

- No terminal, execute `gradle -v` para confirmar a versão
Ambas podem ser instaladas via [[SDKMAN ]]