# HTML5 (Básico) :book:

É uma linguagem de **marcação**.

Tim Berners-Lee e Roberto Cailliau foram os criadores do HTML.

W3C surgiu para padronizar o HTML.

Ao entrar em um site e usar o comando "**CTRL + U**" você terá acesso ao código fonte (html) da página

Link do W3S com todas as tags: https://www.w3schools.com/tags/default.asp

Sempre criar um arquivo "**index**" quando iniciar um projeto, pois normalmente esse nome é utilizado para indicar a raiz do projeto. É um padrão para todos os servidores.

O atalho utilizado para abrir o **Go Live** é **ALT + O** *(ou alt + L)*

Todo arquivo HTML tem:

1. !doctype
2. html
3. head
4. body

Sempre seguindo a hierarquia, como na imagem a seguir.

![image-20241017120808688](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241017120808688.png)

"**Meta tag**" são tags utilizadas para descrever o conteúdo de uma página da web. Elas não necessitam que haja uma tag de fechamento. *(Quando um site aparece na pesquisa do google, a meta tag é como se fosse aquela descrição da página que fica logo abaixo do título, como na imagem abaixo)* 

![image-20241017121659060](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241017121659060.png)

A tag "**H**" significa HEAD, ou seja, é um título do texto. Ela pode ser seguida pelos números 1, 2, 3, 4, 5 ou 6, sendo 1 o título de **MAIOR** importância (e tamanho) e 6 o de **MENOR** importância (e tamanho). **Não é indicado que utilize mais de um título H1 por página.** Exemplo:

![image-20241017124451739](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241017124451739.png)

A tag "P" cria um **PARÁGRAFO**

*A tag "B" deixa a palavra em **negrito** (mas em questão de semântica, ele não é tão utilizado)*

A tag "STRONG" deixa a palavra em **NEGRITO** é mais semântico, de maior relevância, sendo melhor e mais utilizado do que a tag B

A tag "I" deixa a palavra em ***ITÁLICO***

A tag "U" deixa a palavra **SUBLINHADA**

A tag "S" deixa a palavra com um **RISCADA** no meio

Levando em conta que o HTML é uma linguagem de MARCAÇÃO, essas tags não são comumente usadas para deixar a estética da página bonita, para isso é utilizado o **CSS**. No caso do HTML é para demonstrar importância semântica.

Link para formatação de textos HTML: https://developer.mozilla.org/pt-BR/docs/Learn/HTML/Introduction_to_HTML/Advanced_text_formatting?_gl=1*1qd8d3q*_ga*MTEwMjE3ODAuMTcyODM5NjEwNA..*_ga_37GXT4VGQK*MTcyOTE3NTM5NS4zLjEuMTcyOTE3OTY5OC4wLjAuMA..



Para fazer um **comentário** no HTML basta escreve no VS Code \<!-- e ele irá autocompletar, devendo ficar <!-- -->, também é possível fazer um comentário com um atalho no teclado, deve-se selecionar todo o texto que é para comentar e clicar no atalho CTRL + ; (para desfazer o comentário pode selecionar todo texto novamente e clicar o atalho novamente)

Podemos usar o comentário para fazer anotações no código, para que outras pessoas não vejam, mas que vc precise lembrar, por exemplo "TODO: fazer a animação do h1".

![image-20241018134248541](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241018134248541.png)

Quando **NÃO** usar comentários: se você não estiver mais utilizando um código, não deixa ele comentado. Também é bom utilizar códigos de qualidade e fáceis para outras pessoas verem e conseguirem mexer, sem a necessidade de ter um comentário para explicar tudo. 



**Para criar um link EXTERNO dentro do HTML:**

Use a tag "A" (âncora) *(que automaticamente é completada com **href="")*** e dentro do atributo href você insere o link/url, por exemplo: <a href="https://linkedin.com/in/leticia-avelar95">

Para que o link aberto **não sobreponha a sua página**, é necessário acrescentar mais um atributo que faz com que ela abra em uma nova aba. Basta acrescentar **target="_blank"** logo depois do link *href*.

![image-20241018133858396](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241018133858396.png)

É importante lembrar que o uso desse atributo *target* é indicado para quando vai direcionar para links **externos**. Quando é um link para continuar navegando no seu próprio site, não faça o uso dele.



**Para criar um link INTERNO dentro do HTML:**

Quando a navegação entre links será feita dentro do mesmo site, após o atributo de *href*, coloca-se o nome do arquivo que o link será redirecionado. Exemplo: você está criando um portfólio e quer um link que vá para o seu contato, então **PRIMEIRO** vc precisa ter um arquivo com essa página de contato em questão *(exemplo "contato.html")* e depois vc vai criar uma linha com <a href="contato.html">

![image-20241018133753330](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241018133753330.png)

**Dica**: vc pode entrar nas aspas "" do *href* e dar um CTRL + barra de espaço que o vs code vai listar todos os arquivos que tem dentro daquela pasta, não sendo necessário decorar o nome de todos os arquivos.

![image-20241018133821058](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241018133821058.png)

Para fazer com que um link retroceda à **página anterior**, vc seguirá o mesmo protocolo de âncora, mas no *href* colocará "../" para que ele reconheça os arquivos anteriores

![image-20241018133514420](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241018133514420.png)



**Para criar/adicionar IMAGENS no HTML:**

Utilizando a tag "IMG" (que será auto completada por src="" alt="", sendo que SRC significa source, que é onde a imagem se encontra e ALT é de alternativa, que é o que aparece quando a imagem não carrega/está quebrada, também é útil para leitores de tela e acessibilidade).

![image-20241018165025950](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241018165025950.png)

Também é importante lembrar de colocar o atributo "title" que é aquela legenda que aparece quando o mouse fica parado em cima de uma imagem.

![image-20241018165054664](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241018165054664.png)

Dica: utilizando o **INSPECIONAR** na página da web, é possível conferir qual o tamanho da imagem e se está igual ao tamanho real dela no seu desktop.

É possível carregar imagens **EXTERNAS** para dentro do site também, utilizando o site [PLACEHOUDER](https://placehold.co/?_gl=1*1g7bfdg*_ga*MTEwMjE3ODAuMTcyODM5NjEwNA..*_ga_37GXT4VGQK*MTcyOTI4MDM0Ni40LjEuMTcyOTI4MDM5OC4wLjAuMA..) e copiando o link/url e colocando no html

![image-20241018165924569](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241018165924569.png)

![image-20241018165908432](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241018165908432.png)



**Para criar lista NÃO ORDENADAS:**

Utilizando a tag "UL" vc dá início a uma lista, dentro dela deve haver o atributo "LI" que são os itens da lista

![image-20241018171820078](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241018171820078.png)

Para facilitar a criação da lista já com os itens, pode-se usar o atributo ul>li*número de itens da lista. Exemplo: uma lista que terá 5 itens ficaria ul>li\*5

![image-20241018170928378](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241018170928378.png)



**Para criar lista ORDENADA:**

Utilizando a tag "OL" vc dá início a uma lista, dentro dela deve haver o atributo "LI" que são os itens da lista.

![image-20241018171837647](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241018171837647.png)

Também é possível facilitar a criação da lista já com os itens utilizando o atributo ol>li*número de itens da lista. Exemplo uma lista que terá 5 itens ficaria ol>li\*5

![image-20241018171708379](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241018171708379.png)



**Para criar uma tabela:**

Utilizando a tag "TABLE" vc inicia a criação de uma tabela e serve para englobar toda a estrutura dela. É uma palavra reservada.

Seguido da tag "THEAD" serve para criar um cabeçalho, ou seja, serve para organizar quais serão as representações da coluna dessa tabela. Engloba toda a estrutura do cabeçalho.

A tag "TR", que significa table row, ela representa uma **LINHA** na tabela. Dentro da tag tr, cria-se uma tag "TH" que é responsável por cada **COLUNA** do cabeçalho.

![image-20241022165258757](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241022165258757.png)

A tag "TBODY" refere-se ao corpo legítimo dos dados. Dentro dela é possível utilizar também a tag "TR" e também "TD", que significa table data, que diz respeito aos dados de cada coluna da tabela.

Existem atributos que podem ser utilizados nas tags. Os dois principais são o "colspan" e o "rowspan".

O "colspan" tem a capacidade de esticar/expandir uma determinada coluna para que ela ocupe outras colunas (horizontalmente).

O "rowspan" tem a capacidade de expandir as linhas, fazendo com que ela ocupe mais linhas (verticalmente).

![image-20241022165331031](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241022165331031.png)

Com a tag "TFOOT" é possível representar a parte do rodapé da tabela, serve para agrupar um conteúdo ali, além de ser utilizado para representar informações importantes, como por exemplo valores totais, resumo etc.

O tfoot também terá um tr e um td dentro.

![image-20241022165345704](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241022165345704.png)

![image-20241022165412239](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241022165412239.png)

Nesse caso, para que a tabela ficasse estilizada com as bordas, dentro da tag head foi criada uma tag "STYLE" com alguns atributos.

![image-20241022170519752](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241022170519752.png)