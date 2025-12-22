Extensible Markup Language é uma linguagem de marcação de documentos.
Arquivos textuais -> documentos XML.
- Descrição bem precisa;
- Marcar documentos (Markup);
- definir e criar os seus próprios documentos (Extensible);
Dados portáteis
- Para humanos ou não;
- Simplicidade na leitura, gravação e compreensão;
- Projetado para armazenar e transportar dados;
- Aceito em qualquer plataforma de desenvolvimento atualmente;
- É um padrão da W3C;
Todo tag XML seque a estrutura de sintaxe geral.
```xml
<tag-atributos>Conteúdo</tag-atributos>
ou
<tag-atributos/> quando não tem conteúdo (self close tag)
```  
Onde:
```xml
<tag> início de um rótulo XML
</tag> encerramento de um rótulo XML
```
Atributos: Lista de atributos (0 a N).
Conteúdo: Dados, inclusive outras tags.

Exemplo de XML - visualização
```xml
<?xml version="1.0" encoding="UTF-8"?>
<!--email-->
<mail>
	<to>destinatario@email.com</to>
	<from>remetente@email.com</from>
	<subject>Início das aulas</subject>
	<body>Aulas 2025</body>
	<attach content="false"/>
</mail>
```
Os comentários são feitos entre <!-- e -->
``` xml
<!--exemplo de comentário-->
```
No início temos a definição da versão e encoding. ``<?xml version="1.0" encoding="UTF-8"?>``

# Regras para nomear as tags
	O primeiro caractere deve ser uma letra, undescore  ou dois pontos;
	Os demais caracteres podem ser letras, números, ponto, underscore ou dois pontos;
	É case sensitive (diferencia maiúsculas e minúsculas);
	Dois pontos são associados a namespaces.

# Namespaces
- Criar um  "espaço de nomes" únicos;
- Adicionar um prefixo ao nome do elemento;
- seguido do nome único destro do espaço;
```xml 
<Prefixo:Elemento> </Prefixo:Elemento>
```
- Namespaces precisam ser declarados e associados a um prefixo;
- Em documentos XML, o namespace é associado a um URI (semelhante a um endereço de internet).

HTML possui baixo nível de formalismo quando comparado ao XML.

Caso o XML não siga essa notação, o chamamos de XML mal formatado. Isso pode ser um problema do ponto de vista computacional.
Todo o XML tem um nó raiz com atributo id.
Em um ==XML bem formatado== temos um nó raiz, todos os atributos foram delineados, os conteúdos foram marcados, além de ter um cabeçalho indicando qual é a versão e o encoding do XML.
O documento XML segue uma estrutura em árvore.
Arquivos #XHTML nada mais são do que uma página estilo HTML que utilizam namespaces do JSF (Java Server Faces).

