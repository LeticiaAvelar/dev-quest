# CSS3 (Básico) :book:

:link: ​Notion: https://glowing-scilla-18d.notion.site/CSS3-B-sico-121bf6c7b63d80f189a0cc92cbc2cdd2?pvs=4



É a sigla para "cascading style sheet" ou FOLHAS DE ESTILO EM CASCATA.

A estilização respeita uma ordem de menor pra maior importância, por isso o "cascata" no nome.

Resumindo, o CSS deixa o HTML mais bonito.



Existem três principals formas de estilização no CSS, sendo elas inline, interna e externa. Dentre as três, a mais recomendada é a EXTERNA.



**CSS Inline:** (não é uma abordagem boa, pois repete demais e o código não fica limpo)

A forma mais simples de colocar um estilo no CSS seria colocando um atributo "STYLE" dentro da tag e a estrutura dele é a "propriedade: valor"

Exemplo, um cliente pediu para colocar um fundo azul, então ficaria:

![image-20241022180043319](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241022180043319.png)

Sempre que quiser colocar alguma propriedade no style, a alteração deve ser feita depois de um ponto e vírgula, exemplo:

![image-20241022180259346](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241022180259346.png)



**CSS Interno:**

Nos dá a chance de estilizar várias tags ao mesmo tempo e fazer isso dentro da página HTML do windows.

Utilizando a tag "STYLE" (dentro da tag head) vc indica o que quer estilizar (style + a tag que quer estilizar + { o que será modificado }), exemplo:

![image-20241022182426732](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241022182426732.png)

A tag STYLE apresenta limitações, pois quando é necessários fazer manutenção de mais páginas (exemplo, tem 20 páginas de html e o cliente quer mudar o site todo), a tag fica responsável somente por aquela página, fazendo com que, dessa forma, seja necessário alterar manualmente as 20 páginas.



**CSS Externo:**

Serve para refatorar o código. O externo permite incorporar regras de CSS presentes em um documento à parte a outro arquivo HTML, em que ficam os elementos da página.

Utilizando a tag "LINK" (link:css), que é automaticamente completado por "*rel*="stylesheet" *href*="style.css", sendo que REL quer dizer que o relacionamento dos links é um style sheet e HREF é qual o nome desse arquivo. Exemplo:

![image-20241022183602628](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241022183602628.png)

Nesse caso, a folha "style.css" não existe ainda, então ela deve ser criada. Ao passar com o mouse por cima, o próprio sistema já dá a opção de seguir para style.css

![image-20241022183800995](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241022183800995.png)

Como o arquivo não existe, aparecerá uma mensagem de erro, avisando que o arquivo não foi encontrado, mas basta clicar em "Criar Arquivo". Observa-se que ele já será criado no formato correto (.css).

Arquivos .css não entendem o conceito de tag, eles são seletores. Então quando for criar o corpo de um arquivo CSS, não se coloca tags (style, por exemplo), apenas as propriedades.

![image-20241022184204452](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241022184204452.png)

Para seguir o mesmo padrão em várias folhas de HTML, basta que a tag link de styles esteja nelas (e dentro do head), assim, qualquer alteração feita na folha de CSS será automaticamente reconhecida nas folhas de html, não sendo necessário fazer alterações manualmente uma a uma. Isso ajuda muito no desenvolvimento e manutenção da página, tanto seu, quanto de qualquer outra pessoa.



**Chrome DevTools**

Já vem instalado por padrão no navegar chrome. Apertando F12 abrirá uma tela lateral (ou dar um clique com o botão direito do mouse e clicar em "Inspecionar").

Ela já vem aberta na parte "Elements/Elementos", onde mostra a estrutura do html e, ao clicar no ícone da setinha no canto superior esquerdo (ou ctrl + shift + c), é possível selecionar um elemento da página para inspecionar e ver mais detalhes sobre.

![image-20241023093136909](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241023093136909.png)

É possível fazer isso em alguns sites que queira testar como ficaria com uma cor X, por exemplo. Também é útil para olhar onde está o erro na sua página.



**Cores em CSS**

Existem 4 formas de representar cores no CSS, sendo ela:

1. As cores “chapadas”,  apenas com o nome da cor;

   ![image-20241023094837670](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241023094837670.png)

2. Usando RGB (red, green e blue);

   ![image-20241023094857965](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241023094857965.png)

3. Usando RGBA (red, green, blue e uma opacidade);

   ![image-20241023094916613](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241023094916613.png)

4. E por hexadecimal, onde 0 é a menor cor e a maior será F, conforme essa ordem: 0 1 2 3 4 5 6 7 8 9 A B C D E F 

   ![image-20241023140118994](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241023140118994.png)

OBS.: as cores RGB's são classificadas de 0 até 255 e a opacidade varia entre 0 (que é totalmente transparente) e 1 (onde fica totalmente sólido).

OBS².: o decimal é uma escala de números que variam de 0 a 9 (0, 1, 2, 3, 4, 5, 6, 7, 8, 9), já o **HEXA**decimal (que vem de seis) é uma escala que varia em 16 algarismos (0, 1, 2, 3, 4, 5, 6, 7, 8, 9, A, B, C, D, E, F), sendo o zero o **MENOR** valor, e o f o **MAIOR** valor. Cada casa é separada como se fosse uma letra do RGB, exemplo: "#00*(R)*00*(G)*00*(B)*"

![image-20241023140055779](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241023140055779.png)

#000000 = 100% preto

#ffffff = 100% branco



**Também é possível fazer alterações utilizando HSL e HSLA**

**HSL** é mais simples para criar variações de cores.

**H**: representa a matiz, a cor específica em si, variando de 0 a 360 graus, sendo 0 = vermelho, 120 = verde, 240 = azul, 360 = vermelho

**S**: representa saturação/intensidade da cor, variando de 0 a 100%, sendo 0% = cinza (sem cor) e 100% = cor total

**L**: representa a quantidade de luz/luminosidade na cor, seria a iluminação da cor, variando de 0 a 100%, sendo 0% = preta e 100% = branca

![image-20241023140549779](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241023140549779.png)

No **HSLA**, cada letra tem o mesmo significado anterior *(matiz, saturação, luminosidade)*, porém o "**A**" significa alpha, que é a TRANSPARÊNCIA/opacidade da cor, variando de 0 a 1, sendo 0 o máximo de transparência e 1 sólida.

![image-20241023141105467](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241023141105467.png)



**Espaçamento externo com margin:**

O "**MARGIN**" serve para dar espaçamento ENTRE elementos html.

![image-20241023143546085](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241023143546085.png)

Caso todos os valores para espaçamento sejam iguais, pode-se usar apenas "margin: __px".

![image-20241023144912076](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241023144912076.png)

Caso os valores sejam diferentes em todos os lados, é necessário fazer a inclusão de um atributo para cada lado

![image-20241023144829996](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241023144829996.png)

Caso queira um valor igual nos lados paralelos, pode-se usar o "margin: \__px \_px" (1° valor corresponde ao topo e base e o segundo valor às laterais esquerda e direta)

![image-20241023144951684](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241023144951684.png)

Também é possível fazer a alteração de cada uma das laterais com o margin, utilizando a mesma linha (lembrando que ele segue um sentido horário, ou seja, topo, lateral direita, base, lateral esquerda).

![image-20241023145342613](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241023145342613.png)

**LEMBRE-SE**: se o código ficar repetindo demais, é porque tem alguma coisa errada. Nesse caso, se as laterais forem iguais em cima e em baixo, por exemplo, não há necessidade de usar um código extenso configurando o tamanho de pixels de cada um. Seja prática, dê preferência para escrever o código na versão shot hand/encurtada.



**Espaçamento interno com padding:**

O "**PADDING**" serve para dar espaçamento DENTRO dos elementos html

Basicamente funciona da mesma forma que o margin (em questão de estrutura do código). O padding é utilizando quando você quer dar um espaçamento entre o conteúdo (o que tem dentro) e as bordas.

![image-20241023151219741](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241023151219741.png)



**Adicionando bordas aos elementos com border:**

Assim como o próprio nome já diz, o atributo aplica uma borda ao elemento. Utilizando a propriedade "border: __". Em 90% dos casos, o tipo de borda será "solid", ou seja "border: solid + px".

Adicionando a propriedade "width" no border, é possível definir as larguras das bordas (tanto uma a uma, quanto no geral).

Utilizando "border-color" é possível alterar a cor da borda.

![image-20241023152411491](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241023152411491.png)

Porém essa não é a forma mais limpa de configurar as bordas. Dando preferência aos códigos de uma linha só e **lembrando de respeitar a ordem de hierarquia**.

![image-20241023153201098](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241023153201098.png)

Assim como no margin, também é possível fazer a menção de cada lateral e designar uma cor separadamente

![image-20241023152632766](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241023152632766.png)

Porém, essa também não é a forma mais limpa de se fazer, dando preferência novamente a utilizar apenas um código e linha

![image-20241023152845414](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241023152845414.png)



**Modelos de caixa:**

É um dos conceitos mais importantes do html, possibilitando ver onde o margin, paddin e border trabalham juntos.

Para resetar os valores padrões que o navegador coloca de margin, padding, border, é possível utilizar a regra "\*", que serve para dizer que vai afetar todos os elementos que estão na tela, por exemplo:

![image-20241023160040179](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241023160040179.png)

Lembrando que, para que o reset seja válido para todos os elementos, o asterisco precisa vir no topo do corpo do CSS.

![image-20241023160611088](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241023160611088.png)

Podemos utilizar o inspecionar do navegador sempre que houver alguma dúvida sobre as bordas, ficando melhor para visualizar.

![image-20241023160552109](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241023160552109.png)

O modelo de caixa é constituído por alguns elementos, sendo eles o conteúdo, padding, border e margin.



**Tipos de Caixas**

Elementos do tipo "block level" automaticamente têm uma quebra de linha (fica um bloco ocupando a largura total da tela e um embaixo do outro). 

Por exemplo, h1 por padrão já é um display block, então estilizá-lo com "display: block" não faria diferença. Mas, se trocar os displays para "inline", por exemplo, ficaria tudo na mesma linha, alterando a configuração padrão do navegador.

![image-20241023165829716](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241023165829716.png)

Um texto no estilo "block" tem a quebra de linha automática e ocupa a largura total.

![image-20241023170245510](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241023170245510.png)

Elementos do tipo **block**: divs, h1, parágrafos...

Elementos do tipo **inline**: span, a (âncoras)...



**IDs ou Identificadores**

IDs são únicos por página, ou seja, se vc estiver montando uma página e tiver um produto com id "descricao", nenhum outro produto poderá utilizar esse ID, pois não é válido *(não poderia ter dois ids chamados "id="descricao"" na página, por exemplo)*.

![image-20241024124405692](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241024124405692.png)

Para estilizar no CSS um elemento que seja ID no html, é preciso que inicie com uma "#" *(exemplo: #descricao{})*. Caso haja mais de um elemento para fazer alteração, é possível fazer tudo na mesma linha, basta colocar uma vírgula + *#elemento*.

![image-20241024124446699](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241024124446699.png)

Porém, essa **NÃO** é a forma mais limpa e fácil de fazer. Para estilizar vários elementos ao mesmo tempo *(se o estilo for o mesmo)* é melhor utilizar as **classes**.



**Classes: adicionando estilos em múltiplos elementos**

Tudo que tiver um ponto "." na frente o CSS vai entender que é uma classe. Então, da mesma forma que fez com os IDs *(utilizando #)*, agora com class ficará ".descricao-pc, .descricao-videogame", MAS, para que fique mais fácil para manutenção e menos verboso, a maneira correta seria trocando as classes para um nome ÚNICO e genérico, por exemplo "class=descricao-produto".

![image-20241024130106882](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241024130106882.png)

![image-20241024130449956](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241024130449956.png)

Dessa forma, se, por exemplo, tiverem vários produtos na página que precisem ser estilizados para o fundo laranja, como o valor de class é genérico, pode-se usar esse único estilo para outros elementos/produtos.

É possível colocar mais de uma classe dentro de um elemento html *(o que não é possível fazer dentro de um id)*. 

Lembre-se da importância de criar uma classe/id que seja um nome mais **geral** e não estilos específicos *(como: "borda verde", "texto grande", "botão azul")*, pois assim fica objetivo e contextualizado. Por exemplo, se um item em promoção precisa ter a aparência de uma borda verde, é melhor criar uma classe com o nome "promocao" do que "borda-verde", pois, se amanhã o cliente pedir para trocar a cor da borda para azul, o seu botão não se torna "inútil/difícil de entender" e a manutenção é rápida, não sendo necessário trocar cada classe "borda-verde" para "borda-azul" ou "promocao".

![image-20241024132312210](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241024132312210.png)

![image-20241024132325372](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241024132325372.png)



**Divs e Span**

As **divs** são divisões de um espaço na página, geralmente utilizados para agrupar elementos do HTML em um bloco. Elas possuem um "display: block" do tipo block level por padrão.

Sempre que fizer uma *div* é importante classificar ela com um nome **contextualizado**, como por exemplo: div class="produto". Não é indicado estilizar no CSS o atributo "*div*", pois, como ele é muito comum, ao fazer alterações no estilo de *div's* num geral, todas serão afetadas e não apenas aquela específica que você queria.

​		![image-20241024152557682](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241024152557682.png) 		![image-20241024152612110](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241024152612110.png)

Existe um macete no vs code (emmet) para criar divs com classe, quando for digitar coloca "div.*nomedaclasse*" e assim ela já vem pronta.

![image-20241024160322050](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241024160322050.png)

![image-20241024160341717](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241024160341717.png)

O **span** é uma tag *inline level (não quebram linha)* que geralmente é utilizada para modificar/destacar uma palavra sem interferir com o estilo do elemento pai *(que o engloba)*, ou seja, você pode criar uma tag span no meio de uma frase e alterar apenas aquilo em específico, sem atrapalhar outras modificações de classe e tags de maior importância.

![image-20241024154857154](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241024154857154.png)![image-20241024154911357](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241024154911357.png)![image-20241024155530174](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241024155530174.png)

Também é possivel criar uma classe dentro de span, para que consiga estilizar valores específicos, por exemplo span class="destaque", **PORÉM**, fazendo da forma anterior o código no html fica mais limpo e o css faz a leitura normalmente.



**Unidades de medidas relativas**

- **Unidade "%"**

Primeiramente, é importante entender o conceito de pai e filho no corpo do html/css. Sempre que for estilizar algo, lembrando que a leitura é feita de cima para baixo *(exceto em casos em que há comando específico)* o html tem o maior valor, seguido do head, body e assim por diante. Por exemplo:

![image-20241024175936250](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241024175936250.png)

![image-20241024175952586](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241024175952586.png)

Como foi imposta uma largura no "body" de 50%, então todas as divs abaixo *(.pai e .filha)* serão configuradas para ir de acordo com body, ocupando a largura que setar no **pai de todos**, que nesse caso é o body *(seguindo a hierarquia)*.

Seguindo essa lógica, entende-se que, a "*div classe .filha*" tem a "*div classe .pai*" como pai, **MAS** a "*div classe .pai*" tem como pai a "*div body*".

Fazendo alterações na *div .pai*, como colocando largura de 50%, por exemplo, percebe-se que ela configura na delimitação imposta, mas, como a *div body* é mais importante, a *div .pai* preenche o espaço dos 50% de largura e a *div body* preenche os outros 50% *(levando em conta a proporção do pai de todos, totalizando 100%. 50% body e 50% .pai)*.

Da mesma forma, ao colocar uma largura de 50% na *div .filha*, ela ocupará 50% do espaço da *div .pai*, formando assim esse efeito de cascata, que é o conceito que consideramos **pai e filho**.

​							![image-20241024184149132](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241024184149132.png) 

![image-20241024181911641](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241024181911641.png)

*É como se o body fosse 100%, .pai fosse 50% e .filha fosse 25%*.

Unidade relativa é justamente porque será relativo ao que ele está dentro, ao tamanho de uma tela etc, não é uma medida absoluta ou fixa.

- **Unidade "EM"**

É uma unidade de medida tipográfica. 1 em = 16 pixels, por padrão o html já tem um font size de 16px *(pixel é uma unidade absoluta)*. Logo, se 1em = 16px, então 2em = 32px e assim sucessivamente. 

Lembrando que a hierarquia continua sendo seguida. Por exemplo:

![image-20241024190435802](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241024190435802.png)

Nesse exemplo acima, BODY tem uma font size de 3em, ou seja **48px**, logo, a div .pai, que tem uma font size de 1.5em teria **72px** *(pois levando em consideração a hierarquia, body tem 48px de tamanho, então **48** x 1,5 = 72)* e logo em seguida a div .filha com a font size de 3m, ou seja 225px *(72 x 3 = 225)*.

![image-20241024190501387](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241024190501387.png)

*UM ADENDO: Na W3C a indicação é de que, para unidades de medidas relativas, usemos o "em", pois o "rem" é mais novo.*



- **Unidade "REM"**

É o root font-size, ou seja ele sempre olhará a propriedade da **raiz** e não a do pai. Nas hierarquias, a tag html sempre será a raiz. Por exemplo:

![image-20241024192112138](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241024192112138.png)

Se na raiz (html) a font size está **32px**, logo, seguindo a ordem *(e lembrando que rem segue a raiz)*, body, que está com 3rem possui **96px** (32 x 3 = 96), a div .pai, que está com 1.5rem possui 48px (32 x 1,5 = 48) e a div .filha, que está com 0.5rem possui 16px (32 x 0,5 = 16). Ou seja o cálculo é sempre feito de acordo com a raiz e não de acordo com a hierarquia anterior.

![image-20241024192817762](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241024192817762.png)



**Unidades de medidas absolutas (ou fixas)**

Existem várias unidades fixas/absolutas, podemos até usar cm se quiser, porém usaremos, no máximo, 2 ou 3 tipos durante toda a carreira.

**Medida "pixel"**

Pixel é o menor elemento em um dispositivo de exibição *(tela, monitor, tela de celular etc)*, são aqueles pontinhos quadrados bem pequenos que compõem as imagens.

Essa unidade é a que será mais usada quando precisarmos de medidas absolutas para alguma coisa *(largura e altura, tamanho de fonte, etc)*.

A W3C indica que usemos ou o "px" como **medida absoluta** ou o "em" como **medida relativa**.

Falando em questão de responsividade, as unidades absolutas podem dar problema no seu site, o pixel, por exemplo, a depender do tamanho da tela do dispositivo de quem estiver navegando, a página ficará desconfigurada, fazendo com que saia do campo de visão total e crie um scroll.

​	![image-20241025102428232](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241025102428232.png)			![image-20241025102449049](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241025102449049.png)

​	![image-20241025102609777](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241025102609777.png)	 ![image-20241025102942602](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241025102942602.png)



**Vh e Vw**

**Unidade Vh**

Significa "viewport height" ou **ALTURA DA JANELA DE VISUALIZAÇÃO** (verticalmente). Ele se refere ao tamanho da altura da tela de onde está sendo visualizado aquele conteúdo. Por exemplo, se no site existem várias sessões e queremos que a altura dessa sessão seja baseada na altura da janela de visualização, ou seja, da tela *(será diferente para celulares, tablets, monitores etc., pois possuem tamanhos diferentes)*, a vw servirá para que o conteúdo se adapte ao dispositivo que estiver sendo utilizado.



A tag "section" serve para demarcar seções que são cenários onde, geralmente, aplicamos as propriedades Vw e Vh. Assim como na tag div que, ao acrescentar um ponto "." na frente é possível adicionar automaticamente uma classe, na tag section isso também é válido.

![image-20241025124249200](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241025124249200.png)

![image-20241025124318164](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241025124318164.png)



No exemplo abaixo, podemos visualizar como a unidade Vh se comporta na prática. Ao colocar a altura *(height)* de 100vh, automaticamente a janela de visualização que estiver exibindo aquela página entende que a .primeira-sessao deverá preencher 100% do campo de visualização na tela, independente de qual seja o dispositivo.

​			<img src="C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241025124857505.png" alt="image-20241025124857505" style="zoom:67%;" />		<img src="C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241025120126325.png" alt="image-20241025120126325" style="zoom: 50%;" />

*Dando um inspecionar (F12) na página podemos observar como o border-bottom green serve para ilustrar onde encerra o tamanho da section em questão (que está com 100vh e deve ocupar a tela toda). Nesse caso o exemplo foi de um iPhone XR, mas qualquer dimensão que colocar como exemplo terá o mesmo resultado, pois ele **se adapta de acordo com a janela de visualização**.*

Em outro cenário, deixando a .primeira-sessao com altura *(height)* de 100vh e também colocando a .segunda-sessao com altura *(height)* de 100vh, então cada uma dessas sessões ocupará 100% da janela de visualização *(ao abrir a tela a primeira sessão estará ocupando tudo e ao rolar (scroll) pra baixo, a segunda sessão estará ocupando tudo)*.

<img src="C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241025124937620.png" alt="image-20241025124937620" style="zoom:80%;" />

​			<img src="C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241025121112196.png" alt="image-20241025121112196" style="zoom:50%;" />		<img src="C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241025121133212.png" alt="image-20241025121133212" style="zoom:50%;" />



É importante saber que, ao colocar uma altura de 100vh, a primeira sessão ocupará 100% da tela de visualização **E NADA MAIS**, logo, qualquer outra imagem/texto que seja inserido e ultrapasse essa proporção de 100%, ficará cortado. Como podemos visualizar no exemplo abaixo:

​	![image-20241025125046680](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241025125046680.png)		<img src="C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241025123143934.png" alt="image-20241025123143934" style="zoom: 67%;" />

Como a primeira sessão tem um Vh de 100, então, mesmo havendo mais conteúdo que deveria ser exibido na tela, isso não será possível, pois Vh é uma unidade de medida **FIXA**, ele vai exibir os 100% da janela e apenas isso. Tudo o que sobrar ficará cortado, dando espaço para a exibição da segunda sessão e assim por diante.



Para fazer com que a **altura cresça se for necessário**, ou seja, se o conteúdo que tem dentro da sessão for maior do que a altura da janela de visualização, podemos alterar a propriedade *height* para "min-height", ele então estenderá para além da altura da janela de visualização. Isso acontece porque quando utilizamos o "min-height: 100vh" falamos que ele terá **NO MÍNIMO** 100% da altura da janela de visualização, o que cria uma **flexibilidade** para que, caso o conteúdo dentro dessa sessão seja maior *(tenha muito conteúdo)* e não couber dentro da sessão/altura da tela, ele consiga expandir/crescer.

​		<img src="C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241025130410763.png" alt="image-20241025130410763" style="zoom: 80%;" />		<img src="C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241025130514919.png" alt="image-20241025130514919" style="zoom:67%;" />

*Agora as divs já não estão mais cortadas, aparecendo por toda a extensão da primeira sessão.*



**Unidade Vw**

Significa "viewport widht" ou **LARGURA DA JANELA DE VISUALIZAÇÃO** (horizontalmente). A proposta entre as unidades é parecida, porém agora será aplicada na largura.

Ao colocar a .primeira-sessao com uma largura *(widht)* de 100vw, automaticamente ele ocupa 100% da largura da janela de exibição e cria uma barra de scroll, porque o conteúdo está **ABAIXO** do scroll *(ao ocupar a largura total, ele não conta o scroll como parte da tela de visualização)*.

​			<img src="C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241025132806120.png" alt="image-20241025132806120" style="zoom:67%;" />		<img src="C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241025133035303.png" alt="image-20241025133035303" style="zoom: 67%;" />



Seguindo a mesma lógica do vh, ao colocar um "min-widht: 100vw", avisamos que a largura terá **NO MÍNIMO** 100vw, ou seja, deverá exibir todo o conteúdo horizontal na tela de visualização, independente do tamanho, criando essa flexibilidade para, se for necessário, ele expandir a largura.

![image-20241025133554191](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241025133554191.png)



**Box-Sizing (Border-Box)**

Essa propriedade nos permite trabalhar mais facilmente com o cálculo do tamanho da largura e altura dos elementos. 

Ela nos permite **incluir** no cálculo da altura ou largura o padding e o border, somando o seu valor total.

Se não especificar a propriedade do box-sizing com o valor do border-box, a altura e a largura do elemento será calculada somando o padding e o border.

O cálculo é feito da seguinte forma: largura + padding esquerda + padding direita + border esquerda + border direita = largura total do elemento.

Por exemplo:

​		![image-20241025173112300](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241025173112300.png)	![image-20241025173326192](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241025173326192.png)

Como no CSS está estilizado para ter 100px de largura e cada um dos lados tem 10px, então a conta seria: 100 + 10 + 10 + 10 + 10 = 140, exatamente como pode-se observar ao inspecionar a página. *(Então é: 100 de largura + 10 de padding esquerda + 10 de padding direita + 10 de border esquerda + 10 de border direita = 140 que é a largura total do elemento - 140x140)*.

O mesmo cálculo é feito para altura, apenas invertendo o cálculo para: altura + padding de cima + padding de baixo + border de cima + border de baixo = altura total do elemento".

Isso significa que, quando definimos uma largura e uma altura, o elemento vai parecer maior se tivermos um padding e um border sem border-box, pois eles serão somados e o objeto que teoricamente era pra ser 100x100 (width x height), como definido no exemplo, acaba se tornando 140x140.

Por esse motivo existe a propriedade "box-sizing" com o valor "border-box". Ao fazer a inclusão dela na div .com.border.box podemos ver que ela finalmente se adaptou e reconheceu a altura total e largura total, ignorando o padding e border.

​			![image-20241025175052633](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241025175052633.png)	![image-20241025175108088](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241025175108088.png)

Ao fazer a inclusão do "box-sizing: border-box" ele automaticamente já faz o cálculo de 100px, deixando 10px para cada lateral (esquerda e direita), que totaliza 40px, ou seja o centro fica com 60px + 40px de padding e border = 100px, como era o desejado.

![image-20241025175805545](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241025175805545.png)
