# CSS3 (Avançado) :book:

:link: Notion: https://glowing-scilla-18d.notion.site/CSS3-Avan-ado-157bf6c7b63d8067bf84eeebd75c23cb



### **PARTE 1**

**Pseudo Classes**

São palavras que colocamos depois de um seletor separadas por : (dois pontos). Elas servem para estilizar estados dos seletores, outros elementos da página ou também fatores externos, como, por exemplo, histórico de navegação (utilizando o visited, por exemplo, que serve para estilizar um link já foi visitado pelo usuário, como vimos anteriormente).

[Todas pseudo-classes | Developer Mozilla](https://developer.mozilla.org/pt-BR/docs/Web/CSS/Pseudo-classes?_gl=1*3sgzr2*_ga*MTEwMjE3ODAuMTcyODM5NjEwNA..*_ga_37GXT4VGQK*MTczNDAyMTc3My43OS4xLjE3MzQwMjE3ODkuMC4wLjA.)



A anatomia de uma pseudo classe é: o seletor:pseudo-classe { propriedade: valor; }

![image-20241213120123673](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241213120123673.png)

Elas são muito boas, pois permitem que escrevamos menos classes no nosso código html.



**First Child**

Com ela conseguimos estilizar o **primeiro** elemento **filho** de um elemento **pai**.

Por exemplo, temos uma div e dentro dessa div temos 2 parágrafos. Digamos que eu só queira estilizar o primeiro que está ali dentro. Para isso, podemos estilizar utilizando a pseudo classe first child.

<img src="C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241212183659760.png" alt="image-20241212183659760" style="zoom:80%;" />

No CSS vamos criar a nomenclatura de uma pseudo-classe + first child e atribuir as propriedades que desejar nela, nesse caso, uma cor. Dessa forma, podemos ver que foi estilizado apenas o primeiro parágrafo e o segundo continuo na cor preta.

​			![image-20241212184607456](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241212184607456.png)		![image-20241212184208991](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241212184208991.png)



**Last Child**

Funciona praticamente da mesma forma que a first child, porém agora vai estilizar o último elemento/filho.

​			![image-20241212184720427](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241212184720427.png)		![image-20241212184736827](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241212184736827.png)



**Not**

Ele é de negação, sua estrutura é um pouco diferente, ficando seletor:note() {	} e dentro do abre e fecha **parênteses** será dado algum parâmetro, que vai ser o valor que será negado, a classe que será negada.

Por exemplo, temos 3 parágrafos na página e queremos que todos os parágrafos que NÃO tenham a classe ".padrão", recebam a cor amarela, então esse seria o comportamento (todos os parágrafos sem padrão ficaram amarelos)

​			![image-20241212185546931](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241212185546931.png)				<img src="C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241212185609280.png" alt="image-20241212185609280" style="zoom:80%;" />

No exemplo anterior, nenhum dos parágrafos tinha a classe padrão, logo, todos os parágrafos ficaram amarelos, MAS se voltarmos ao html e atribuirmos essa classe a um dos parágrafos, poderemos ver o comportamento do not

​			![image-20241212185929494](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241212185929494.png)			![image-20241212185943919](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241212185943919.png)

O primeiro parágrafo voltou a ser aquamarine, como estava estilizado anteriormente.



**Nth Child**

A estrutura é parecida com o not, seletor:nth-child() {	} e dentro dos parênteses será passado algum argumento. Essa pseudo-classe vai selecionar elementos a partir da posição deles em um grupo de elementos irmãos. Dentro do parênteses da nth-child, podemos passar alguns argumentos que já são definidos.

![image-20241212192611932](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241212192611932.png)

Por exemplo, podemos aplicar o odd para que todos os itens **ímpares** fiquem vermelhos, então todos os ímpares (1, 3, 5, 7 e por assim em diante) ficarão vermelhos e os pares não serão afetados.

​			![image-20241212192223007](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241212192223007.png)			![image-20241212192238948](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241212192238948.png)

Para estilizar os **pares**, devemos dar o argumento even. Dessa forma os itens 2, 4 (e assim por diante) ficarão estilizados em vermelho.

​			![image-20241212192306957](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241212192306957.png)			![image-20241212192319229](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241212192319229.png)

Essa prática de utilizar pseudo-classes é muito boa, pois vai deixar o html menos verboso, já que não precisa colocar uma classe para cada elemento que deseja estilizar, sendo assim, mais fácil de dar manutenção.

Utilizando o 3n (ou 2n, 4n etc) podemos estilizar os itens com um salto de espaço entre eles, ou seja, 3n = vai estilizar os itens de 3 em 3, o 2n = vai estilizar os itens de 2 em 2.

​		![image-20241212193012197](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241212193012197.png)	![image-20241212192940292](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241212192940292.png)	<img src="C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241212192950828.png" alt="image-20241212192950828" style="zoom:80%;" />

Outra argumento que podemos dar é escrever apenas o número do item que deseja fazer a estilização. Por exemplo, se colocar apenas um (2), o segundo elemento será estilizado.

​				![image-20241213094617831](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241213094617831.png)			![image-20241213094628823](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241213094628823.png)

Também podemos dar o argumento de range, que fará com que, do elemento X ao elemento Y fique estilizado. A forma de escrita fica bem diferente, sendo necessário estabelecer um nth-child de início e outro nth-child com onde será o fim. Por exemplo, se queremos estilizar do item 2 ao item 5:

​		![image-20241213095753073](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241213095753073.png)		![image-20241213095809001](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241213095809001.png)

*Se fosse do 1° item ao 3°, então ficaria n+1 e -n+3, e assim por diante.*



No seletor nth-child(n+2):nth-child(-n+5), cada parte define um intervalo específico:

1. **nth-child(n+2)**:
   - Significa "a partir do 2º elemento".
   - O cálculo é baseado em n, que assume valores inteiros (0, 1, 2, ...).
   - Quando n = 0, começa no 2º (2 + 0).
2. **nth-child(-n+5)**:
   - Significa "até o 5º elemento".
   - O cálculo também usa n. Para limitar a seleção, -n+5 considera os valores que resultam em números ≤ 5.

**Combinados:**

- Apenas elementos que atendem **ambas as condições** serão estilizados, ou seja, os elementos **do 2º ao 5º**.

**Por que assim?**

- (n+2) fixa o ponto inicial (≥ 2).
- (-n+5) fixa o ponto final (≤ 5).
- A interseção desses critérios seleciona o intervalo desejado.



LEMBRANDO QUE, COMO É NTH **FIRST CHILD**, A ORDEM A SER SEGUIDA É DE CIMA (PRIMEIRO ELEMENTO) PRA BAIXO (ÚLTIMO ELEMENTO).



**Nth Last Child**

Também é muito parecido com o nth last child, porém a ordem seguida será do ultimo elemento até o primeiro. 

Por exemplo, colocando apenas o número do argumento, por exemplo (1), o elemento a ser estilizado será o último *(e não o primeiro)*.

![image-20241213103059638](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241213103059638.png)



**Only Child**

Essa pseudo-classe vai pegar o único elemento que NÃO TEM elementos irmãos. Por exemplo, se existem duas divs, mas uma tem um parágrafo e a outra tem dois parágrafos (dois irmãos), então o only child vai estilizar a div composta por um parágrafo.

![image-20241213103852796](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241213103852796.png)

​		![image-20241213104211487](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241213104211487.png)			![image-20241213104223856](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241213104223856.png)

O primeiro parágrafo foi estilizado, pois estava em uma div sem irmãos e os dois seguintes não foram, pois são irmãos.



**Pseudo Elementos**

Servem para estilizar partes especificas de um elemento, por exemplo, com eles podemos estilizar a primeira letra ou linha de um elemento html. Também podemos inserir conteúdo antes ou depois do conteúdo do elemento em si *(before e after)*.

Parecido com as pseudo-classes os pseudo-elemento também terão vários tipos de estilização.



A anatomia de um pseudo-elemento é um pouco diferente, vamos escrever o seletor::pseudo-elemento { propriedade: valor; }

![image-20241213120332218](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241213120332218.png)



**First Letter**

Com esse pseudo elemento, é possível estilizar a **primeira letra** do elemento.

Por exemplo, temos um parágrafo e queremos deixar apenas a primeira letra dele colorida.

![image-20241213121446184](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241213121446184.png)

Para utilizar o first letter é necessário que o elemento seja do tipo **BLOCK**, por exemplo, a tag span não pode ser estilizado com ele, pois é do tipo inline level.

Também é possível estilizar classes e ids.

​			![image-20241213121849129](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241213121849129.png)		![image-20241213121857349](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241213121857349.png)

​			![image-20241213121929590](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241213121929590.png)		![image-20241213121936479](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241213121936479.png)

Qualquer tipo de seletor vai funcionar.



**First Line**

Serve para estilizar a primeira linha de um elemento (lembrando que isso varia de acordo com o tamanho da tela, se não tiver uma dimensão fixa para o texto e a primeira linha for dinâmica, quanto mais tela, maior será o texto estilizado reconhecido como 'primeira linha').

Por exemplo, se estilizar a primeira linha desse parágrafo, enquanto estiver com a tela menor, fica menos texto colorido e quanto maior a tela, mais texto será considerado como first line.

![image-20241213122358741](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241213122358741.png)

![image-20241213122430698](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241213122430698.png)

É possível colocar os dois juntos, misturados (first letter + first line):

![image-20241213122945166](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241213122945166.png)



**Marker**

Serve para estilizar os marcadores de uma lista.

![image-20241213123405552](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241213123405552.png)



**Before**

Vai inserir um conteúdo ANTES do conteúdo do elemento que estamos estilizando, que basicamente vai ser o seletor antes dos :: (pode ser uma tag, uma classe, um id). Por exemplo, se eu quero inserir uma imagem antes de todos os títulos da página. O jeito mais "comum" seria criando o h2 e colocando uma tag de img no html para cada um deles.

![image-20241213132822345](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241213132822345.png)	![image-20241213132919215](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241213132919215.png)



Usando um pseudo elemento, não é necessário ficar repetindo o código e deixando verboso, basta apenas estilizar no CSS. 

Nesse caso, como queremos inserir uma imagem, a propriedade dentro do before será um content (que quer dizer conteúdo) seguida de uma url como valor (que nesse caso será o caminho até a imagem)

![image-20241213134114886](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241213134114886.png)

O content basicamente define o conteúdo que será inserido na página. No exemplo foi utilizado para inserir uma imagem, mas após o contest também podemos colocar um texto.

![image-20241213134420505](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241213134420505.png)

*Dessa forma, independente de quantos h2 tenham na página, todos estarão automaticamente estilizados para terem algo antes (seja imagem, texto).*



Também podemos usar o before com um background, nesse caso, a estrutura fica bem diferente e é necessário acrescentar mais propriedades.

![image-20241213135415548](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241213135415548.png)

*O content deve ficar em branco (só com aspas); um background com url da imagem; center center para que centralize a imagem horizontalmente e verticalmente; mudar o display para inline-block; e altura e largura iguais a da logo (no meu caso, 20x20).*



Podemos usar o **content = URL;** quando quiser inserir a imagem diretamente. E usar o **content = "";** quando quiser ter mais flexibilidade de estilização - redimensionamento ou posicionamento da imagem, por exemplo.



**After**

É bem parecido com o before, mas vai colocar o conteúdos DEPOIS do elemento do seletor que foi especificado.

![image-20241213140147042](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241213140147042.png)



Para ficar melhor exemplificado:

<img src="C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241213140544531.png" alt="image-20241213140544531"  />  <img src="C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241213140708366.png" alt="image-20241213140708366" style="zoom:80%;" />  ![image-20241213140729550](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241213140729550.png)



**Seletores**

São padrões de CSS que usamos para selecionar qual elemento no HTML que queremos estilizar. Permitem estilizar com precisão, seja por tags, classes, IDs, atributos, estados ou relações hierárquicas. Usado para criação de designs personalizados e responsivos.



**Tags**

Existem diversas maneiras de escolhermos esse seletores, uma das formas comum é usando a própria tag do html, que é basicamente escrever o nome da tag, seguida de um abre e fecha chaves contendo as propriedades a serem estilizadas. Por exemplo, h1 { color: green; }

​		![image-20241216120815979](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241216120815979.png)	![image-20241216120824095](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241216120824095.png)	![image-20241216120908696](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241216120908696.png)



- **O que é:** seleciona todos os elementos de um tipo específico.
- **Nível semântico:** baixo.
- **Quando usar:** para aplicar estilos globais ou básicos a elementos específicos.



**Classes**

É outra forma bem comum, consiste basicamente em atribuir uma classe a uma tag e estilizar essa classe específica no css (lembrando de sempre utilizar um . (ponto) antes). Por exemplo, um p com classe paragrafo, ficaria .paragrafo { color: blue }

​	![image-20241216124612442](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241216124612442.png)	![image-20241216124621310](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241216124621310.png)	![image-20241216124634214](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241216124634214.png)



- **Nível semântico:** médio.
- **Quando usar:** para aplicar estilos reutilizáveis a múltiplos elementos.



**Id**

Dessa vez nós atribuímos uma id na tag do html, porém o ID é mais específico (lembrando de sempre utilizar uma # (hashtag) antes). O ideal é usar **UM ID POR PÁGINA**. 

O id não é muito aconselhável para estilização, sendo mais indicado para fazer interação com o javascript (o que será visto mais para frente no curso), **é mais aconselhado utilizar classes para estilizar.**

​     <img src="C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241216130006473.png" alt="image-20241216130006473" style="zoom:80%;" />	![image-20241216130015278](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241216130015278.png)	<img src="C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241216130027174.png" alt="image-20241216130027174" style="zoom:80%;" />



- **Nível semântico:** alto.
- **Quando usar:** para estilizar um único elemento exclusivo. Evite usar para reutilização.



**\* *(asterisco/reset)***

O seletor universal (\*) aplica estilos a **todos os elementos** da página. É usado para "resetar" os estilos padrão aplicados pelos navegadores, garantindo uniformidade no design. Geralmente define margens, paddings e bordas como 0 para evitar inconsistências entre navegadores.

Por exemplo, ao utilizar o * e dando um padding de 0, tudo o que contém naquela página receberá esse propriedade.

​	![image-20241216131608158](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241216131608158.png)		![image-20241216131759360](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241216131759360.png)



- **Nível semântico:** muito baixo, pois é genérico e aplica-se a todos os elementos, sem distinção.
- **Quando usar:** quando deseja uma base neutra para construir o layout. Use com cautela em projetos grandes para evitar impacto desnecessário na performance.



**Duas classes *(ou mais)*** 

Consiste em aplicar estilos a elementos que possuem **duas ou mais classes simultaneamente**. Permite maior especificidade e controle ao estilizar elementos com combinações específicas de classes.

Por exemplo, dois h3 com duas classes, sendo uma igual entre eles e duas distintas, ao estilizar no css devemos colocar as classes com . (ponto) + classe, seguida de outro . (ponto) + outra classe.

![image-20241216134054847](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241216134054847.png)![image-20241216134105980](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241216134105980.png) 

![image-20241216134147222](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241216134147222.png)

Dessa forma, .titulo.vermelho estiliza apenas os elementos que possuem **ambas as classes** (titulo e vermelho), permitindo que, caso queira, estilize o titulo em um campo separado (.titulo), abrangendo a todos os elementos que possuam classe "título", mas não se contendo a apenas titulos vermelhos, ou laranjas, por exemplo. Assim como, também, o *vermelho* e o *laranja* viram classes e podem ser estilizadas separadamente ou incluídas em outras tags para estilizar.



- **Nível semântico:** médio-alto, pois combina classes para criar regras mais específicas e claras.
- **Quando usar:** quando precisa estilizar variações específicas de um mesmo componente ou elemento. Para evitar criar classes redundantes e promover reutilização e organização no código CSS.



**, *(vírgula)***

É uma técnica usada para aplicar o **mesmo estilo** a múltiplos seletores separados por vírgulas. Simplifica o código ao evitar repetição, aplicando regras comuns a diferentes elementos ou seletores de uma só vez.

  <img src="C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241216140134947.png" alt="image-20241216140112846" style="zoom:80%;" />	![image-20241216140157916](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241216140157916.png)	![image-20241216140302249](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241216140302249.png)



- **Nível semântico:** médio, pois mantém clareza e organização sem perder significado.
- **Quando usar:** para definir estilos compartilhados entre elementos que precisam ter o mesmo comportamento visual. Ao evitar duplicação de código para estilos iguais em diferentes seletores.



**Classe filha**

Refere-se à aplicação de estilos a um **elemento filho** dentro de um elemento pai, utilizando o seletor de classe do pai seguido pelo seletor de classe do filho, separados por um espaço. Especifica o estilo de elementos filhos dentro de um elemento pai, garantindo que a estilização seja aplicada apenas quando o elemento filho estiver dentro de um pai específico.

Por exemplo, uma tag pai com uma classe (section+class), tem uma tag filha com outra classe (p+class), podemos estilizar no css utilizando a classe pai (com um ponto na frente), dar um espaço e colocar a classe filha (com um ponto na frente também).

​	<img src="C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241216152550290.png" alt="image-20241216152550290" style="zoom:80%;" />	![image-20241216152643848](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241216152643848.png)



- **Nível semântico:** alto, pois indica claramente a hierarquia e a relação entre os elementos.
- **Quando usar:** para estilizar elementos com base em sua estrutura hierárquica. Quando se deseja aplicar regras específicas a filhos dentro de um elemento pai com determinada classe.



**\> *(sinal de maior)*** 

Seleciona apenas os **filhos diretos** de um elemento pai, ignorando os descendentes mais profundos (neto, bisneto etc). Aplica estilos exclusivamente aos elementos que são filhos imediatos de um elemento pai, oferecendo maior controle e evitando afetar elementos mais internos na hierarquia.

Por exemplo, uma div (pai) que tem um parágrafo (filho) **dentro**, ficaria "div > p" e isso quer dizer então que estamos selecionando todos os P*arágrafos* que estão dentro do elemento div (também pode ser uma classe, um id etc, a div é apenas um exemplo, como nos outros casos). 

​    ![image-20241216155124669](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241216155124669.png)	![image-20241216155153522](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241216155153522.png)

*Se a div tiver vários parágrafos, todos serão estilizados, sendo assim, não seria necessário acrescentar uma classe, por exemplo, em cada um para estilizar* 



- **Nível semântico:** alto, pois reflete com precisão a relação direta entre pai e filho.
- **Quando usar:** quando há necessidade de estilizar apenas os filhos imediatos de um elemento. Para evitar que estilos se propaguem para elementos descendentes não desejados.
- **Diferença div p {} e div > p {}**: div p {} seria "descendente", isso quer dizer que ele seleciona QUALQUER elemento p que esteja dentro de qualquer outro elemento, em qualquer nível de PROFUNDIDADE (ou seja, filhos, netos, bisnetos, etc). Já o div > p {} seleciona somente os filhos diretos dessa div, ou seja, não seleciona os elementos p que são netos, binestos, etc, somente os filhos.



**\+ *(sinal de mais)***

Seleciona um elemento **irmão** adjacente que aparece **imediatamente** após outro elemento. Aplica estilos ao primeiro elemento que segue diretamente outro no mesmo nível hierárquico.

Por exemplo, temos três tags, uma div seguida de dois p (1° div, 2° p, 3° p), porém, dessa vez, os p **não estão dentro** da div, os três possuem a mesma hierarquia (são irmãos). Utilizando o +, podemos estilizar o primeiro irmão (2° p) e qualquer irmão seguinte não será afetado.

![image-20241216160717001](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241216160717001.png)	![image-20241216160825673](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241216160825673.png)



- **Nível semântico:** médio, pois destaca relações entre elementos próximos, mas depende da ordem no *DOM*¹.
- **Quando usar:** quando é necessário estilizar elementos que seguem imediatamente outro específico. Para criar diferenciações visuais com base na proximidade entre elementos.



¹ **DOM (Document Object Model)** é como um "mapa" da página web que transforma o HTML em uma estrutura organizada, parecida com uma árvore. Cada parte da página, como textos, imagens e botões, vira um "nó" nessa árvore.



**Para que serve:**

- **Mudar o conteúdo da página:** você pode usar JavaScript para alterar textos, imagens ou cores sem recarregar a página.
- **Adicionar interatividade:** dá para criar ações, como um botão que muda algo quando clicado.
- **Controlar a estrutura:** permite mexer nos elementos, criar ou apagar partes da página.



**Atributo *[attr]*** 

Seleciona elementos com atributos específicos. Permite aplicar estilos a elementos com base nos atributos que possuem. É útil para personalizar comportamentos específicos sem precisar adicionar classes extras.

Por exemplo, criando duas tags a, porém uma com target *(que faz com que ao clicar no link a página seja aberta em uma nova aba)* e a outra sem *(que faz com que ao clicar no link, a nova página sobreponha a que estamos visualizando no momento)*

![image-20241216162138838](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241216162138838.png)

Para estilizar escrevemos a tag *(que nesse caso é a, mas também poderia ser uma classe, id etc)*, seguida de colchetes e o valor do atributo e, feito isso, fazemos o abre e fecha chaves { } normalmente.

![image-20241216162916947](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241216162916947.png)

​    <img src="C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241216163010570.png" alt="image-20241216163010570" style="zoom:80%;" />     <img src="C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241216163042163.png" alt="image-20241216163042163" style="zoom:80%;" />



- **Nível Semântico:** Médio a alto, dependendo do uso. Usa atributos já presentes no HTML, sem modificar a estrutura.
- **Quando Usar:** Para estilizar elementos com características ou estados específicos. Adiciona estilos com base no comportamento ou tipo de elemento, sem criar classes adicionais. Ideal para manter o código mais limpo e eficiente.



**Aplicando transformações com transform**

Permite modificar a aparência de um elemento no html (imagem, div, etc), como rotacionar (rotate), redimensionar (scale), mover (translate) ou inclinar (skew), sem alterar sua posição real no *DOM*.

- **Nível semântico**: baixo. Focado apenas em estilização visual, sem significado estrutural.
- **Quando utilizar**: para criar animações, efeitos visuais interativos e designs dinâmicos, especialmente em interfaces modernas e atraentes.



[Link do W3Schools com mais valores para a propriedade transform](https://www.w3schools.com/cssref/css3_pr_transform.asp?_gl=1*6afb3d*_ga*MTEwMjE3ODAuMTcyODM5NjEwNA..*_ga_37GXT4VGQK*MTczNDM3NzUwNy44NC4xLjE3MzQzNzc1MjQuMC4wLjA.)



Estrutura do HTML usado durante a aula:

![image-20241216173730877](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241216173730877.png)

Todas as imagens dos exemplos foram inicialmente resetadas para ter uma largura de 200px

​				![image-20241216165205936](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241216165205936.png)		<img src="https://cdn.areademembros.com/files/instancia_3760/editor/qtjsuD2UYP5uP0ReeexjfBPvYjqd1k6W2WqsOGoG.jpg" alt="img" style="zoom:50%;" />

*Atentando-se a estrutura, depois de img não é dado um espaço para digitar a classe, eles ficam grudados (por exemplo, img.scale { }), usar o img antes da classe deixa mais específico.*



**Scale**

Redimensiona o tamanho do elemento proporcionalmente. Serve para ampliar ou reduzir elementos. No exemplo, vamos utilizar o valor scale(), para que altere o eixo X (vertical) e Y (horizontal), respectivamente *(mas também é possível utilizar o scaleX para alterar somente o eixo X ou o scaleY para alterar somente o eixo Y)*.

![image-20241216165859052](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241216165859052.png)	![image-20241216165925208](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241216165925208.png)

Um scale(2, 3) significa que está aumentando 2x no eixo X e 3x no eixo Y, deixando, assim, a imagem esticada *(maior verticalmente e "menor" horizontalmente)*.



**Rotate**

Gira o elemento em torno de um ponto fixo (normalmente o centro). Serve para criar efeitos de rotação, como girar ícones ou imagens. Assim como no exemplo anterior, há também o rotateX e rotateY, mas vamos utilizar o rotate() que abrange os dois.

No caso do rotate, o valor a ser atribuito será em graus, "deg" (degrees, em inglês).

​		![image-20241216171011369](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241216171011369.png)		![image-20241216171105593](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241216171105593.png)

Ao rotacionar algo utilizando o rotateX ou Y, quer dizer que vc quer girar o elemento referente ao eixo em questão.

![image-20241216172041526](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241216172041526.png)	![image-20241216172052495](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241216172052495.png)	**ROTATE Y**

![image-20241216172116728](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241216172116728.png)	   ![image-20241216172133889](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241216172133889.png)	**ROTATE X**

*Não fica tão bacana, já que para rotacionar é preciso dos dois eixos.*



**Translate**

Move o elemento no eixo X ou Y. Serve para posicionar elementos sem alterar o fluxo do layout. Faz uma translação do elemento na tela em 2D, horizontalmente e verticalmente.

Também temos a opção do translateX e Y, para que essa movimentação seja focada em um eixo específico. O valor atribuído ao translate deve ser em pixels.

![image-20241216173807207](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241216173807207.png)	![image-20241216173916954](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241216173916954.png)



**Trabalhando com variáveis**

Como o CSS é uma linguagem de marcação, muitas pessoas não sabem que é possível utilizar variáveis nele, mas essas variáveis irão nos ajudar bastante na estilização, mantendo o código simples e ajudando na manutenção. 

As variáveis podem não ser compatíveis com alguns navegador, podemos olhar essa compatibilidade no [CSS Variables](https://www.w3schools.com/css/css3_variables.asp?_gl=1*2z3nv4*_ga*MTEwMjE3ODAuMTcyODM5NjEwNA..*_ga_37GXT4VGQK*MTczNDM4MDU3NS44NS4xLjE3MzQzODE2MTAuMC4wLjA.).

É o uso de valores reutilizáveis definidos com o prefixo -- (variáveis CSS). Serve para simplificar a estilização, manter a consistência (cores, espaçamentos, fontes) e facilitar a manutenção do código.

- **Nível semântico:** baixo. Afeta apenas a aparência e facilita a gestão do estilo.
- **Quando utilizar:** em projetos com várias páginas ou componentes que compartilham o mesmo design. Para mudanças globais rápidas, como alterar o tema de cores.



Estrutura do HTML utilizada na aula:

![image-20241216175714674](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241216175714674.png)



Digamos que queira colocar um tamanho de fonte e uma cor igual em todos os elementos criados. Ao invés de fazer como anteriormente, tendo que dar propriedades e valores um a um e deixando o código repetitivo. 

As variáveis podem ter um escopo global ou local. **Global** pode ser usada em todos os estilos do documento e a **local** só poderá ser utilizada naquele seletor em que ela foi criada.



**Global**

São definidas no seletor :root (é a raiz do documento, que no caso é o html), ficam acessíveis em todo o documento. Servem para manter consistência e reutilização em todo o projeto. Mais utilizada para alterar valores amplamente usados, como cores, fontes e espaçamentos.

Após criar o root com as variáveis desejadas, para poder aplicá-las ao elemento, é necessário utilizar "var(variavel, outra opção caso dê problema)".

​	<img src="C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241216182303731.png" alt="image-20241216182303731" style="zoom:80%;" />			<img src="C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241216182316358.png" alt="image-20241216182316358" style="zoom:80%;" />

Dessa forma, caso precise fazer alguma alteração na cor padrão, por exemplo, basta apenas ir no :root e trocar, deixando a manutenção fácil. 

É sempre bom colocar as variáveis no topo do CSS, para que sejam localizadas facilmente.

Vantagens: deixa o código muito mais limpo e torna as mudanças mais simples.



**Local**

Definidas dentro de um seletor específico, sendo acessíveis apenas no seu escopo. Serve para personalizar estilos específicos sem afetar o restante do código. Mais utilizadas para ajustes únicos em componentes ou seções específicas.

No exemplo, foi criado um escopo dentro do h2 com as próprias variáveis dele. Podemos observar que essa variável é válida apenas dentro daquele seletor, os outros elementos continuam pegando a configuração do root.

![image-20241216182948586](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241216182948586.png)

No caso a variável mudou a cor padrão para vermelho, então o texto e o fundo ficaram vermelhos e os outros elementos continuam seguindo a variável da raiz com a cor padrão verde. 



### **PARTE 2**

**Flexbox**

Permite criar uma estrutura de layout que serve para organizar elementos dentro de um container, dispondo, alinhando e distribuindo o espaço entre eles de forma eficiente. Mais indicado para layouts de pequena escala e/ou componentes de um site *(ao contrário do grid, que é indicado para layout de grande escala, como por exemplo de uma página inteira)*. Basicamente, ele facilita a criação de uma estrutura de layouts sem precisar do uso do float ou position.

O flexbox trabalha com o conceito de pai e filho, onde o pai é chamado de flex container e os filhos são chamados de flex item.

![image-20241217151308523](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241217151308523.png)

Ele é um modelo de layout flexível que possui dois eixos, o principal e o transversal. As propriedades e valores do CSS vao alterar o comportamento de acordo com a direção dos eixos.

![image-20241217155038562](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241217155038562.png)

O container roxo seria como se fosse a div class="container" da imagem anterior. Os três elementos seriam os flex itens.

- O eixo principal inicia na esquerda e finaliza na direita
- O eixo transversal inicia em cima e termina em baixo.

**O eixo transversal SEMPRE vai ser perpendicular ao eixo principal.**

O comportamento desses dois eixos é definido pela propriedade css flex-direction, é ela quem vai ditar as regras dos eixos. O flex direction possui 4 valores principais: row; row-reverse; column; column-reverse.

**Display Flex:** Define um contêiner flexível, organizando seus elementos filhos de maneira eficiente em linhas ou colunas. Facilita alinhamento e distribuição de espaço.



**Row**

Se o flex direction estiver definido como **row** (que significa "linha" em inglês), o eixo principal vai se mover na horizontal e o eixo transversal vai se mover na vertical, como na imagem introdutória. Itens organizados em linha, da esquerda para a direita.

![image-20241217155038562](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241217155038562.png)



**Column**

Se o flex direction estiver definido como **column** (que significa "coluna" em inglês), então os eixos vão mudar a sua direção, como na imagem abaixo. O eixo principal passará a se mover na vertical e o eixo transversal passará a se mover na horizontal.  Itens organizados em linha, da direita para a esquerda. Itens organizados em coluna, de cima para baixo.

<img src="C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241217153237885.png" alt="image-20241217153237885"  />



**Row reverse**

Se o flex direction estiver definido como **row-reverse**, a direção dos eixos se manterá a mesma que o row (horizontal), mas a única diferença está no início principal (que agora é na direita) e fim principal (que agora é na esquerda). Itens organizados em linha, da direita para a esquerda.

![image-20241217155224413](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241217155224413.png)



**Column reverse**

Se o flex direction estiver definido como **column-reverse**, então os eixos vão mudar a sua direção, como na imagem abaixo. O eixo principal passará a se mover na horizontal e o eixo transversal passará a se mover na vertical. *Vai começar pelo item 1, 2, 3, porém de baixo para cima.* Itens organizados em coluna, de baixo para cima.

![image-20241217154749645](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241217154749645.png)



**Quando utilizar cada um:**

- **Row:** Layouts horizontais comuns (menu de navegação).
- **Row-reverse:** Para inverter a ordem visual em layouts horizontais.
- **Column:** Layouts verticais (listas, formulários).
- **Column-reverse:** Para inverter a ordem visual em layouts verticais.



**Flex direction**

Com o flex direction vamos conseguir alterar a posição dos elementos/itens dentro do container flexível e alterar o eixo também.

Estrutura do html usado em aula para os exemplos:

<img src="C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241217160528643.png" alt="image-20241217160528643" style="zoom:67%;" />

Cada h1 está com uma div pai e três divs filhas (flex itens), como visto no exemplo da aula anterior.

Acima, dentro do head, foi dado um link para duas páginas css, globals e style.

O css globals está com algumas estilizações globais feitas:

​		![image-20241217161119643](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241217161119643.png)		<img src="C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241217162142224.png" alt="image-20241217162142224" style="zoom:50%;" />

**Lembrando que precisamos aplicar a propriedade display com o valor flex no container pai, no qual vamos querer aplicar as propriedades.**

Por padrão, as divs ficam em bloco, um acima do outro. Para estilizar utilizando o flex, devemos dar o nome da classe e atribuir o display: flex.

Na maioria das vezes **não** iremos utilizar o row-reverse e o column-reverse, 90% das vezes será o row ou column. Um exemplo de uso seria na responsividade de uma página que pode ser row no desktop e column no mobile.



**Container row**

O container pai será a div class='container row'. Basta escrever a classe e dar a propriedade de display flex na folha de estilos. Por padrão, o flex direction sempre será row (default), no caso de ser um elemento row, não é necessário atribuir a propriedade de flex-direction: row, mas nos outros casos sim.

Os itens estão sendo dispostos ao longo de uma única linha, um ao lado do outro.

​		![image-20241217162805198](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241217162805198.png)		<img src="C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241217162819640.png" alt="image-20241217162819640" style="zoom:67%;" />



**Container row-reverse**

O container pai será a div class='container row-reverse'. Basta escrever a classe e dar a propriedade de display flex na folha de estilos. Agora será necessário dar a propriedade flex-direction: row-reverse.

Os itens estão sendo dispostos ao longo de uma única linha, porém ela vai dispor os itens de forma reversa, então a linha começará da direita para a esquerda, um ao lado do outro.

​    ![image-20241217164828240](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241217164828240.png)        <img src="C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241217164847919.png" alt="image-20241217164847919" style="zoom: 67%;" />



**Container column**

O container pai será a div class='container column'. Basta escrever a classe e dar a propriedade de display flex na folha de estilos. Agora será necessário dar a propriedade flex-direction: column. 

Com isso, queremos dizer que queremos que os filhos fiquem em coluna, um embaixo do outro. Lembrando que o eixo muda, com o column o início principal passa a ser em cima e o fim embaixo (principal na vertical e transversal na horizontal).

​	![image-20241217165238623](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241217165238623.png)   	<img src="C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241217165253680.png" alt="image-20241217165253680" style="zoom:67%;" />



**Container column-reverse**

O container pai será a div class='container column-reverse'. Basta escrever a classe e dar a propriedade de display flex na folha de estilos. Agora será necessário dar a propriedade flex-direction: column-reverse.

Com isso, queremos dizer que queremos que os filhos fiquem em coluna, um em cima do outro. Lembrando que o eixo muda novamente, como ele é o column reverse, então o início principal passa a ser embaixo e o fim em cima (principal na vertical e transversal na horizontal).

   ![image-20241217165951432](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241217165951432.png)    <img src="C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241217170004521.png" alt="image-20241217170004521" style="zoom:67%;" />



**Justify Content**

Seria algo como "justificar o conteúdo" (traduzindo para o português). Define como os itens dentro de um contêiner flexível são alinhados ao longo do eixo principal (horizontal em row, vertical em column), ou seja, ele se move ao longo do eixo principal. Ajuda na distribuição do espaço entre os elementos.

O valor padrão do justify content é ter flex-direction: row e ser flex-start.

Estrutura do html usado em aula como exemplo:

​	  <img src="C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241217171033821.png" alt="image-20241217171033821" style="zoom:50%;" />      	<img src="C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241217171054321.png" alt="image-20241217171054321" style="zoom:67%;" />

Cada h1 está com uma div pai e três divs filhas (flex itens), como visto no exemplo da aula anterior.

Acima, dentro do head, foi dado um link para duas páginas css, globals e style.

O css globals está com algumas estilizações globais feitas:

![image-20241217171525943](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241217171525943.png)

**Lembrando que o justify content também é uma propriedade de flex container, isso quer dizer que é uma propriedade de css que deve ser aplicada no container (ou seja, no pai), para que os filhos sejam alinhados de acordo com o valor definido.**

O ideal é utilizá-los sempre que precisar organizar itens flexíveis em um layout, como menus de navegação, botões, ou listas de elementos, garantindo alinhamento e espaçamento adequados.



**Flex-start**

Esse é o valor padrão do justify contant. Os itens ficam alinhados ao **início** do eixo principal (horizontal), deixando o espaço restante no final. Ideal para layouts onde o conteúdo deve ficar agrupado à esquerda ou ao topo.

   ![image-20241217174033992](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241217174033992.png)	<img src="C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241217174856460.png" alt="image-20241217174856460" style="zoom:67%;" />

Como exemplo, para visualizar melhor outras situações, caso fosse dado um flex-direction: column, ele alinharia os itens no início ao longo do eixo principal, ou seja, agora na vertical (de cima para baixo)

​    ![image-20241217174604485](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241217174604485.png)	<img src="C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241217174918305.png" alt="image-20241217174918305" style="zoom:67%;" />



**Flex-end**

É o oposto do flex-start. Os itens ficam alinhados ao **final** do eixo principal, deixando o espaço restante no início. Útil quando é necessário agrupar conteúdo à direita ou na base. Dessa forma, podemos ver que os números não ficaram em ordem decrescente (como acontece no row-reverse).

​      ![image-20241217174958290](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241217174958290.png)	<img src="C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241217175011980.png" alt="image-20241217175011980" style="zoom:67%;" />

Como exemplo, para visualizar melhor outras situações, caso fosse dado um flex-direction: column, ele alinharia os itens no início ao longo do eixo principal, ou seja, agora na vertical (de baixo para cima)

​      ![image-20241217175252757](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241217175252757.png)	<img src="C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241217175302930.png" alt="image-20241217175302930" style="zoom:67%;" />



**Center**

Os itens são **centralizados** no eixo principal, com espaços iguais antes e depois dos elementos. Ideal para destacar ou centralizar elementos em layouts minimalistas.

Esse é um dos valores mais utilizados, justamente porque ele alinha os itens no centro do container ao longo do eixo principal (horizontal, por padrão).

​         ![image-20241217175419620](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241217175419620.png)	<img src="C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241217175433262.png" alt="image-20241217175433262" style="zoom:67%;" />

Como exemplo, para visualizar melhor outras situações, caso fosse dado um flex-direction: column, ele alinharia os itens no início ao longo do eixo principal, ou seja, agora na vertical. Isso é muito bom para mudar a visualização mobile.

​        ![image-20241217175821657](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241217175821657.png)	<img src="C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241217175834527.png" alt="image-20241217175834527" style="zoom:67%;" />



**Space-between**

A tradução dele seria algo como "espaçar entre". Ele espaça os itens de forma uniforme, deixando o **primeiro** alinhado ao início e o **último** ao final, com espaço apenas **entre** os itens. Muito utilizado em menus ou cabeçalhos, onde os itens precisam ser distribuídos igualmente com bordas alinhadas.

​      ![image-20241217180014694](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241217180014694.png)  <img src="C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241217180053136.png" alt="image-20241217180053136" style="zoom:67%;" />

Como exemplo, para visualizar melhor outras situações, caso fosse dado um flex-direction: column, ele alinharia os itens no início ao longo do eixo principal, ou seja, agora na vertical (ao longo da altura). Isso é muito bom para mudar a visualização mobile.

![image-20241217180356662](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241217180356662.png)	<img src="C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241217180418460.png" alt="image-20241217180418460" style="zoom:67%;" />



**Space-around**

Adiciona espaço **ao redor** de cada item, mas as bordas externas têm metade do espaçamento interno. Cria um layout mais fluido e espaçado, mas com proporções visuais leves. Ele é bem parecido com o space-between, porém dará espaço às bordas também.

 ![image-20241217181353132](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241217181353132.png)	<img src="C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241217181406562.png" alt="image-20241217181406562" style="zoom:67%;" />

Como exemplo, para visualizar melhor outras situações, caso fosse dado um flex-direction: column, ele alinharia os itens no início ao longo do eixo principal, ou seja, agora na vertical (ao longo da altura). Isso é muito bom para mudar a visualização mobile.

  ![image-20241217181555850](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241217181555850.png)	<img src="C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241217181610264.png" alt="image-20241217181610264" style="zoom:67%;" />



**Space-evenly**

Distribui o espaço de forma **igual** (uniformemente) entre todos os itens, incluindo as bordas externas. Usado para criar uma distribuição perfeitamente equilibrada, ideal para layouts simétricos. É bem parecido com o space around, mas todos os espaços tem o mesmo tamanho *(no around os espaços entre os itens é maior e as bordas menor, no evenly os espaços de borda e entre itens são os mesmos)*.

  ![image-20241217181626967](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241217181626967.png)	<img src="C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241217181638273.png" alt="image-20241217181638273" style="zoom:67%;" />

Como exemplo, para visualizar melhor outras situações, caso fosse dado um flex-direction: column, ele alinharia os itens no início ao longo do eixo principal, ou seja, agora na vertical (ao longo da altura). Isso é muito bom para mudar a visualização mobile.

  ![image-20241217181748158](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241217181748158.png)	<img src="C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241217181801763.png" alt="image-20241217181801763" style="zoom:67%;" />



**Align Items**

Dá para pensar no align-items como se fosse o justify-content, mas para alinhar os itens no início ao longo do eixo transversal *(que fica na vertical, em um container com flex direction row -padrão)*. Ele também é uma propriedade de flex container.

Utilize quando precisar organizar verticalmente os itens em um contêiner flex, garantindo alinhamento consistente e melhor apresentação.



Estrutura do html usado em aula como exemplo:

<img src="C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241218121437007.png" alt="image-20241218121437007" style="zoom:67%;" />

Cada h1 está com uma div pai e três divs filhas, como visto no exemplo da aula anterior.

Acima, dentro do head, foi dado um link para duas páginas css, globals e style.

O css globals está com algumas estilizações globais feitas:

![image-20241218111655716](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241218111655716.png)



**Flex-start**

Alinha os itens ao **início** do eixo transversal.

​	![image-20241218112436926](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241218112436926.png)	<img src="C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241218112451295.png" alt="image-20241218112451295" style="zoom:67%;" />

Como exemplo, para visualizar melhor outras situações, caso fosse dado um flex-direction: column, ele alinharia os itens no início ao longo do eixo principal, ou seja, agora na vertical (de cima para baixo) e o eixo transversal passa a ser na horizontal (esquerda para a direita).

​	![image-20241218112830107](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241218112830107.png)	<img src="C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241218112841584.png" alt="image-20241218112841584" style="zoom:67%;" />

<img src="C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241218113005516.png" alt="image-20241218113005516" style="zoom:50%;" />	**EXEMPLO VISUAL**



**Flex-end**

Alinha os itens no **final** ao longo do eixo transversal, que se encontra na vertical.

​	![image-20241218113050764](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241218113050764.png)	<img src="C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241218113102525.png" alt="image-20241218113102525" style="zoom:67%;" />

Como exemplo, para visualizar melhor outras situações, caso fosse dado um flex-direction: column, ele alinharia os itens no início ao longo do eixo principal, ou seja, agora na vertical (de cima para baixo) e o eixo transversal passa a ser na horizontal.

​	![image-20241218113133697](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241218113133697.png)	<img src="C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241218113148159.png" alt="image-20241218113148159" style="zoom:67%;" />

<img src="C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241218115326893.png" alt="image-20241218115326893" style="zoom:50%;" />	**EXEMPLO VISUAL**



**Center**

É o que mais vamos utilizar. Ele centraliza os itens no eixo transversal, que se encontra na vertical.

​		![image-20241218113212968](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241218113212968.png)	<img src="C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241218113224425.png" alt="image-20241218113224425" style="zoom:67%;" />

Como exemplo, para visualizar melhor outras situações, caso fosse dado um flex-direction: column, ele alinharia os itens no início ao longo do eixo principal, ou seja, agora na vertical (de cima para baixo) *e o eixo transversal passa a ser na horizontal*. Isso é muito bom para alinhar os itens ao centro com mais facilidade.

​	![image-20241218113252854](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241218113252854.png)	<img src="C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241218113309539.png" alt="image-20241218113309539" style="zoom:67%;" />



**Stretch**

Estica os itens para ocupar **toda a altura** do contêiner (padrão) na vertical. O stretch não vai funcionar se tivermos aplicado uma altura ou largura fixa. **É o padrão do align-items, se não definir um valor, ele será sempre stretch**.

​	![image-20241218113326642](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241218113326642.png)	<img src="C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241218113339796.png" alt="image-20241218113339796" style="zoom:67%;" />

Como exemplo, para visualizar melhor outras situações, caso fosse dado um flex-direction: column, ele alinharia os itens no início ao longo do eixo principal, ou seja, agora na vertical (de cima para baixo) e o eixo transversal passa a ser na horizontal, ou seja, aumentará a **largura total** deles.

​	![image-20241218113416121](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241218113416121.png)	<img src="C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241218113430646.png" alt="image-20241218113430646" style="zoom:67%;" />



**Baseline**

Alinha os itens pela **linha de base** do texto. Aparentemente parece que estamos usando o flex-start, mas na verdade, ele está alinhando os itens pela linha de base do conteúdo, ou seja, de acordo com o elemento que possui o maior conteúdo, os seguintes serão alinhados a ele, ainda que isso faça com que fique um espaço "sobrando" de borda nos outros itens.

​	![image-20241218113448886](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241218113448886.png)	<img src="C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241218113503208.png" alt="image-20241218113503208" style="zoom:67%;" />

Mudando o tamanho da fonte das outras divs (segunda e terceira), será possível visualizar melhor como funciona esse alinhamento.

​	![image-20241218121324869](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241218121324869.png)	<img src="C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241218121329712.png" alt="image-20241218121329712" style="zoom:67%;" />



No align itens baseline, o flex direction column não é utilizado, pois ele se aplica ao alinhamento de texto somente na horizontal (e o column deixa em coluna vertical).



**Flex wrap e Flex flow**

São propriedades do CSS Flexbox que controlam a organização dos elementos em um container (quebra de linhas).

Estrutura do html usado como exemplo na aula:

<img src="C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241218123619054.png" alt="image-20241218123619054" style="zoom:50%;" />

Acima, dentro do head, foi dado um link para duas páginas css, globals e style.

O css globals está com algumas estilizações globais feitas:

![image-20241218123643345](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241218123643345.png)



**Flex wrap**

Faz com que os itens quebrem para a próxima linha, se necessário e move os itens ao longo do eixo **transversal** *(na vertical em row ou horizontal em column)*. Por padrão eles não quebram, isso faz com que os flex items sejam compactados, sempre respeitando o limite do conteúdo (largura, altura). Quando não há mais espaço disponível dentro do container, ele quebra os itens ao longo do eixo transversal. O flex-wrap também é uma propriedade de flex container.

​		![image-20241218125630215](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241218125630215.png)		<img src="C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241218125643417.png" alt="image-20241218125643417" style="zoom:67%;" />

Como o flex-direction está definido como row (por padrão), os itens estão se movendo na horizontal e quando não houver mais espaço, ele vai quebrar para baixo, na vertical.

Se o flex-direction estiver definido como column, quando não houver mais espaço disponível na **altura** do container, ele vai quebrar os itens para a horizontal (da esquerda para a direita).

​	![image-20241218130619207](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241218130619207.png)		<img src="C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241218130642480.png" alt="image-20241218130642480" style="zoom:67%;" />



**Flex nowrap**

Itens ficam em uma única linha, que é o **comportamento padrão**. Os flex items se adequam ao tamanho do container.

​		![image-20241218125450359](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241218125450359.png)		<img src="C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241218125514814.png" alt="image-20241218125514814" style="zoom:67%;" />

No exemplo acima as 12 divs foram se modificando e ficando mais estreitas, para que todas pudessem caber dentro do container, conforme o número de elementos aumente ou diminua, os tamanhos vão se readequando para caberem.



**Flex wrap-reverse**

Quebra os itens para a próxima linha, mas na **direção inversa**. É parecido com o wrap, mas, ao invés de quebrar os itens na ordem natural, ele inverte a direção de quebra. Quando os itens não couberem mais em uma única linha, eles irão quebrar para a linha de cima.

​	![image-20241218125708377](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241218125708377.png)		<img src="C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241218125718666.png" alt="image-20241218125718666" style="zoom:67%;" />

Como o flex-direction está definido como row (por padrão), os itens estão se movendo na horizontal e quando não houver mais espaço, ele vai quebrar para cima, na vertical.

Se o flex-direction estiver definido como column, quando não houver mais espaço disponível na **altura** do container, ele vai quebrar os itens para a horizontal (porém começando da direita para a esquerda). O eixo transversal passa a ser na horizontal.

​	![image-20241218131023785](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241218131023785.png)		<img src="C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241218131037906.png" alt="image-20241218131037906" style="zoom:67%;" />



**Flex flow**

É uma **shorthand** (abreviação) para combinar flex-direction e flex-wrap. Usado para simplificar o código ao definir direção e quebra de linha juntas.

O primeiro parâmetro que passamos para o flex-flow é o valor do flex-direction;

O segundo parâmetro é o valor do flex-wrap.

​		![image-20241218132941998](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241218132941998.png)		<img src="C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241218133040785.png" alt="image-20241218133040785" style="zoom:50%;" />

A forma como é escrita fica mais limpa, mas não muda em nada os parâmetros e visualização da página, fica igualmente era no flex-wrap, porém encurtado.

Os valores padrões das propriedades quando utilizamos o flex-flow são row e nowrap.



**Align Content**

Alinha as linhas do container em relação ao eixo transversal (vertical, *ou de acordo com o flex-direction -row: vertical, column horizontal*), mas, muito importante, a propriedade **só funciona se houver mais de uma linha de flex items**, para isso o flex wrap precisa ter o valor wrap *(ou wrap-reverse)*. Além disso o efeito dela só poderá ser visualizado caso o container seja **maior que a soma das linhas dos itens**, ou seja, se não for definida uma altura para o container, essa propriedade não vai influenciar no layout.

O align content é muito parecido com o align items e justify content, isso porque ele pode ser considerado uma combinação entre as duas propriedades.

**Align-content** atua no **eixo cruzado (transversal)**, enquanto **justify-content** atua no **eixo principal**.

- **Alto nível semântico**: Alinha conteúdos de múltiplas linhas dentro do container flex.



Estrutura do html usado em aula como exemplo:

<img src="C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241218160837789.png" alt="image-20241218160837789" style="zoom: 67%;" />	<img src="C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241218160906290.png" alt="image-20241218160906290" style="zoom: 67%;" />

Acima, dentro do head, foi dado um link para duas páginas css, globals e style.

O css globals está com algumas estilizações globais feitas:

![image-20241218160932678](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241218160932678.png)



**Flex start**

Alinha as linhas no início do eixo transversal. Usado quando você quer agrupar as linhas no topo ou na esquerda.

​	![image-20241218162305938](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241218162305938.png)	<img src="C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241218162317235.png" alt="image-20241218162317235" style="zoom:67%;" />

Caso seja dado um flex-direction column, o eixo *(transversal)* passa a ser horizontal, fazendo com que os itens do container sejam alinhados no início da horizontal (dispostos na vertical, mas alinhados na vertical).

​	![image-20241218163211355](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241218163211355.png)	<img src="C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241218163227600.png" alt="image-20241218163227600" style="zoom:67%;" />



**Flex end**

Alinha as linhas no final do eixo transversal, porém agora será por baixo. Usado para agrupar as linhas no final (parte inferior ou direita).

​	![image-20241218162437497](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241218162437497.png)	<img src="C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241218162450334.png" alt="image-20241218162450334" style="zoom:67%;" />

Caso seja dado um flex-direction column, o eixo *(transversal)* passa a ser horizontal, alinhando os nossos itens ao longo da horizontal.

​	![image-20241218163755101](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241218163755101.png)	<img src="C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241218163807734.png" alt="image-20241218163807734" style="zoom:67%;" />

**Center**

Um dos mais utilizados (mais importante). Ele centraliza as linhas no meio do eixo cruzado, alinha os itens no centro ao longo do eixo transversal, que é vertical. Usando quando o objetivo é distribuir as linhas no centro. Foi usado de exemplo uma div com 3 filhas.

​	![image-20241218162514439](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241218162514439.png)		<img src="C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241218164251341.png" alt="image-20241218164251341" style="zoom:67%;" />

Quando o container possui mais itens é possível manter o alinhamento ao centro utilizando o justify-content. No exemplo agora foram usadas uma div com seis filhas.

​	![image-20241218164906431](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241218164906431.png)		<img src="C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241218164930434.png" alt="image-20241218164930434" style="zoom:67%;" />

Caso seja dado um flex-direction column, o eixo *(transversal)* passa a ser horizontal. Dessa forma, assim como foi feito anteriormente, também é possível utilizar o justify content quando houverem vários elementos para alinhar ao centro (como seis divs, por exemplo).

​	![image-20241218163826319](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241218163826319.png)		<img src="C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241218164313037.png" alt="image-20241218164313037" style="zoom:67%;" />



**Space between**

Distribui as linhas igualmente com **espaço entre elas**, sem espaços nas extremidades, ao longo do eixo transversal (vertical). É muito importante definir o flex-wrap como wrap, para que, quando não tiver mais espaço em linha disponível dentro do container, os itens possam quebrar pra baixo. Usado quando deseja uma distribuição organizada sem espaços externos.

​	![image-20241218162544280](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241218162544280.png)	<img src="C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241218162601985.png" alt="image-20241218162601985" style="zoom:67%;" />

Caso seja dado um flex-direction column, o eixo *(transversal)* passa a ser horizontal e o espaçamento do space-between passa a ser ao longo da linha do eixo horizontal.

​	![image-20241218163903192](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241218163903192.png)	<img src="C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241218163916105.png" alt="image-20241218163916105" style="zoom:67%;" />



**Space around**

As linhas têm **espaços iguais ao redor** (espaço nas extremidades é metade dos internos). Diferente do space between (row), no space around é dado um espaçamento entre as bordas e os itens, fazendo com que eles tenham o mesmo espaço ao redor de si mesmos (tanto em cima, quanto em baixo), ao longo do eixo transversal (que é vertical). Usado para distribuição equilibrada com margens externas menores.

​	![image-20241218162622481](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241218162622481.png)	<img src="C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241218162637618.png" alt="image-20241218162637618" style="zoom:67%;" />

Caso seja dado um flex-direction column, o eixo *(transversal)* passa a ser horizontal, então, quando não tiver mais espaço disponível em coluna, os itens serão espaçados ao longo da horizontal.

​	![image-20241218163936490](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241218163936490.png)	<img src="C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241218163951042.png" alt="image-20241218163951042" style="zoom:67%;" />



**Space evenly**

Distribui as linhas com **espaços completamente iguais**, inclusive nas extremidades (itens e bordas). Vai espaçar os itens um pouco **menos** do que o space-around. O espaço que há em cima, é o mesmo que o do meio, que também é o mesmo que há em baixo. Usado quando você quer uma distribuição uniforme.

​	![image-20241218162657394](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241218162657394.png)	<img src="C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241218170225863.png" alt="image-20241218170225863" style="zoom:67%;" />

Caso seja dado um flex-direction column, o eixo *(transversal)* passa a ser horizontal, mas o espaçamento continua sendo feito da mesma forma, o mesmo espaço que tem na borda esquerda, é o mesmo do centro e que também é o mesmo que o da direita.

​	![image-20241218170251312](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241218170251312.png)	<img src="C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241218170309618.png" alt="image-20241218170309618" style="zoom:67%;" />



**Stretch**

É a configuração padrão do align-content em containers **flex** com várias linhas. Faz com que as linhas flexíveis **estiquem** para preencher o espaço disponível (aumentando a **altura** deles, justamente por isso não devemos definir uma altura máxima fixa, senão ele não vai pegar) no **eixo transversal** (vertical). Utilizado quando você deseja que as linhas se expandam igualmente para **preencher todo o espaço vertical** (em row) ou horizontal (em column) no container.

![image-20241218171937219](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241218171937219.png)

*Para conseguir visualizar essa propriedade foi necessário fazer uma alteração no globals.css, **retirando a altura** (height) de 100px da .container div*

​	![image-20241218170536342](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241218170536342.png)		<img src="C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241218171955113.png" alt="image-20241218171955113" style="zoom:67%;" />

![image-20241218182637447](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241218182637447.png)

*Para conseguir visualizar essa propriedade foi necessário fazer uma alteração no globals.css, **retirando a largura** (width) de 100px da .container div* 

Caso seja dado um flex-direction column, o eixo *(transversal)* passa a ser horizontal fazendo com que a largura dos itens estique.

​	![image-20241218172306464](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241218172306464.png)		<img src="C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241218172557755.png" alt="image-20241218172557755" style="zoom:67%;" />



**Gap**

Propriedade usada para definir o **espaçamento** entre TODOS os itens dentro de um container flex ou grid. Serve para facilitar a criação de espaçamentos consistentes entre elementos, sem a necessidade de usar **margins** em cada item.

Ele também é um shorthand pra column-gap e row-gap (gap em coluna e gap em linha), isso, basicamente, significa que nós podemos escrever eles com dois valores.

- **Nível semântico alto**: deixa o código mais limpo e fácil de manter, garantindo alinhamento consistente.

Utilizamos sempre que precisar criar **espaços regulares** (uniformemente) entre itens de um container flex ou grid. Ideal para layouts organizados, como **listas**, **grelhas de imagens**, ou **menus horizontais/verticais**.



Estrutura do html usado em aula como exemplo:

<img src="C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241220104006653.png" alt="image-20241220104006653" style="zoom:67%;" />

Acima, dentro do head, foi dado um link para duas páginas css, globals e style.

O css globals está com algumas estilizações globais feitas:

<img src="C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241220104244512.png" alt="image-20241220104244512" style="zoom:67%;" />

Na página de styles, vamos permanecer fazendo da mesma forma, seguindo os padrões de flexbox. Atribuimos um display: flex, o flex-direction: row e o gap será de acordo com o tamanho da distância que quer entre os itens (no exemplo foi dado um gap de 50px):

![image-20241220105334883](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241220105334883.png)

<img src="C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241220105811743.png" alt="image-20241220105811743" style="zoom: 80%;" />

Nesse caso, como o gap é um shorthand, nós podemos colocar dois valores, se quisermos. No exemplo acima, da forma como foi usado, ele está colocando 50px de coluna e 50px de linha.

Podemos então utilizar o column-gap, que só vai funcionar se o flex-direction estiver definido como column, e o row-gap, que também só é aplicado se o flex-direction estiver como row.

Por exemplo, mudando o flex-direction para column e com o gap: 50px 20px, podemos visualizar que agora o gap entre um item e outro ficou de 50px em coluna:

![image-20241220113653126](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241220113653126.png)

![image-20241220114109459](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241220114109459.png)



Também podemos utilizar valores em porcentagem, no exemplo abaixo está sendo reconhecido 5% de gap em linha (pois o flex direction está como row). Se estivesse como column, o gap seria de 10% entre um flex item e outro.

![image-20241220114327970](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241220114327970.png)

Podemos utilizar o gap independentemente do eixo definido pelo flex direction, que pode  ser row, row-reverse, column, column-reverse, não tem restrições quanto a isso.

O gap só espaça os elementos filhos do container flex ou grid, ele não cria espaçamento ao redor, assim como o margin faz, por exemplo. O espaçamento criado é de um item pro outro e não em volta do item, espaçando a borda.

Usando o gap tendo apenas um valor (por exemplo, o gap: 50px que vimos no início), ele vai entender que será esse mesmo espaçamento tanto em row quanto em column (seria uma forma encurtada de usar).

A diferença entre o gap, margin e padding é:

- GAP é o espaçamento entre os itens dentro de um container flex ou grid. É somente utilizado com display flex ou display grid
- MARGIN é o espaçamento externo ao redor de um elemento, que, basicamente, separa ele de elementos vizinhos. Funciona com qualquer elemento html
- PADDING é o espaçamento interno, entre o conteúdo que existe dentro de um container e suas bordas. Também funciona com qualquer elemento html



**Grow**

Propriedade que define quanto espaço extra um item dentro de um container **flex** pode ocupar em relação aos outros itens (caso isso seja necessário). Serve para controlar como os itens se expandem para preencher o espaço disponível no container.

- **Alto nível semântico**: Facilita layouts responsivos, tornando o design mais adaptável e eliminando a necessidade de cálculos complexos de largura.

Utilizado quando desejar que um ou mais itens ocupem mais espaço disponível do container em relação aos outros. Também é util para criar layouts dinâmicos, como botões ou colunas de tamanhos proporcionais.

Nas aulas passadas, vimos sobre o flexbox container, que são as propriedades que são setadas no pai. 

Agora, vamos ver sobre as que são passadas nos **filhos**, iniciando pelo Grow.



Estrutura do html usado em aula como exemplo:

<img src="C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241220134445855.png" alt="image-20241220134445855" style="zoom:67%;" /><img src="C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241220135534831.png" alt="image-20241220135534831" style="zoom:50%;" />

Acima, dentro do head, foi dado um link para duas páginas css, globals e style.

O css globals está com algumas estilizações globais feitas:

<img src="C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241220134526383.png" alt="image-20241220134526383" style="zoom:67%;" />

Uma mudança que ocorreu no globals foi na estrutura das divs filhas, onde não aplicamos nenhuma altura e largura nelas.

Essa propriedade (grow) possui valores inteiros que vão de 0 a 3, quanto maior o valor, maior será a prioridade para esse item crescer e quanto menor for esse valor, menos espaço/prioridade esse item ocupará dentro do container.

Assim como nos flex-container, nesse nós também temos que aplicar o display flex no container pai, para poder trabalhar com o flexbox de maneira geral.

No caso do nosso exemplo, o pai é a div class="container", então ele será estilizado com o display: flex.

*O valor padrão para o flex grow é 0, então, caso não seja atribuído um valor, por padrão ele será zero.*

Para podermos visualizar melhor como funciona o grow, vamos alterar o html, atribuindo um nome de classe diferente e atribuindo no css um valor para cada uma das 3 divs filhas, ficando dessa forma:

![image-20241220140227551](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241220140227551.png)

​	![image-20241220135733803](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241220135733803.png)	<img src="C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241220135651690.png" alt="image-20241220135651690" style="zoom:67%;" />

O conteúdo da terceira div tomou mais espaço pois possui valor 3, que é o maior.

Se tiver um conteúdo maior dentro de um elemento html com grow aplicado, por mais que o valor do flex-grow seja menor do que os outros elementos irmãos, ele vai aumentar de tamanho, porque o conteúdo dentro dele é maior, então é normal que isso aconteça. 

Por exemplo, se adicionar um conteúdo de texto no grow-2, ainda que o valor 3 seja maior, o item 2 que ocupará maior espaço dentro do container. Pois o conteúdo é maior.

![image-20241220140626752](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241220140626752.png)

![image-20241220140639200](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241220140639200.png)

Se todos tiverem o mesmo peso, por exemplo as divs (flex items) 1, 2, 3 tem o grow de 2 (ou 1), o espaço ocupado dentro do container será igual entre elas.

​	![image-20241220140832167](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241220140832167.png)	<img src="C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241220140842284.png" alt="image-20241220140842284" style="zoom:67%;" />



**Basis**

Define o tamanho inicial de um item flexível antes de o espaço disponível ser distribuído entre os itens. Serve para especificar o tamanho base de um item (largura ou altura, dependendo do eixo principal) no container **flex**.

- **Alto nível semântico**: melhora a legibilidade do código ao definir tamanhos base claros e evita o uso excessivo de valores fixos como width ou height.

Utilizado quando for necessário determinar o tamanho inicial de um item em layouts flexíveis, antes de aplicar crescimento ou encolhimento (flex-grow e flex-shrink). Também é útil para criar layouts proporcionais ou com tamanhos iniciais consistentes.

Estrutura do html usado em aula como exemplo:

<img src="C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241220142410661.png" alt="image-20241220142410661" style="zoom:67%;" />

Acima, dentro do head, foi dado um link para duas páginas css, globals e style.

O css globals está com algumas estilizações globais feitas e o style também possui algumas propriedades já definidas na aula anterior:

​				<img src="C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241220142427762.png" alt="image-20241220142427762" style="zoom:67%;" />			![image-20241220142825910](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241220142825910.png)

Antes, tínhamos visto que a propriedade flex-grow permitia que os itens crescessem conforme o valor que nós definíamos e que, mesmo que tivessem o mesmo valor de tamanho, caso o conteúdo dentro de um deles fosse maior ele mesmo assim cresceria para que o conteúdo coubesse.

A propriedade flex-basis **vai permitir que os itens de um container flex tenham sempre o mesmo tamanho**, independente do conteúdo dentro deles, então, mesmo que o conteúdo seja maior, ele vai respeitar o valor que colocarmos no css flex-basis.

O flex-basis não possui valores mínimos ou máximos predefinidos, como acontece com o flex-grow. Ele aceita qualquer valor válido de tamanho em CSS, como unidades absolutas, relativas e auto.



**Auto**

É o valor padrão do flex-basis. Levando em conta que os itens do html estão com grow-1, ao colocar o basis auto, podemos observar que o comportamento é igual ao da aula anterior, ainda que todos tenham peso 1, a terceira div se expande, pois o conteúdo dentro é maior.

​		![image-20241220143051627](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241220143051627.png)		<img src="C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241220143125537.png" alt="image-20241220143125537" style="zoom:67%;" />



**Flex-basis + unidade relativa/absoluta**

Define que todos os itens tenham o mesmo tamanho, independente do conteúdo dentro deles. Se colocarmos os tamanhos de basis, por exemplo, em ordem crescente, sendo menor na div com mais conteúdo e maior na div com menos, podemos ver que, mesmo estando com mais conteúdo, a div respeita a delimitação do basis.

<img src="C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241220150755400.png" alt="image-20241220150755400" style="zoom: 80%;" />	<img src="C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241220150812445.png" alt="image-20241220150812445" style="zoom:80%;" />

![image-20241220150901472](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241220150901472.png)



É importante saber que, caso a palavra dentro do item seja muito grande e não seja uma palavra válida, o html não vai reconhecê-la, dessa forma o item não fará a quebra de linha e irá ultrapassar o limite de largura container.

![image-20241220151450944](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241220151450944.png)



**Shrink**

A tradução é: encolher. É uma propriedade usada para determinar **quanto um item deve encolher** em relação aos outros, caso o espaço disponível no contêiner seja menor que o necessário para acomodar todos os itens. Ela é o oposto da propriedade flex-grow.

**Como funciona?**

- **Valor padrão:** 1 (o item pode encolher quando necessário).
- Valores possíveis:
  - **0:** O item **não encolhe**, mesmo que falte espaço no contêiner.
  - **Números positivos:** Quanto maior o número, **mais o item encolhe** em relação aos outros.

**Fórmula simplificada:**
Se o espaço no contêiner for insuficiente, o navegador calcula a proporção de redução com base no valor do flex-shrink de cada item.

Usado para evitar que itens importantes encolham em layouts responsivos (use flex-shrink: 0) e para criar proporções específicas de redução entre elementos.



Estrutura do HTML usada em aula como exemplo:

<img src="C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241227165656765.png" alt="image-20241227165656765" style="zoom:80%;" />

Acima, dentro do head, foi dado um link para duas páginas css, globals e style.

O css globals está com algumas estilizações globais feitas e o style também possui algumas propriedades já definidas na aula anterior:

​			<img src="C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241227163754867.png" alt="image-20241227163754867" style="zoom:80%;" />				![image-20241227164318530](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241227164318530.png)



De início, como todos os conteúdos tem o mesmo tamanho (exatamente o mesmo texto no html), e o shrink foi definido como 1, então todos permanecerão iguais (nada vai acontecer), pois essa definição faz com que o conteúdo não extrapole o tamanho para caber dentro do container, ou seja, está dividindo o espaço deles entre as divs irmãos.

​	![image-20241227170016179](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241227170016179.png)		<img src="C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241227170036390.png" alt="image-20241227170036390" style="zoom:80%;" />



Porém, colocando o valor **zero** (e aumentando o tamanho do texto no html), ele não permite que o item reduza de tamanho para dividir o espaço dele dentro do container, então ele acaba expandindo, de acordo  com o conteúdo, e jogando todos os outros itens para fora.

​	<img src="C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241227171059556.png" alt="image-20241227171059556" style="zoom:67%;" />	![image-20241227171115735](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241227171115735.png)

<img src="C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241227171133815.png" alt="image-20241227171133815" style="zoom:67%;" />



**Quanto maior o valor do shrink, maior será a capacidade do item encolher de tamanho.**

![image-20241227171523956](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241227171523956.png)	<img src="C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241227171536625.png" alt="image-20241227171536625" style="zoom:80%;" />

![image-20241227171559166](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241227171559166.png)

O que tem a classe shrink 1 vai encolher **menos** e o que tem a classe shrink 3 vai encolher **mais**.



**Flex**

É um atalho que combina **flex-grow**, **flex-shrink** e **flex-basis**, permitindo controlar o comportamento de crescimento, encolhimento e tamanho inicial de um item dentro de um contêiner Flexbox.

Usado para layouts responsivos e proporcionais e controlar o comportamento de itens flexíveis em layouts dinâmicos.

**Dica prática**: use **flex** para economizar código em vez de configurar flex-grow, flex-shrink e flex-basis separadamente. 



Estrutura do HTML utilizada em aula como exemplo:

<img src="C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241227173146403.png" alt="image-20241227173146403" style="zoom: 80%;" />

Acima, dentro do head, foi dado um link para duas páginas css, globals e style.

O css globals está com algumas estilizações globais feitas e o style também possui algumas propriedades já definidas na aula anterior:

​				<img src="C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241227173210080.png" alt="image-20241227173210080" style="zoom: 67%;" />			![image-20241227173217983](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241227173217983.png)



Ao definir uma propriedade flex no css e atribuir os valores, eles serão, respectivamente, flex-grow, flex-shrink e flex-basis.

​	   ![image-20241227173554656](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241227173554656.png)	<img src="C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241227174039907.png" alt="image-20241227174039907" style="zoom:80%;" />

Nesse caso o grow = 0, shrink = 1 e basis = 150px. Caso queira especificar apenas a primeira propriedade, ela será referente ao grow e os outros dois valores serão reconhecidos como padrão (no caso do shrink o valor padrão é 1 e o valor padrão do basis é 0).

**O flex: 1 (que abrange apenas o grow) é uma das formas mais utilizadas nos projetos.**



**Order**

Define a ordem em que os itens aparecem dentro de um contêiner Flexbox, independentemente de sua posição no HTML.

Por padrão, todos os itens têm **order: 0** (de cima para baixo, de importância). Podemos atribuir um valor inteiro (positivo, negativo ou zero) para alterar a ordem dos itens:

- Menores valores aparecem primeiro.
- Maiores valores aparecem depois.

Usado para reordenar visualmente itens sem modificar o HTML e em layouts dinâmicos, como mudanças em diferentes breakpoints de design responsivo.

**Dica prática**: Evite abusar de **order**, pois pode prejudicar a acessibilidade e dificultar a compreensão do código. Use com moderação em casos específicos.



Estrutura do HTML utilizada em aula como exemplo:

<img src="C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241227174955084.png" alt="image-20241227174955084" style="zoom:80%;" />

Acima, dentro do head, foi dado um link para duas páginas css, globals e style.

O css globals está com algumas estilizações globais feitas e o style também possui algumas propriedades já definidas na aula anterior:

​			<img src="C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241227175119211.png" alt="image-20241227175119211" style="zoom:80%;" />		![image-20241227175228605](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241227175228605.png)*valor 1 no grow*



Com a propriedade order podemos modificar a ordem dos elementos html filhos de um container. Caso queira, por exemplo, que o terceiro item fique na última posição, no lugar do quinto elemento, para isso, basta que passemos qualquer valor maior que zero (podendo ser qualquer número inteiro para representar a posição onde aquele elemento ficará).

​	  ![image-20241227180148383](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241227180148383.png)			<img src="C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241227180320666.png" alt="image-20241227180320666" style="zoom:80%;" />

<img src="C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241227180210116.png" alt="image-20241227180210116" style="zoom:80%;" />

Se um elemento possuir um valor maior, então ele ficará mais para a direita, e quanto menor o valor, mais para a esquerda ele vai ficar.

Seguindo o exemplo, o 4 é o maior valor (mais a direita) e o 0 o menor (mais a esquerda). Dessa forma, o bloco 2, que recebeu o valor 4, ficou mais a direita de todos, pois é o número maior e o bloco 4, que recebeu o valor 0, ficou mais a esquerda de todos, pois é o número menor.



Se, por exemplo, for aplicado um flex-direction: row-reverse no container pai, então ele irá inverter a ordem, deixando o elemento que possui o maior valor mais para a esquerda e os elementos que possuem menor valor, vão ficar para a direita.

​	<img src="C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241227181109232.png" alt="image-20241227181109232" style="zoom:80%;" />		<img src="C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241227181126505.png" alt="image-20241227181126505" style="zoom: 67%;" />



No caso de dois elementos possuindo o mesmo valor de order, a leitura será feita pelo que vem primeiro e depois os seguintes. Por exemplo, se a div 2 e 3 possuírem o mesmo valor de order, o elemento que ficará mais para a direita será o elemento que vem depois na sequência do html.

​	![image-20241227181515894](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241227181515894.png)	<img src="C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241227181542148.png" alt="image-20241227181542148" style="zoom:67%;" />



**A mudança de ordem dos elementos ocorre apenas no navegador (visual), não no HTML (código, texto).**



**Align Self**

Seria algo como "alinhar a si próprio". Permite alinhar um único item dentro de um contêiner ao longo do eixo transversal (vertical, por padrão), **sobrescrevendo o align-items definido no contêiner**.

Define o alinhamento de **um único item**, enquanto align-items afeta todos os itens do contêiner. Os valores possíveis são os mesmos do align-items: auto (valor padrão do align-self); flex-start; flex-end; center; stretch.

Usado quando precisamos de **exceções** no alinhamento de um ou poucos itens, sem modificar o comportamento geral do contêiner. Exemplo: Destacar um botão ou elemento em um layout.



Estrutura do HTML utilizada em aula como exemplo:

<img src="C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241227191355539.png" alt="image-20241227191355539" style="zoom:67%;" />

**RESSALTANDO QUE APENAS O PRIMEIRO FLEX ITEM DO CONTAINER ESTÁ COM A CLASSE APLICADA, OS DEMAIS ITENS (2 E 3) ESTÃO SEM PROPRIEDADE.**

Acima, dentro do head, foi dado um link para duas páginas css, globals e style.

O css globals está com algumas estilizações globais feitas e o style também possui algumas propriedades já definidas na aula anterior (porém foi acrescentada uma largura e altura no container div):

​		<img src="C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241227191421956.png" alt="image-20241227191421956" style="zoom:80%;" />			![](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241227191811409.png)



**Auto**

Por ser o valor padrão, nada irá acontecer quando a propriedade for auto (e o flex-direction for row). 

Usado quando não há necessidade de personalizar o alinhamento de um item específico.

​		![image-20241227191859715](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241227191859715.png)	  <img src="C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241227191911351.png" alt="image-20241227191911351" style="zoom:67%;" />

Caso o flex-direction seja alterado para column, então o eixo transversal passa a ser na horizontal.

​		![image-20241227192748963](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241227192748963.png)		<img src="C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241227192802396.png" alt="image-20241227192802396" style="zoom: 67%;" />



**Flex-start**

Como o flex-direction está como row, por padrão, ou seja, o eixo transversal está na vertical, isso faz com que o flex-start alinhe o item no topo e ao longo do eixo vertical.

Usado para posicionar um item no topo, como um cabeçalho ou um botão destacado.

​	![image-20241227192002205](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241227192002205.png)	<img src="C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241227192014217.png" alt="image-20241227192014217" style="zoom:67%;" />

Caso o flex-direction seja alterado para column, o resultado será exatamente igual ao visto na propriedade auto.



**Flex-end**

Vai alinhar o item no final do eixo transversal (vertical, pois o flex-direction está como row). Lembrando que, apenas o primeiro item está com classe, então podemos observar que ele fica lá em baixo e o restante das divs ficam no topo.

Usado para alinhar um item na parte inferior, como um rodapé ou um rótulo no canto.

​	![image-20241227192055087](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241227192055087.png)		<img src="C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241227193208094.png" alt="image-20241227193208094" style="zoom:67%;" />

Se alterarmos o flex-direction pra column, o eixo transversal passa a se mover na horizontal, alinhando o item no final da horizontal.

​	![image-20241227194009795](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241227194009795.png)		<img src="C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241227194022688.png" alt="image-20241227194022688" style="zoom:67%;" />



**Center**

Vai alinhar o item ao centro do eixo transversal (vertical, pois o flex-direction está como row). O center é um dos valores mais usado, mas a propriedade do align-self: center, nem tanto.

Usado para chamar atenção para um elemento centralizado, como um título ou botão.

​	![image-20241227194130934](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241227194130934.png)		<img src="C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241227194140460.png" alt="image-20241227194140460" style="zoom:67%;" />

Se trocarmos o flex-direction para column, então o eixo transversal passa a ser na horizontal e ele fica alinhado ao centro e na horizontal.

​	![image-20241227194421769](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241227194421769.png)		<img src="C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241227194432330.png" alt="image-20241227194432330" style="zoom:67%;" />



**Stretch**

É algo como "esticar" ou "alongar". Stretch é o valor padrão do align items, então, mesmo aplicando a classe apenas na primeira div, todas as outras vão esticar também. 

Usado para manter itens dimensionados uniformemente, como caixas em um layout.

Para poder visualizar precisamos fazer duas pequenas mudanças:

- No globals estamos aplicando uma largura e uma altura para as divs, mas o stretch funciona apenas quando não definimos uma largura ou altura fixa pro elemento, então esse valor deverá ser retirado;
- Aplicar no align-items (em .container) a propriedade de flex-start (pois o padrão dele é stretch);

​		![image-20241227195054788](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241227195054788.png)		![image-20241227195102673](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241227195102673.png)

Agora sim, será possível visualizar. Lembrando que a linha transversal está na vertical, pois o flex-direction está row, por padrão.

<img src="C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241227195235413.png" alt="image-20241227195235413" style="zoom:67%;" />

Assim como os outros, caso o flex-direction seja alterado para column, o eixo transversal passará a ser na horizontal.

​	![image-20241227195331306](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241227195331306.png)	<img src="C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241227195342167.png" alt="image-20241227195342167" style="zoom:67%;" />



**Dicas finais *(diferenças entre justify-content, align-items, align-content e align-self)***

**Justify-content vs. Align-items**

São semelhantes, pois compartilham alguns comportamentos. Mas a principal diferença é que o justify-content atua ao longo do eixo **principal** e o align-items atua ao longo do eixo **transversal**. 

E, além disso, os valores disponíveis em cada uma dessas propriedades são um pouco diferentes

- No justify-content possui valores como space-between, space-around e space-evenly, que o align-items não tem.
- O align-items, por outro lado, tem o valor stretch, que não existe no justify-content.

Apesar dessas diferenças, ambos possuem as propriedades de flex-start, flex-end e center.



**Align-items vs. Align-content vs. Align-self**

Essas são as comparações que mais causam dúvidas, isso, principalmente, por conta dos nomes parecidos, e porque elas atuam no eixo transversal.



**Align-items**

O align-items alinha todos os itens, dentro de um container e em uma única linha no eixo transversal. Todos itens na mesma linha seguirão o mesmo alinhamento. Por exemplo, se aplicarmos o align-items: center, todos os itens serão alinhados ao longo do eixo transversal e no centro.



Para visualizar na prática:

​	<img src="C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241227202637999.png" alt="image-20241227202637999" style="zoom: 80%;" />	![image-20241227202901612](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241227202901612.png)



No primeiro exemplo, utilizando o align-items: center, é possível visualizar que todos os itens ficam alinhados na mesma linha e centralizados (na vertical).

<img src="C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241227204640209.png" alt="image-20241227204640209" style="zoom:67%;" />

Vamos utilizá-lo quando precisarmos alinhar itens em uma única linha e em layouts flexbox, controlando como os elementos filhos serão posicionados verticalmente.



**Align-content**

A diferença para o align-content é que ele só faz diferença (só é aplicado e visto visualmente), se o container tiver múltiplas linhas de itens, ou seja, ele não está preocupado com os itens individuais (linhas únicas), mas sim com o espaçamento entre as linhas desses itens, por isso, só é possível usar o align-content quando temos o flex-wrap (no container pai) também definido.

​		![image-20241227204008370](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241227204008370.png)		<img src="C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241227204023587.png" alt="image-20241227204023587" style="zoom:67%;" />

Dessa forma, há a quebra de linha dos itens e eles ficam centralizados no container, sem disputar espaço.



**Align-self**

Já o align-self atua ao longo do eixo transversal, mas a diferença é que ele é um flex-item, então a propriedade deve ser aplicada diretamente no item (filho), não no container (pai).

Essa propriedade vai permitir que um item individual tenha um alinhamento diferente do dos outros, o que não acontece no align-items e no align-content (onde todos os itens sempre terão o mesmo alinhamento, pois são flex container).

<img src="C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241227204827792.png" alt="image-20241227204827792" style="zoom:67%;" />

Ela não é muito utilizada no dia a dia, geralmente vamos acabar utilizando bem mais os outros dois anteriores.



**DICA PARA LIDAR COM PROBLEMAS EM HTML COMPLEXOS**

Geralmente existe uma grande dificuldade quando precisamos aplicar o flexbox na prática, em projetos mais complexos. Em html's mais complexos, com mais níveis de elementos, mais divs, por exemplo.

Uma forma bem fácil de pensar em como resolver qualquer problema ou dúvida com flexbox:

Sempre devemos ver primeiro quem é o pai direto dos elementos que queremos posicionar. Geralmente vamos querer posicionar os elementos filhos de um pai (de uma só vez), e, na maioria das vezes, ao centro.

Podemos ir diretamente ao arquivo index.html do arquivo e procurar quais são as divs pais e filhas, ou também podemos dar um inspecionar na página.



1. **Identifique o Pai e os Filhos**:

   - Determine quem é o container pai e quem são os itens filhos.

   - Exemplo: 

     <img src="C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241227210513404.png" alt="image-20241227210513404" style="zoom: 67%;" />

     

2. **Defina o Comportamento**:

   - Use **Justify Content** para alinhar no eixo principal.
   - Use **Align Items** ou **Align Content** para alinhar no eixo transversal.

   

3. **Inspecione o Elemento**:

   - Utilize o inspetor do navegador para verificar o pai e os filhos.

     

4. **Centralização**:

   - Para centralizar:

     

<img src="C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241227210749002.png" alt="image-20241227210749002" style="zoom:67%;" />

Lembre-se: Flexbox é poderoso, mas requer prática. Revise os conceitos, experimente diferentes valores e inspecione seus elementos no navegador para entender melhor.



**Figma**

É uma ferramenta de design baseada na nuvem utilizada para criar protótipos, interfaces de usuário (UI), layouts de sites e aplicativos. Ele permite o trabalho colaborativo em tempo real, onde designers, desenvolvedores e equipes podem criar, revisar e compartilhar projetos de forma integrada.

[Acessar site Figma](https://www.figma.com/)



**Principais usos do Figma:**

1. **Design de Interfaces:** Criação de layouts para aplicativos, sites e sistemas.
2. **Prototipagem:** Simulação de navegação e interações para testar funcionalidades.
3. **Colaboração em Equipe:** Permite que várias pessoas trabalhem no mesmo arquivo simultaneamente.
4. **Entrega para Desenvolvimento:** Facilita a comunicação entre designers e desenvolvedores, mostrando dimensões, cores e outros detalhes técnicos.



**Atalhos de teclado mais utilizados no Figma:**

1. **Seleção e Navegação:**

   Selecionar ferramenta de Seleção: V
   Ferramenta de Mão (para mover a tela): H
   Zoom In: Ctrl + +
   Zoom Out: Ctrl + -
   Ajustar tela (fit to screen): Shift + 1
   Ir para o modo de visualização: Ctrl + Shift + P

   

2. **Ferramentas de Desenho e Forma:**

   Retângulo: R
   Elipse: O
   Linha: L
   Caneta: P
   Texto: T
   Quadro (Frame): F

   

3. **Ações de Edição:**

   Desfazer: Ctrl + Z
   Refazer: Ctrl + Shift + Z
   Copiar: Ctrl + C
   Colar: Ctrl + V
   Cortar: Ctrl + X
   Excluir: Delete
   Agrupar: Ctrl + G
   Desagrupar: Shift + Ctrl + G

   

4. **Transformações e Alinhamento:**

   Alinhar à esquerda: Alt + Shift + L
   Alinhar ao centro horizontal: Alt + Shift + C
   Alinhar à direita: Alt + Shift + R
   Alinhar ao topo: Alt + Shift + T
   Alinhar ao centro vertical: Alt + Shift + M
   Alinhar à base: Alt + Shift + B

   

5. **Camadas e Objetos:**

   Selecionar a camada superior: Ctrl + ]
   Selecionar a camada inferior: Ctrl + [
   Bloquear camada: Ctrl + Shift + L
   Desbloquear camada: Ctrl + Shift + Alt + L

   

6. **Prototipagem e Animação:**

   Entrar no modo de protótipo: Shift + P
   Ir para a tela anterior (prototipagem): Ctrl + Shift + ←
   Ir para a tela seguinte (prototipagem): Ctrl + Shift + →



