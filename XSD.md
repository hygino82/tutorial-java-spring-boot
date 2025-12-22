# XML Schema
XML pode sofrer atualizações e modificações que podem ocasionar erro de interpretação.

# Tipos de elementos no schema

Os elementos podem ser de tipo simples ou complexo.

## Tipos Simples
- Podem conter apenas texto. Eles não podem ter elementos filhos ou atributos;
- Todos os tipos integrados são do tipo simples;
- Pode adotar um padrão específico;
- Os tipos simples podem ser atômicos ou não.

## Tipos complexos
- Podem conter elementos e atributos filhos, bem como texto;
- Por padrão elementos de tipo complexo contém elementos filhos;
- Podem ser limitados a ter conteúdo simples;
- Podem ter atributos;
- Podem ser limitados a não ter conteúdo;
- Podem ter conteúdo misto.

As atributos de um objeto se tornam uma sequencia de elementos.
Participante
- id: int
- nome: String

Um software pode criar o XMl de uma maneira dinâmica para outro processar.
XML schema descreve a estrutura de um documento XML.
XSD ajuda a formalizar a maneira que devemos criar o XML.

O tipo abstrato de quemos é o element, que pode ser Simply ou Complex.
Temos tipos primitivos de dados e derivados.

 Podemos ter expressões regulares para validar o tipo de dado de entrada, como em um e-mail.

Os nós superiores só podem ser feitos após serem definidos os nós inferiores.
Para nos referirmos aos nós inferiores usamos ```xml
<xs:element ref="referẽcia", niOccurs="1" maxOccurs="1">```nesse caso 
deverá aparecer uma única vez a referẽncia.

Para vincular um XML a um arquivo XSD a referẽncia da localização do Arquivo XSD.
Podemos vincular via namespace podendo ser um arquivo ou uma URL.

Em Java podemos vincular o XSD. Isso ajuda a reduzir o uso do XML  .
Existem modelos de XSD prontos para várias coisas, como emissão de nota fiscal.

XSD sustiuiu o DTD (document type definition)