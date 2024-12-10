# CSS3 (Intermediário) :book:

:link: Notion: https://glowing-scilla-18d.notion.site/CSS3-Intermedi-rio-132bf6c7b63d81589d4ac4e8f8b74f34?pvs=74



Como o próprio nome já diz, CSS vem de *Cascading Style Sheets*, ou folhas de estilos em cascata.

Seletor é tudo o que está **ANTES** do abre chaves "{", quanto mais específico for o seletor, maior prioridade ele terá quando aplicar estilos.



**Efeito Cascata**

No efeito cascata, o CSS faz a leitura do código de cima para baixo, ou seja, se tiver, por exemplo, um background color azul em uma div específica no início do código e no final tiver outro background color laranja para essa mesma div, o que vai valer é o laranja, pois ele veio por último e, sendo assim, foi o último parâmetro lido.

![image-20241122173533428](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241122173533428.png)



Dando um inspecionar na página é possível ver que o azul está cortado, isso acontece porque ele tentou aplicar essa regra, mas viu que tinha outra igual e riscou a anterior.

![image-20241122173738388](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241122173738388.png)



Contudo, caso tenha algum estilo que não foi feito na página de css (style.css) e sim no corpo do HTML *(dentro do head e **DEPOIS** da tag link)*, então, quando for feita a leitura, será levado em conta o que está no html.

![image-20241122180332561](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241122180332561.png)

*OBS.: isso aconteceu porque a ordem de leitura ficou (de cima pra baixo) html > link > style.css > background color aqua > background color orange > volta para html > tag style com background color blueviolet. Caso a tag style estivesse acima da tag link, então a cor final seria orange. Sempre será lido o estilo que veio por último na cascata.*



**Mas é importante lembrar, NÃO DEVEMOS ESTILIZAR OS CAMPOS INTERNAMENTE NO CORPO DO HTML, não é recomendado e causa confusão! Isso deve ser feito na página de estilo do CSS.**



**Especificidade**

É uma regra que determina quais estilos serão aplicados a um elemento quando há conflitos entre seletores. Quanto maior a especificidade de um seletor, mais prioridade ele tem.



**Pontuação da especificidade:**

1. **Inline styles** (atributo style diretamente em uma tag no HTML) têm mais peso, mas, como dito anteriormente, **NÃO** deve ser utilizado.
2. **IDs** (#id) são mais específicos que classes, atributos e pseudo-classes.
3. **Classes**, atributos ([atributo]) e pseudo-classes (:hover) têm menos peso que IDs.
4. **Elementos** (div, p) e pseudo-elementos (::before) têm o menor peso.

A especificidade garante que o estilo desejado seja aplicado corretamente, mesmo com múltiplas regras conflitantes.



Diferente do modelo cascata, em que tudo é lido de cima para baixo e o que vale é a última estilização, nesse, o que vale é a maior especificidade, ou seja, indiferente se a regra está vindo em primeiro, no meio ou por último, se ela for a mais específica, então é ela que será aplicada.

![image-20241123125725410](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241123125725410.png)

![image-20241123124936184](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241123124936184.png)



**DICA: ao passar o mouse por cima, o vs code mostra qual a especificidade do seletor. Por exemplo:**

<img src="C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241123125031070.png" alt="image-20241123125031070" style="zoom:80%;" />	<img src="C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241123125056943.png" alt="image-20241123125056943" style="zoom:80%;" />	<img src="C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241123125112808.png" alt="image-20241123125112808" style="zoom: 80%;" />

*0, 0, 1 tem menor especificidade*

*0, 1, 1 tem média especificidade*

*1, 0, 0 tem maior especificidade*

[Calculadora de especificidade](https://specificity.keegan.st/?_gl=1*7f4uiy*_ga*MTEwMjE3ODAuMTcyODM5NjEwNA..*_ga_37GXT4VGQK*MTczMjMwMzAyNS40Ni4xLjE3MzIzMDMwMzUuMC4wLjA.)



É possível dar um peso extra na estilização colocando um "!important" logo após a propriedade no CSS, mas também **não é recomendado**, pois, além de ser possível colocar vários "!important" na página, o código fica poluído e difícil de dar manutenção.

![image-20241123130410775](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241123130410775.png)



Sempre que precisar estilizar elementos, evite utilizar IDs, atributo style na tag ou !important. Dê preferência para classes, pois assim sempre mantém o mesmo nível de estilização, ficando sempre naquele nível de classe, sem ter algo mais ou menos específico para ficar confundindo. Salvo casos em que precisar estilizar um ID ou tag diretamente, mas já tendo conhecimento das regras e conceitos.



**Estilos de texto**

São propriedades usadas para personalizar a aparência de textos, como cor, tamanho, fonte, espaçamento e decoração. Eles servem para melhorar a estética e a legibilidade, além de criar hierarquias visuais na página.

**Exemplos de estilos comuns:**

1. **Cor:** background-color: red
2. **Fonte:** font-family: Arial, sans-serif;
3. **Tamanho:** font-size: 16px;
4. **Espaçamento:** line-height: 1.5;
5. **Decoração:** text-decoration: underline;
6. **Alinhamento:** text-align: center.



**Alinhamento *(text-align)***

Define como o texto é posicionado horizontalmente dentro de um elemento. Melhora a organização e legibilidade do conteúdo, ajustando o layout ao design desejado.

- **Left**: alinha o texto à esquerda (padrão).
- **Right**: alinha o texto à direita.
- **Center**: centraliza o texto.
- **Justify**: alinha o texto nas margens esquerda e direita, ajustando o espaçamento.



Nos exemplos abaixo teremos 3 textos que estão sendo estilizados no CSS para seus devidos lugares *(esquerda, direita e centro)*:

![image-20241123143557624](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241123143557624.png)

​	![image-20241123143659453](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241123143659453.png)	<img src="C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241123143725870.png" alt="image-20241123143725870" style="zoom: 80%;" />

Também é possível fazer com que o texto fique justificado, ou seja, o parágrafo ocupa toda a largura do elemento *(como acontece com textos de jornais, revistas, trabalhos de escola, faculdade etc, é uma formatação que também tem no pacote office/word)*:

![image-20241123144315693](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241123144315693.png)

![image-20241123144333819](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241123144333819.png)	<img src="C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241123144406318.png" alt="image-20241123144406318" style="zoom: 80%;" />



**Transformação *(text-transform)***

Altera a forma como o texto é exibido em relação a maiúsculas e minúsculas. Padroniza a apresentação do texto sem alterar o conteúdo original no HTML. Ideal para estilização visual.

- **Uppercase**: transforma todo o texto em maiúsculas.
- **Lowercase**: transforma todo o texto em minúsculas.
- **Capitalize**: deixa a primeira letra de cada palavra em maiúscula.
- **None**: mantém o texto no formato original.



Nos exemplos abaixo teremos 3 textos que estão sendo estilizados no CSS para suas devidas formatações *(tudo em maiúscula, tudo em minúscula e cada primeira letra maiúscula)*:

![image-20241123151150611](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241123151150611.png)

<img src="C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241123151212391.png" alt="image-20241123151212391" style="zoom:80%;" />	<img src="C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241123151313891.png" alt="image-20241123151313891" style="zoom: 80%;" />



**Decoração *(text-decoration)***

Controla a aplicação de efeitos visuais ao texto, como sublinhado, linha sobre o texto ou linha removida. Melhora a aparência do texto e é útil para destacar, corrigir ou estilizar elementos, como links e títulos.

- **none**: Remove qualquer decoração.
- **underline**: Adiciona um sublinhado ao texto.
- **line-through**: Adiciona uma linha sobre o texto (tachado).
- **overline**: Adiciona uma linha acima do texto.



Nos exemplos abaixo teremos 3 textos que estão sendo estilizados no CSS para suas devidas formatações *(sublinhado, riscado no meio -como se fosse um rasurado- e sem decoração)*:

![image-20241123152550723](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241123152550723.png)

<img src="C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241123152606055.png" alt="image-20241123152606055" style="zoom:80%;" />	<img src="C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241123152627320.png" alt="image-20241123152627320" style="zoom:80%;" />

*Geralmente, os links vem por padrão com um sublinhado embaixo, então, para retirar essa decoração, faz-se o uso do text-decoration: none.*



**Altura entre linhas *(line-height)***

Define o espaçamento vertical entre as linhas de texto dentro de um elemento. Melhora a legibilidade e organização visual do texto, especialmente em blocos longos.

- Normal: Espaçamento padrão do navegador.

- Valores numéricos: 1.5 (multiplica a altura da linha pela fonte).
- Valores absolutos: 20px (define um valor fixo de altura).
- Valores percentuais: 150% (proporcional ao tamanho da fonte).



No exemplo abaixo teremos um texto que está sendo estilizados no CSS para sua devida formatação:

![image-20241123154122542](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241123154122542.png)

No caso do line-height, ele modifica o tamanho da linha/espaçamento entre uma linha e outra.

![image-20241123154305126](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241123154305126.png)	<img src="C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241123154316479.png" alt="image-20241123154316479" style="zoom:80%;" />

Quanto mais pixels, mais distante e quanto menos, mais grudadas e sobrepostas.

![image-20241123154404016](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241123154404016.png)	<img src="C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241123154414722.png" alt="image-20241123154414722" style="zoom:80%;" />



**Sombra no Texto *(text-shadow)***

Aplica sombras ao texto, criando efeitos visuais como destaque ou profundidade. Dá destaque ao texto, cria efeitos decorativos ou melhora a legibilidade sobre fundos complexos.



No exemplo abaixo teremos um texto que está sendo estilizados no CSS para suas devidas formatações. 

![image-20241123155804725](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241123155804725.png)

<img src="C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241123155818226.png" alt="image-20241123155818226" style="zoom:80%;" />   <img src="C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241123155834162.png" alt="image-20241123155834162" style="zoom:80%;" />  

*Sintaxe: text-shadow: deslocamento horizontal-x deslocamento vertical-y desfoque da sombra cor da sombra;*

*No caso do exemplo das imagens: deslocamento horizontal 10px deslocamento vertical 10px desfoque da sombra 1px cor da sombra #808080*



Quanto maior o desfoque da sombra (mais px), menos será possível ler o que está atrás e vice-versa.

<img src="C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241123161927714.png" alt="image-20241123161927714" style="zoom:80%;" />  <img src="C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241123161945732.png" alt="image-20241123161945732" style="zoom:80%;" />



Segue abaixo a formatação geral dos fundos utilizados durante a explicação dos exemplos:

![image-20241123162534174](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241123162534174.png)



**Propriedades das Fontes**

Definem a aparência do texto, como o tipo, estilo e família de fontes usadas.

O font-family: define a família de fontes. Exemplo: "font-family: Arial, sans-serif;" *(usa Arial, ou uma fonte sem serifa similar)*.

**Fontes comuns:**

- **serif**: fontes com "terminações" decorativas *(ex.: Times New Roman)*.
- **sans-serif**: fontes sem essas "terminações" *(ex.: Arial)*.
- **monospace**: fontes com espaçamento fixo *(ex.: Courier)*.



Uma **fonte sem serifa similar** é uma fonte da família **sans-serif** (sem serifa), que o navegador usa como substituta caso a fonte principal definida no font-family não esteja disponível no sistema do usuário.

![image-20241123164457257](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241123164457257.png)

*Sans-serif: Fontes sem serifas, com aparência mais limpa e moderna. Ex.: Arial.*



![image-20241123164526703](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241123164526703.png)

*Serif: Fontes com serifas, pequenos traços decorativos nas extremidades das letras. Ex.: Times New Roman.*



![image-20241123164717371](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241123164717371.png)

*Monospace: Fontes onde todas as letras têm o mesmo espaçamento horizontal. Ex.: Courier New.*



Na prática, ao fazer a estilização de um elemento no CSS, o próprio vs code nos dá algumas opções de fontes e também já classifica se é serif, sans-serif ou monospace.

![image-20241123165318502](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241123165318502.png)



Essa propriedade de font-family pode ser aplicada tanto no html todo quanto em alguns elementos específicos. Geralmente vamos utilizar mais em elementos específicos, como parágrafos, títulos, para dar uma diferenciação entre um título e um texto normal.

![image-20241123165822694](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241123165822694.png)

<img src="C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241123165836613.png" alt="image-20241123165836613" style="zoom:67%;" /> <img src="C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241123165856743.png" alt="image-20241123165856743" style="zoom: 67%;" />

*Courier New está entre aspas simples, pois ela é um nome composto.*

*No h1 a fonte será "arial", caso não tenha, ele tentará carregar a fonte "helvetica", se também não tiver, então ele tentará carregar qualquer fonte que seja "sans-serif".*

No font-family existem **fontes safe**/seguras, que são as fontes que provavelmente terão no sistema operacional do usuário.

Lembrando que, como já foi estudado anteriormente, existem outras formas de estilizar fontes, como font-size, font-weight *(do 100 ao 400 normal/regular, 500 ao 700 bold/negrito, 700 ao 900 extra bold).*



**Usando fontes do Google Fonts**

Com o site aberto é possível visualizar todas as fontes existentes e há duas formas para poder incorporar elas ao html/css.

Se quiser manter o HTML mais limpo, então podemos importar as fontes pelo CSS, mas também quando você importa pelo CSS, suas fontes podem demorar pra carregar, isso porque você precisa que o arquivo de CSS termine de ser baixado por completo para renderizar elas.

**HTML**: quando você quer que as fontes sejam carregadas de forma mais rápida, o que ajuda a melhorar o desempenho;

**CSS**: pode ser melhor pra organização do código, mas pode afetar o desempenho, principalmente se o arquivo de CSS tiver muitos estilos sendo aplicados;



**PRIMEIRA FORMA (HTML)**

1. Encontre a fonte que deseja utilizar no google fonts, na lateral superior direita clique no botão "get font"

   ![image-20241123192333859](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241123192333859.png)

2. Na página seguinte clique em "get embed code"

   ![image-20241123192403813](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241123192403813.png)

3. Aparecerão duas formas de incorporação do código, mas, para o HTML, utilizaremos **\<link>**

   ![image-20241123192454175](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241123192454175.png)

4. Copie o código da fonte com CTRL + C ou clicando no botão "Copy code"

   ​			![image-20241123192526928](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241123192526928.png)		![image-20241123192540576](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241123192540576.png)

5. No arquivo html, antes da tag title, cole o código (CTRL + V) em uma linha em branco

   ![image-20241123201445563](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241123201445563.png)

   *As duas primeiras linhas fazem uma pré conexão com o google fonts, enquanto a última faz o download da fonte.*

6. Após feito isso, é possível testar para ver se a fonte está funcionando aplicando uma tag de style no h1, por exemplo *(esse método continua não sendo recomendado, será apenas para teste)*

   ![image-20241123201505115](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241123201505115.png)

7. Ao abrir a página e inspecionar em cima do elemento, concluímos que a fonte foi reconhecida e está funcionando

   ![image-20241123201605974](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241123201605974.png)

Para fazer a inclusão de várias fontes, basta ir adicionando elas no google fonts (cada vez que clica em "get font", uma fonte nova é incluída na lista) e colar o novo código naquela linha acima de title (link). 

![image-20241123202021650](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241123202021650.png)

Caso vc já esteja fazendo uso de alguma fonte anteriormente e queira adicionar uma nova, deve-se ter todas essas font-families selecionadas no google fonts e refazer o processo desde o passo 2 em diante.

Para apagar alguma fonte da lista ou remover todas, basta clicar na lixeira.

![image-20241123195656473](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241123195656473.png)



**SEGUNDA FORMA (CSS)**

1. Encontre a fonte que deseja utilizar no google fonts, na lateral superior direita clique no botão "get font"

   ![image-20241123192333859](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241123192333859.png)

2. Na página seguinte clique em "get embed code"

   ![image-20241123192403813](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241123192403813.png)

3. Aparecerão duas formas de incorporação do código, mas, para o CSS, utilizaremos **@import**

   ![image-20241123212308673](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241123212308673.png)

4. Copie o código da fonte com CTRL + C ou clicando no botão "Copy code", porém, dessa vez ao invés de pegar o código por completo, devemos copiar apenas o que está **dentro** da tag style *(@import url...)*

   ​			![image-20241123192526928](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241123192526928.png)		![image-20241123192540576](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241123192540576.png)

   ![image-20241123195959472](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241123195959472.png)

   *Essa tag style é para quando for usar dentro do head no html (porém após o title), mas segue não sendo recomendado.*

5. Assim como já foi feito em aulas anteriores, basta criar uma tag de link:css e colar o código na folha de CSS

   ![image-20241123203619184](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241123203619184.png)	![image-20241123203640861](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241123203640861.png)

6. Com o código colado, escreva o seletor que deseja estilizar e atribua a formatação

   ![image-20241123203704366](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241123203704366.png)

7. Novamente, ao abrir a página e inspecionar em cima do elemento, concluímos que a fonte foi reconhecida e está funcionando

   ![image-20241123203853586](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241123203853586.png)

Para deixar tudo mais organizado, podemos criar um arquivo css para linkar as fontes.



**Usando fontes que não existem no Google Fonts**

Pode acontecer de algum cliente pedir para usarmos uma fonte que não tenha no google fonts. Ele pode mandar as fontes/arquivos *(em formato .ttf, .otf etc)*. Caso não receba, precisamos ir no site e baixar as fontes *(se forem pagas, temos que cobrar que o cliente pague e baixe para podermos usar -**NÃO DEVEMOS PAGAR E USAR NO PROJETO, POIS ISSO PODE DAR PROBLEMA PRA GENTE, deve ser feito pelo cliente**)*. 



**TTF (TrueType Font):** Formato mais simples, com boa compatibilidade e menor tamanho. Ideal para usos básicos.

**OTF (OpenType Font):** Formato mais avançado, suporta recursos extras como ligaduras e variações estilísticas. Mais flexível para designs complexos.



Utilizando o site "[DaFont](https://www.dafont.com/pt/)", basta ir no campo lateral direito do site para pesquisar qual fonte deseja e baixar na página seguinte

![image-20241124100957017](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241124100957017.png)	![image-20241124101219284](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241124101219284.png)

![image-20241124101201669](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241124101201669.png)

Será feito o download de um arquivo zip para descompactar. Nessa fonte do exemplo, vieram 4 arquivos, sendo dois tipos da mesma. Usaremos apenas os dois primeiros

![image-20241124101712624](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241124101712624.png)

Esses dois arquivos deverão ser extraídos para uma nova pasta que será criada no mesmo local do html

​				![image-20241124102444042](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241124102444042.png)		![image-20241124102454930](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241124102454930.png)

​			![image-20241124102617917](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241124102617917.png)		![image-20241124102638885](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241124102638885.png)

Feito isso, é possível visualizar que a pasta com as fontes foi reconhecida no vs code

![image-20241124102816841](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241124102816841.png)

Para configurar as fontes no projeto é preciso ir na folha de CSS e digitar @font-face, que já será preenchido automaticamente com "font-family" e "src: url()"

![image-20241124103148519](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241124103148519.png)

![image-20241124103206762](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241124103206762.png)

Dentro dessa estrutura vamos preencher o font-family com um nome que podemos criar para a fonte (nesse caso a fonte chama "Milky", então vamos deixar assim mesmo) e em src: url() vamos preencher com o caminho para chegar até a fonte.

![image-20241124103616999](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241124103616999.png)

**OS VALORES COLOCADOS DENTRO DOS ATRIBUTOS PRECISA ESTAR ENTRE ASPAS SIMPLES.**

Para colocar mais de uma fonte *(que na verdade é "a mesma fonte", mas em outro formato)*, basta colocar uma VÍRGULA *(não é ponto e vírgula)*, pular uma linha e escrever um novo url('*caminho para outra fonte*') e se tivesse mais fontes era só seguir o mesmo passo até incorporar todas

![image-20241124104454804](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241124104454804.png)

**Cada fonte precisa do seu próprio font-face, então se tiver 3 fontes distintas (por exemplo: uma "milky nice", uma "rimons" e outra "namaku"), as três necessitarão que seja criado um novo font-face completo (@font-face com font-family e src: url).**



Após configurado, basta estilizar a fonte no texto que desejar, utilizando o font-family

![image-20241124105629087](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241124105629087.png)

DICA: se o nome da fonte tiver espaços ou caracteres especiais o uso das aspas simples é **obrigatório** (se fosse Milky Nice, então o font-family deveria ser 'Milky Nice)'. Se o nome for simples, as aspas são opcionais.

É interessante colocar outra opção de font safe para que o navegador possa carregar, caso o usuário não possua a fonte em questão *(pelo menos se é sans-serif, serif, monospace etc)*.



Também podemos controlar o **peso** da fonte, como ja vimos anteriormente, basta colocar o font-weight, lembrando que do 100 ao 400 normal/regular, 500 ao 700 bold/negrito, 700 ao 900 extra bold.

![image-20241124110657647](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241124110657647.png)

Nesse caso, como foi colocado 100, o texto ficou com menos negrito.



No próprio site DaFont é possível ver se a fonte possui **glifos** e quais são eles. Isso é muito importante, pois quando estamos fazendo um site em português ele precisa ter as acentuações, do contrário, as palavras que possuem acento ficarão fora de formato.

![image-20241124111208843](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241124111208843.png)

Quando abrir uma fonte, basta rolar a página até um pouco mais abaixo e logo será possível visualizar os glifos.

Um glifo **é um elemento da escrita**.



**Estilizando Links**

Por padrão, os links já vem estilizados com essa cor azul e underline/sublinhado (que é o text-decoration: underline)

Outra característica dos links é que aparece uma mãozinha quando passa o mouse por cima

![image-20241124112326398](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241124112326398.png)	![image-20241124112534110](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241124112534110.png)



Para alterar o ícone da mão, deve-se ir na folha de CSS e fazer a estilização da tag a. Com a propriedade "cursor" é possível alterar como o cursor do mouse deve se comportar ao passar sobre o elemento.

​		![image-20241124113130624](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241124113130624.png)		![image-20241124112534110](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241124112534110.png) 	"pointer" = mãozinha



O vs code por si só já dá algumas opções de cursores para escolher

![image-20241124113815417](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241124113815417.png)

​		![image-20241124114403193](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241124114403193.png)		![image-20241124114441834](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241124114441834.png) 	"progress" = seta com loading



Os links também tem "estados", ou seja, quando clicamos ele troca de cor por padrão, saindo de azul e ficando roxo, indicando que já foi clicado/visitado

![image-20241124114806207](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241124114806207.png)

É possível alterar esse evento que faz a cor ficar roxa no CSS, estilizando novamente a tag a, porém incluindo a pseudo-classe de que ela foi visitada, ficando a:visited

![image-20241124115640975](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241124115640975.png)

*Lembrando que essa estilização serve apenas para links que foram **CLICADOS**. Para alterar a cor azul padrão do link antes de ser clicado, deve-se seguir outro passo*



Outra alteração possível de fazer é com a pseudo-classe "active", onde, sempre que clicar no link, ele vai momentaneamente ficar daquela cor *x* e depois ir para a cor de "visited" 

![image-20241124120131094](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241124120131094.png)

*Então, nesse exemplo, ele seria azul -padrão-, iria para vermelho e depois ficaria laranja*



Fazendo alterações um pouco mais elaboradas, e utilizando outra pseudo-classe, é possível fazer com que o link tenha um novo estado quando o mouse passar por cima utilizando o "hover"

![image-20241124121911646](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241124121911646.png)  *OBS.: foi dado um padding de 10px*



Quando o hover está ativo pode acontecer do active ser cancelado, principalmente se o hover tiver mais especificidade/prioridade.



**Estilizando Listas**

Geralmente, os sites removem os bullets de customização padrão das listas (que são aquelas bolinhas laterais nas linhas não ordenadas e os numerais nas listas ordenadas) e para realizar essa remoção utilizamos o CSS

![image-20241124125028447](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241124125028447.png)

Por padrão, a lista não ordenada vem com o list-style-type: disc, mas é possível fazer essa alteração no vs code. Ele mesmo já sugere algumas opções.

![image-20241124125521235](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241124125521235.png)

O que é mais utilizado é "none", para deixar sem nenhum bullet



Além disso, podemos trocar esses bullets padrões por uma imagem que tenha dentro do projeto. Para fazer isso, temos que colocar a propriedade list-style-image: url(*'./caminho para a imagem'*)

![image-20241124130030838](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241124130030838.png)

![image-20241124130951613](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241124130951613.png)

***A IMAGEM NÃO PODE ESTAR COM ESPAÇO NO NOME, SENÃO NÃO FUNCIONA!** (Por exemplo, se o nome da imagem fosse "check list" daria errado o caminho, o certo seria colocar "check-list")*

Nesse tipo de estilização com list-style-image não é possível mexer no tamanho do bullet/imagem, por esse motivo usamos pseudo-classes (vamos aprender isso no nível CSS Avançado). *Para que essa imagem do exemplo funcionasse ela teve que ser do tamanho 16x16.*



Para fazer com que o navegador tenha outra opção de bullet padrão para usar (caso a imagem não carregue/não tenha ela no projeto), deve-se utilizar a propriedade list-style: square *(ou outro bullet padrão que desejar)* url('*./caminho para a imagem*')

![image-20241124144626826](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241124144626826.png)

Usar inside faz com que os bullets fiquem dentro dos li's, caso contrário eles ficam pra fora, o que às vezes pode não ser interessante, se quiser estilizar tudo junto

![image-20241124145246493](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241124145246493.png)



Se quiser, podemos estilizar o fundo colocando um background color, fazendo isso será possível ver que, por padrão, o navegador coloca uma margem na lateral

![image-20241124145902867](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241124145902867.png)

Para tirar basta fazer o reset com * (que afeta na estilização de qualquer elemento da página)

![image-20241124150302448](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241124150302448.png)

![image-20241124150905996](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241124150905996.png)



**Estilizando Backgrounds**

Quando a div não possui conteúdo dentro, ela fica com largura e altura igual a zero, então nenhum efeito de estilo se aplica. Por exemplo: 

​	![image-20241124152748561](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241124152748561.png)		![image-20241124152941218](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241124152941218.png)

![image-20241124153020379](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241124153020379.png)	*nenhum conteúdo = nenhuma estilização*

<img src="C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241124153916260.png" alt="image-20241124153916260" style="zoom:80%;" />	*com conteúdo = estilização aplicada*



**Background Image**

Para adicionar uma imagem de fundo na div é necessário colocar uma propriedade no CSS e se atentar às regras de tamanho. Essa propriedade é a background-image seguida da url que é o local onde se encontra aquela imagem *(lembrando de usar parênteses e aspas simples)*

![image-20241124155630856](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241124155630856.png)

![image-20241124155008951](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241124155008951.png)

O fundo de gatinho foi reconhecido e aplicado, porém as dimensões não são reconhecidas e, por isso, a imagem fica cortada e repetida, o que é um comportamento padrão de um background-image. Para termos uma "melhor visualização" da imagem, podemos dar um padding de 100px

![image-20241124155243791](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241124155243791.png)

![image-20241124155301083](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241124155301083.png)

*A imagem se repete tanto horizontalmente (eixo x), quanto verticalmente (eixo y)*

Para resolver essa questão, podemos estilizar outras classes, nesse mesmo exemplo, no html foi definida a classe bg-image, nela conseguimos mexer na altura e largura da imagem *(lembrando de retirar o padding que foi dado na classe .bg)*

<img src="C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241124160222433.png" alt="image-20241124160222433" style="zoom: 80%;" />		<img src="C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241124160241393.png" alt="image-20241124160241393" style="zoom: 67%;" />

*O tamanho da imagem pode ser consultado pelo próprio vs code ou no arquivo da imagem no desktop, para que não perca qualidade.*

*No caso do gatinho: Largura = 514px e Altura = 340px (uma div é maior que isso)*



**Background Repeat**

Define se e como uma imagem de fundo será repetida dentro de um elemento. Controla o comportamento de imagens de fundo, ajustando o layout e o design visual.

repeat: repete a imagem horizontal e verticalmente (padrão).

- Usado para criar fundos contínuos de padrões como madeira, areia ou estrelas.
- Exemplo: sites de papel de parede ou texturas, como bancos de imagens (Unsplash).

no-repeat: não repete a imagem.

- Garante que o logo aparece apenas uma vez.
- Exemplo: páginas de empresas com um logotipo ou imagem promocional no cabeçalho, como Google na página inicial.

repeat-x: repete apenas na horizontal.

- Cria linhas ou barras visuais na horizontal.
- Exemplo: banners horizontais decorativos em sites como Twitter (antigamente usado para separar seções).

repeat-y: repete apenas na vertical.

- Estende uma textura ou padrão vertical ao longo da página.
- Exemplo: barra lateral em blogs (como temas antigos do WordPress).



Deixando a propriedade como no-repeat a imagem vai se ater a ficar somente do tamanho real dela, alinhada ao topo e a esquerda e sem repetir.

![image-20241124164221239](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241124164221239.png)

Para conseguir visualizar melhor que a imagem não repete e observar a div podemos definir uma altura *(lembrando que a imagem tem altura de 340px e foi dado agora um height 540px)*.

![image-20241124164814918](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241124164814918.png)

Seguindo a ordem das regras de repetições, trocando o no-repeat para repeat-x ele repetiria na horizontal e assim por diante.



**Background Size Cover**

Ajusta a imagem de fundo para cobrir todo o elemento, mantendo sua proporção. Prático em telas de fundo responsivas, como banners e heróis de sites.

Garante que a imagem ocupe todo o espaço do fundo, sem deixar áreas vazias, mesmo que partes sejam cortadas.

No exemplo foi dado um height de 540px novamente, mas como essa propriedade foi feita para cobrir tudo com a imagem (e ela tem 340 de height), então vai estourar e perder a qualidade, o que não é profissional.

![image-20241124171040012](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241124171040012.png)

![image-20241124171118649](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241124171118649.png)



**Background Fixed**

Fixa a imagem de fundo, fazendo com que ela permaneça estática enquanto o conteúdo da página rola. Cria um efeito visual de *parallax¹*, dando destaque ao fundo e melhorando o design. Prático em seções de destaque em sites modernos.

*¹ **Parallax** é um efeito visual onde o fundo do site se move em uma velocidade diferente do conteúdo em primeiro plano ao rolar a página, criando uma sensação de profundidade e dinamismo.*

*Por padrão o background-attachment é scroll, onde a imagem e o texto acompanham a rolagem da página.*

![image-20241124184026796](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241124184026796.png)

![image-20241124172546757](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241124172546757.png)



**Background Position**

Define a posição da imagem de fundo dentro do elemento. Controla onde a imagem será exibida, como centralizar ou alinhar em cantos específicos. Usado para ajustar a imagem em designs personalizados.

Exemplos de valores:

- Center: centraliza a imagem.
- Top right: alinha no canto superior direito.
- Coordenadas



Com o background position é possível definir qual será a localização da imagem

![image-20241124173233454](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241124173233454.png)

Nesse caso o valor do background position foi left, mas, apesar de estar de fato para a esquerda, ela ainda ficou alinhada ao centro e não no topo a esquerda, por exemplo. Isso acontece porque essa propriedade pode receber mais de um valor, caso não seja colocado outro valor, por padrão, ele fica como center.

Para exemplificar, podemos colocar o background-position: bottom right e então a imagem deverá ficar no canto inferior direito.

![image-20241124173627551](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241124173627551.png)

*Essa propriedade também aceita valores em unidades de medidas relativas e absolutas/fixas, mas geralmente não são utilizadas.*



É possível utilizar todas essas propriedades na forma encurtada, colocando tudo em apenas uma propriedade, ficaria dessa forma:

![image-20241124174553525](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241124174553525.png)

Sempre que puder utilizar na forma encurtada é melhor, assim fica mais limpo e mais fácil de dar manutenção. Lembrando que é importante se atentar a ordem para que funcione.



**Posicionamento com Display**

Define como os elementos serão posicionados e organizados na página. Controla o comportamento e layout dos elementos, ajudando a estruturar a página de forma organizada.

Block: ocupa toda a largura disponível (ex.: \<div>)

Inline: ocupa apenas o espaço necessário (ex.: \<span>)

Inline-block: combina características de inline e block

None: esconde o elemento

Flex: cria layouts flexíveis *(CSS Avançado)*

Grid: cria layouts em grade *(CSS Avançado)*



Antes das explicações e exemplos, na folha de estilo do CSS foram resetados alguns estilos:

![image-20241125134349562](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241125134349562.png)



**Display block**

O elemento ocupa toda a largura disponível e começa em uma nova linha. Serve para criar blocos de conteúdo.

É possível colocar uma largura desejada no display e assim, conseguir controlar o tamanho dele, mas o comportamento padrão é de que ele ocupe toda a linha página.

![image-20241125134938105](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241125134938105.png)

![image-20241125135716171](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241125135716171.png)

Não foi necessário colocar a regra "display: block" pois alguns elemento já tem o comportamento de bloco por padrão. Então, nesse caso, por se tratar de uma ul seria redundante. No caso de div ou p, por exemplo, faz-se necessário.

Elementos do tipo block level ou display block sempre vão ocupar a página inteiro por padrão, ou seja, colocando ou não uma largura específica, eles continuarão um em cima do outro e não um ao lado do outro.



**Display inline**

O elemento ocupa apenas o espaço necessário e não quebra linha. Serve para estilizar partes de texto ou elementos menores. Strong e span são exemplos.

Em elementos que são inline level ou possuem display inline não é possível definir uma altura ou largura, o comportamento padrão é de que fique sempre um ao lado do outro e nas mesmas dimensões.

![image-20241125145351690](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241125145351690.png)

![image-20241125145444064](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241125145444064.png)  *width: 500px não altera nada*



**Display inline-block**

Comporta-se como inline, mas permite ajustar largura e altura como um bloco, como, por exemplo botões, menus ou imagens alinhadas lado a lado. Serve para combinar comportamentos de inline e block.

Esse regra permite colocar uma altura e largura nos elementos, então as li's ficaram uma ao lado da outra (inline), mas permitindo alterar as dimensões. 

![image-20241125150926374](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241125150926374.png)



**Display none**

Esconde o elemento completamente da página (sem ocupar espaço). Serve para ocultar elementos dinamicamente.

![image-20241125152659423](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241125152659423.png)

*OBS.: normalmente quando queremos esconder alguma coisa, não há necessidade de ficar especificando demais. Nos outros exemplos de display foi dada a classe + li, nesse caso do display none, foi dada somente a classe, pois a intensão é que esconda tudo o que tiver ali (no caso toda a ul).*



Ainda que não apareça visualmente na página, ao dar um inspecionar é possível ver os dados que constam no elemento, pois ele não some do HTML.

​				![image-20241125151658987](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241125151658987.png)		![image-20241125151731692](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241125151731692.png)



**Position Static, Relative e Absolute**

Position define como um elemento é posicionado na página. Serve para criar layouts flexíveis e personalizar a posição de elementos na página.



Antes das explicações e exemplos, na folha de estilo do CSS foram resetados alguns estilos:

![image-20241125154658061](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241125154658061.png)



**Position Static**

É o padrão. O elemento segue o fluxo normal do layout, sem posicionamento especial. Ainda que tente mover para os lados, não fará diferença, pois esse é o comportamento padrão de um elemento estático.

![image-20241125162019938](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241125162019938.png)	![image-20241125162037671](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241125162037671.png)

OBS.: o uso do position: static nesse caso é redundante *(e ele é um display block)*.



**Position Relative**

O elemento permanece no fluxo normal, mas pode ser ajustado com top, right, bottom, left *relativamente* à sua posição original.

Por exemplo, se quiser que ele se mova 100px para a direita, então temos que colocar left: 100px, pois o comando se refere a qual lado será dado o espaçamento e não sobre a div em si.

![image-20241125163115975](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241125163115975.png)	<img src="C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241125163201434.png" alt="image-20241125163201434" style="zoom:67%;" />



**Position Absolute**

Remove o elemento do fluxo normal da página e o posiciona em relação ao **elemento pai mais próximo** que tenha position: relative, absolute ou fixed.

Serve para posicionar elementos de forma precisa, ignorando o layout dos demais elementos.

É usado quando precisa posicionar algo em um local específico, sem depender do fluxo normal da página, como botões flutuantes, modais ou ícones em um canto.

Quando temos uma propriedade position absolute no elemento estamos dizendo que queremos destacar esse elemento da camada padrão/original que ele estava.

Usando a analogia das camadas, por exemplo, foi-se criada uma camada COM TODOS os elementos anteriores (static e relative), PORÉM quando um dos elementos recebeu um "position: absolute" então é como se ele tivesse criado uma nova camada. O elemento do position absolute fica em cima da outra camada de baixo.

​    ![image-20241126170410163](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241126170410163.png)	![image-20241126170429806](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241126170429806.png)

<img src="C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241126170530289.png" alt="image-20241126170530289" style="zoom:50%;" />	

Enquanto o position absolute está comentado (o bloco darkcyan está sem nenhuma propriedade ativa), conseguimos visualizar o que era pra ser um outro elemento estático (vermelho) que viria a seguir. Mas, quando descomentamos o absolute e ele fica válido na página, então o bloco darkcyan sobrescreve o vermelho, ou seja, o absoluto cria uma nova camada por cima do estático.

Podemos observar isso melhor se colocarmos o bloco absolute um pouco mais para a direita:

​        ![image-20241126171607629](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241126171607629.png)	<img src="C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241126171631163.png" alt="image-20241126171631163" style="zoom:50%;" />

O comportamento padrão de um elemento position absolute é de se movimentar na viewport como um todo, pois ele está destacado em uma camada só dele. Por exemplo, se vc colocar um top 0, ele vai para o topo da página, mas terá o mesmo efeito que teve anteriormente, porém sobrescrevendo o elemento do topo.

<img src="C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241126173554392.png" alt="image-20241126173554392"  />

<img src="C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241126173624010.png" alt="image-20241126173624010" style="zoom: 67%;" />



Existe uma forma de manter esse elemento no lugar onde foi criado, basta que o elemento absoluto esteja dentro de um elemento relativo.

Usando de exemplo uma div que tem um elemento RELATIVO *(pai)* com filho *(que é o absolute)* e dentro dessa div está o elemento absoluto *(filho)*, podemos ver que o filho respeita as dimensões do pai, então mesmo colocando para ele ir top, bottom, left etc, ele vai seguir o comando da propriedade, porém dentro das diretrizes do pai (fica travado/linkado um ao outro).

​	<img src="C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241126175857957.png" alt="image-20241126175857957" style="zoom:80%;" />	<img src="C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241126175726186.png" alt="image-20241126175726186" style="zoom:67%;" />



**Position Fixed**

Posiciona o elemento em relação à *janela do navegador* (viewport), ignorando o scroll da página. Serve para criar elementos fixos na tela, como menus, barras de navegação ou botões de voltar ao topo. Quando scrolla a tela o elemento continua sendo visível, sobrescrevendo os elementos abaixo (semelhante ao position absolute).

<img src="C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241126201127376.png" alt="image-20241126201127376"  />

Aqui, por enquanto, está sem o position fixed, até então o menu está lá em cima, porém, ao scrollar a tela para baixo, o menu "some"/não desce junto, não está fixo na tela.

![image-20241126201327581](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241126201327581.png)

Agora com a propriedade fixed, ele assume seu local e fica fixo quando scrolla a tela, porém o comportamento é parecido com o absolute, pois ele fica por cima das camadas e também ocupa 100% da tela por padrão.

![image-20241126201421286](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241126201421286.png)

Dando alguns comandos no body e no header será possível modificar isso.

Para que volte a ocupar 100% da viewport = width: 100% no header *(porém o texto vai continuar ficando por baixo, o que ,geralmente, não é o esperado)*

Para fins mais estéticos e melhorar a visualização, foi dado um paddin: 20px no header *(assim o tamanho do tamplate de menu ficou mais largo, mais fácil e bonito de visualizar)*

Agora, por fim, para empurrar o body pra baixo, e conseguir visualizar o texto atrás sem que o menu fique na frente, vamos ter que fazer um cálculo.

1. Inspecione a página para visualizar a caixinha que tem todos os tamanhos dos conteúdos *(altura, largura, padding...)*

   ![image-20241126232445450](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241126232445450.png)

2. Some os valores de padding (20 top + 20 bottom) e com o valor de altura (height 27px) que dará 67px

   ![image-20241126232544890](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241126232544890.png)

3. Esse valor de 67px deverá ser dado no body com o padding-top: 67px, porém, ao fazer isso, automaticamente todos os textos terão recebido a mesma propriedade e serão empurrados para baixo *(o menu e os textos da página terão esse afastamento no top de 6px)*

   ![image-20241126232638972](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241126232638972.png)

4. Isso acontece porque o header com o menu está dentro do body, então ele também vai ser empurrado

5. Para resolver isso, podemos colocar um top: 0 no header e, então, todo os textos que pertencem ao header ficarão com o padding de 67px, dando assim espaço para que o menu apareça sem sobrescrever ninguém

   ![image-20241126232726975](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241126232726975.png)

6. Agora sim será possível scrollar a tela com o menu em position fixed e ele estará fixado na tela, porém não vai tampar o texto quando iniciar a página, apenas ao scrollar a página que ele vêm junto, passando por cima e cobrindo as camadas abaixo.

   ![image-20241126232744720](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241126232744720.png)



**Introdução a Responsividade**

Um layout, a parte visual do site, é responsivo quando fica visualmente bonito tanto na tela de um celular, quanto na tela de um desktop, tablets etc.

Antigamente as pessoas faziam duas versões de HTML e CSS, uma para monitores maiores e uma para celular. O que é bem ruim para dar manutenção, já que teria que mexer em duas bases de código e com o design responsivo temos apenas um html e um css que, aplicando algumas regras, o layout se adapta conforme a resolução do usuário.

Esse é o corpo do HTML, para levarmos de base na didática que será aplicada:

![image-20241127114618943](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241127114618943.png)

A princípio foi dado um reset no margin e padding de toda a viewport *(dessa vez em um arquivo CSS separado -reset.css)*

![image-20241127112645495](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241127112645495.png)

No menu/cabeçalho foram dadas as seguintes propriedades:

![image-20241127112842280](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241127112842280.png)

* Um background-color cinza de fundo no body
* No cabeçalho foi colocado um background-color verde e também um padding de 10px *(top e bottom)* e 5px *(left e right)*
* O logo está com um display inline-block  para que os outros elementos fiquem na linha dele *(que serão os itens da ul>li -quem somos, onde estamos, contato-)*, senão eles ficariam um embaixo do outro *(o que é o comportamento padrão de um display block)*
* No nav foi dado um float¹ right para que os itens ficassem na direita
* No nav li também foi necessário dar um display inline-block *(para que ficassem um ao lado do outro)* com um padding de 15px para ter um espaçamento

![image-20241127121400255](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241127121400255.png)

*¹ Float é uma propriedade CSS que posiciona um elemento à esquerda (left) ou à direita (right) dentro de seu contêiner. Serve para criar layouts, permitindo que texto ou outros elementos fiquem ao lado do elemento flutuante. Apesar de útil, o float é menos usado atualmente devido a técnicas mais modernas como **Flexbox** e **Grid**.*



No main foram dadas as seguintes propriedades:

![image-20241127130839469](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241127130839469.png)

- Um background-color branco, para ficar no fundo do conteúdo, mas por cima do cinza
- Um padding de 30px para dar um espaçamento entre o conteúdo do cabeçalho. OBS.: tudo está ocupando a largura total da tela *(como era o comportamento padrão de se esperar)* e o parágrafo não tem nenhuma quebra de linha
- Para resolver a quebra de linha do parágrafo, foi dada uma largura (width) MÁXIMA da imagem de 900px *(o tamanho pode ser dado conforme quiser e achar interessante)*
- Feito isso, o texto terá a quebra de linha, porém ainda está todo localizado na esquerda da tela, para resolver foi dado um margin de 0 auto para que o conteúdo (h1, p) ficasse centralizado, ou seja, 0 para dizer que eu quero 0 espaçamento em cima e embaixo e auto, que é uma palavra chave, vai deixar a div automaticamente centralizada, pegando tudo que "sobrou" de área e dividindo metade pra direita e metade da esquerda *(todo o campo em cinza que estava sobrando na tela ficou agora 50/50 direita e esquerda e o conteúdo centralizado ao meio)*
- A largura (width) MÍNIMA da imagem foi ajustada para 320px *(geralmente não existem celulares com a tela menor do que isso)*
- E por último, a forma mais simples de resolver a dimensão da imagem seria colocando uma width de 100% nela, fazendo com que a imagem diminuísse e ocupasse toda a largura de conteúdo da tag main
- Ainda sobre a dimensão da imagem, geralmente, em aparelhos menores *(que não sejam um pc, tablet etc)*, não queremos que carregue uma imagem grande, então é recomendado que use a tag picture *(a tag img que havia sido criada no corpo do html, deverá ser apagada e substituída pela picture)*, ao fazer isso, conseguimos configurar para que, nesse caso do exemplo, aparelhos com telas menores que 600px vejam uma imagem MENOR e de 600 pra cima, a imagem MAIOR seja carregada

![image-20241127131058886](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241127131058886.png)

![image-20241127131451575](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241127131451575.png)



**DICA¹**: usar max-widht e min-width faz com que o conteúdo da página fique mais responsivo, então se for uma tela grande, pequena, conforme ajuste da viewport, o conteúdo se ajusta automaticamente.

**DICA²**: se der um inspecionar e redimensionar a janela é possível ver que aparecem dois valores em pixels, que é a largura e a altura, respectivamente.

![image-20241127132047412](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241127132047412.png)



**Media Queries**

São regras CSS usadas para aplicar estilos diferentes com base nas características do dispositivo, como largura da tela. Serve para tornar o design responsivo, ajustando o layout para dispositivos como celulares, tablets e desktops. Isso garante que o site fique bem apresentado em diferentes tamanhos de tela.

[Responsive Viewer](https://chrome.google.com/webstore/detail/responsive-viewer/inmopeiepgfljkpkidclfgbgbmfcennb?_gl=1*1s57gx*_ga*MTEwMjE3ODAuMTcyODM5NjEwNA..*_ga_37GXT4VGQK*MTczMjcyNDAzMC42MS4xLjE3MzI3MjQwNDYuMC4wLjA.)



A estrutura de uma media querie é composta por 

@media (condição) { 

​	seletor {

​		propriedade: valor;

​	}

}

**media** = palavra-chave que inicia a media query

**condição** = define a regra (ex.: max-width: 768px)

**bloco de estilos**: declara os estilos que serão aplicados quando a condição for atendida

Podemos combinar condições com operadores como **and** ou **or** ([lembrando da aula do Gustavo Guanabara](https://www.cursoemvideo.com/curso/curso-de-algoritmo/aulas/algoritmo/modulos/operadores-logicos-e-relacionais/)) por exemplo: (min-width: 600px) **and** (max-width: 1024px)



Utilizando os mesmos códigos da aula anterior *(introdução a responsividade)*, vamos abrir uma estrutura de media querie e o ponto de quebra que vamos querer, nesse caso "max-widht: 576px" para dizer que telas **menores** que 576px, terão essa configuração.

![image-20241128131422260](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241128131422260.png)

Dentro da media querie vão os seletores que terão a regra anterior aplicada:

- Foi trocado o float right da nav do cabeçalho para float: none, para que remova a flutuação do menu e ele fique abaixo do logo

  ![image-20241128131002954](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241128131002954.png)

- Para que os links fiquem um abaixo do outro, alteramos as propriedades da nav li do cabeçalho para display: block

  ![image-20241128131034932](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241128131034932.png)

- Para colocar todos os itens alinhados ao centro (o que ficaria visualmente melhor), basta colocar um text-align: center na classe do cabeçalho como um todo

  ![image-20241128131125294](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241128131125294.png)



Existem outras diversas alterações que podem ser feitas com media queries, mas veremos mais ao longo do curso.

Aquela regra feita na aula anterior (em img, na tag picture), também é considerada uma media querie (breakpoint), é um tipo de responsividade utilizando media querie.



**OS MEDIA QUERIES TAMBÉM FUNCIONAM COM EFEITO CASCATA, então se, por exemplo, tiver um media querie com um background-color azul em cima e um background-color vermelho embaixo, o que vai valer é o vermelho que vem por último.**



Exemplos de tamanhos de media queries:

@media (max-width: 375px) { } // dispositivos extra pequenos

@media (max-width: 576px) { } // dispositivos pequenos (celulares em posição paisagem, menos de 768px)

@media (max-width: 768px) {  } // dispositivos médios (tablets, menos de 992px)

@media (max-width: 992px) {  } // dispositivos grandes (desktops, menos de 1200px)

@media (max-width: 1200px) {  } // dispositivos extra grandes (desktops grandes) // 1200px ou mais, não tem breakpoint



**Float**

É uma propriedade que faz o elemento flutuar, saindo do fluxo da página e podendo ir para a direita ou para a esquerda, ou ficando "none" que é o padrão (não vai flutuar nem pra direita e nem pra esquerda).

O float foi inventado para criar um texto em volta de uma imagem, como no post de um blog, e posicionar elementos na página, apesar de que a gente não use mais ele, ainda podemos nos deparar com isso. Hoje em dia é feito muito mais o uso do display flex e grid para posicionar elementos na página.



Nesse exemplo, colocaremos uma div com float: right e outra com float: left

![image-20241128145207511](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241128145207511.png)	![image-20241128145335371](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241128145335371.png)

Ao fazer isso e dar um inspecionar na página, podemos observar que a section está com altura **zero** e isso é problemático (nunca é bom que um elemento tenha altura zero, pois isso pode ocasionar erros no layout posteriormente)

![image-20241128145249753](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241128145249753.png)

Então foi inventado um hack para que essa section, e qualquer elemento pai que tenha elementos flutuando dentro dele, tenham uma altura definida. Com o float:after (":after" seria uma pseudo-classe), um content vazio, um display: block e um clear: both, com essas regras a tag section ficou com a altura de 100px, que é a mesma altura dos elementos filhos.

![image-20241128150109246](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241128150109246.png)	<img src="C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241128150125189.png" alt="image-20241128150125189" style="zoom:80%;" />



Exemplificando o float: none (no bloco 2), podemos ver que quando é dada essa propriedade no elemento, ele para de flutuar e perde o corpo. Basicamente, como o bloco 1 está flutuando e ele sai do fluxo normal da página, agora o bloco 2 está como se fosse por baixo dele.

![image-20241128151019778](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241128151019778.png)	<img src="C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241128151236736.png" alt="image-20241128151236736" style="zoom:80%;" />



Usando o float para o que ele realmente foi feito: criar textos em volta de uma imagem.

Criando uma tag section no html e inserindo uma imagem e um parágrafo nela, o comportamento padrão é de que fique a imagem acima e o texto abaixo.

![image-20241128153615039](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241128153615039.png)

![image-20241128153550401](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241128153550401.png)

Mas se estilizar a tag img no CSS, podemos ver como o texto engloba a imagem. Além disso foi dado uma altura e largura de 100px e um margin na direita de 15px. Essa é uma formatação comum de ser ver em jornais, revistas e blogs.

![image-20241128153632159](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241128153632159.png)	<img src="C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241128153644688.png" alt="image-20241128153644688" style="zoom:80%;" />

O texto fica englobando a imagem exatamente porque agora a imagem saiu do fluxo normal da página e agora está flutuando (nesse caso à esquerda).



**Centralizando Elementos *(sem display flex)***

Serve para alinhar elementos (como textos, imagens ou blocos) ao centro de um contêiner na página, melhorando o design e a usabilidade. Cria layouts mais organizados, garantindo que elementos fiquem alinhados visualmente de maneira harmoniosa.



Antes de iniciar a exemplificação, foi dado um reset.css e o body tem propriedades fixas:

​	![image-20241128162632022](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241128162632022.png)  ![image-20241129112718802](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241129112718802.png)  ![image-20241128163703267](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241128163703267.png)



E algumas classes também receberam alguns estilos previamente:

![image-20241129115519096](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241129115519096.png)



**Text-align/inline-height**

Criamos uma div com um texto dentro e estilizamos no CSS. Existe um macete para centralizar o texto dentro do quadrado criado. É necessário incluir as regras text-align: center e line-height: 250px (ou seja, o valor do line-height deve ser IGUAL ao valor de altura da div, então div > height: 250px = line-height: 250px)

​	![image-20241128163844279](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241128163844279.png)		![image-20241128163910768](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241128163910768.png)

A desvantagem do line-height é que o tamanho é fixo (tem que ser o mesmo tamanho do conteiner) e trabalhar com tamanhos fixos pode ser problemático.



**Position absolute *(transform %)***

Existe uma forma mais simples de fazer isso, que é usando o position absolute com valores em % e uma propriedade nova que é o "transform". Na prática, colocando a classe .texto-centralizado-2 com as propriedades de position: absolute e fazendo uso da % para ajustar a localização. 

![image-20241129115158864](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241129115158864.png)

*A propriedade transform está encurtada para que não fique repetitiva*

Nesse caso, colocamos um top de 50% (que é referente ao pai), mas ao fazer isso é possível observar que o elemento não fica bem alinhado ao meio do bloco, isso acontece porque ele moveu o topo do texto 50% para baixo, agora para centralizar, precisamos voltar a metade da altura desse conteúdo pra cima. Utilizando o transform: translateY(-50%)

<img src="C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241129113830013.png" alt="image-20241129113830013" style="zoom:80%;" />

Após feito isso, damos a propriedade left: 50% para que a imagem vá para o meio, porém não fica ajustada ao centro, sendo necessário dar mais um transform: translateX(-50%) (dessa vez é no eixo X - horizontalmente) e só aí então, o conteúdo ficará centralizado.

![image-20241129114912383](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241129114912383.png)



**Margin** ***(display block)***

Outra forma de movimentar um conteúdo dentro do container seria utilizando um margin: auto (que quer dizer basicamente que queremos dar uma margem automática para o elemento), porém ao dar esse comando, percebe-se que nada acontece, pois o botão tem display inline

![image-20241204161945675](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241204161945675.png)

![image-20241204161744642](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241204161744642.png)

Para resolver isso, teríamos que trocar o botão para display: block, fazendo isso o margin auto vai ser aplicado e o botão ficará no meio, ou seja, essa regra divide a proporção de espaço sobrando na esquerda e na direita e centraliza o elemento horizontalmente.

![image-20241204161806078](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241204161806078.png)



**Position Absolute**

Também há outra forma para fazer o alinhamento horizontal e vertical do elemento, que é com o position absolute (pois o elemento vem por padrão como estático e não consegue ser movimentado com as palavras-chaves de movimentação). O margin auto não funciona quando o position é absolute dessa forma.

![image-20241204162003762](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241204162003762.png)

![image-20241204162954938](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241204162954938.png)

É possível fazer um hack zerando todas as bordas (top, left, right, bottom = 0), então podemos ver que foi reconhecido e o elemento está centralizado. Isso acontece porque se zerar todos os valores, o margin auto passa a funcionar e consegue calcular a largura e altura sobrando.

<img src="C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241204163046804.png" alt="image-20241204163046804" style="zoom:80%;" />



**Text-align *(img)***

Colocando a propriedade de text-align: center na imagem, ela automaticamente vai para o centro, tanto horizontalmente, quanto verticalmente.

![image-20241206140835879](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241206140835879.png)

![image-20241206140938752](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241206140938752.png)

A imagem (img) é o elemento **filho** da div (que é **pai**) que tem a classe container-text-align. 

Se colocasse o text-align na imagem, ou seja, no elemento filho, não iria funcionar, mas no pai funciona. Qualquer elemento inline, inline block ou texto, dentro da div que está com o text-align vai funcionar esse tipo de alinhamento horizontal.



**Adicionando e customizando ícones com o Font Awesome *(copy link/tag e download/pasta)***

Ele é uma biblioteca que nos permite usar ícones como se fossem fontes. 

Permite adicionar ícones visuais (como ícones de redes sociais, setas, etc.) para melhorar a interface de usuário de forma prática e estilosa, podendo personalizar tamanho, cor e animações facilmente com CSS.

Antigamente, era necessário usar uma imagem utilizando a tag img, por isso essa biblioteca nos facilita. 



**Ícone como SVG:**

- É um elemento gráfico independente, personalizável diretamente no HTML com atributos como fill e stroke.
- Melhor para designs detalhados ou animações avançadas.
- É como uma "imagem desenhada" no código.
- Dá mais controle para mudar cores, formas e animações, direto no HTML.

**Ícone com tag \<i> (font awesome):**

- Representa um caractere de fonte estilizado com CSS.
- Mais fácil de usar e estilizar em projetos simples, mas menos flexível para animações ou ajustes avançados.
- Funciona como um texto estilizado, fácil de usar com classes.
- Bom para projetos simples, mas menos flexível para customizações complexas.



**Use SVG para designs avançados. **

**Use \<i> para rapidez e simplicidade.**



**Copy Link**

Primeiro vamos ao CDN Font Awesome copiar o link no formato de tag para colocar no corpo do html (que é um arquivo all.min.css)

OBS.: Nesses projetos de teste, está sendo utilizada a versão 5.15.4 do font awesome.

![image-20241206143432365](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241206143432365.png)

No html ele fica em um link maior do que o mostrado no site, pois está buscando diretamente do site do CDN, os outros atributos podem ser ignorados, isso vem automaticamente para fazer algumas verificações, o que nos importa é o HREF. NÃO PODE MEXER NO NOME DO ARQUIVO E ELE DEVE ESTAR DENTRO DO **HEAD**.

![image-20241206143942362](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241206143942362.png)



Além desse link .css, também vamos precisar do all.min.js, seguindo o mesmo procedimento anterior de copiar o link e colar no html. Isso é só para transformar os ícones em svg.

![image-20241206144409046](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241206144409046.png)

DEVE ESTAR NO **FINAL DO BODY**.

![image-20241206144434278](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241206144434278.png)



Fazendo isso, a biblioteca do font awesome já estará importada e pronta para ser utilizada no projeto.

Agora indo ao site do font awesome, basta utilizar a lupa para pesquisar qual ícone deseja, como por exemplo "instagram" e ele vai dar as opções disponíveis![image-20241206150055177](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241206150055177.png)

Escolhendo qualquer um dos ícones disponíveis e clicando em cima, vai abrir uma uma caixinha para poder copiar a tag i com o ícone para colocar no html. Se clicar em cima do texto, ele já é copiado. Feito isso, o ícone já estará disponível para colar na página.

![image-20241206151352875](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241206151352875.png)

<img src="C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241206151530320.png" alt="image-20241206151530320"  />	<img src="C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241206151541125.png" alt="image-20241206151541125" style="zoom: 67%;" />



Ao dar um inspecionar na página, podemos observar que o ícone ficou como svg, isso porque foi colocada o script de js no final do body.

<img src="C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241206151746070.png" alt="image-20241206151746070" style="zoom: 80%;" />	<img src="C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241206151812218.png" alt="image-20241206151812218" style="zoom:80%;" />



No exemplo em questão, utilizaremos o ícone do facebook. Então seguindo esse mesmo procedimento de pesquisar, copiar e colar a tag i no html, agora faremos a estilização no css. Dois estilos foram colocados:

1. Trocamos a cor do ícone para laranja (originalmente é preto); 
2. Acrescentamos a pseudo-classe :hover e ao passar por cima do ícone ele altera a cor para vermelho.



​			![image-20241206153507127](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241206153507127.png)	![image-20241206153541043](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241206153541043.png)

Várias outras propriedades podem ser dadas para o ícone, como font-size, por exemplo, para mexer no tamanho. Qualquer propriedade usada para modificar um texto, pode ser usada em um ícone, pois ele não deixa de ser um texto, ele é uma fonte.



**Download/Pasta**

Outra forma possível para fazer essa implementação do ícone no projeto é utilizando uma pasta (fazendo download), baixando ela do font awesome e colocando no projeto. O ponto positivo de fazer isso é que se der algum problema com o CDN (o link cair), o projeto também vai parar de funcionar. Então tendo a pasta dentro do próprio projeto, isso não vai acontecer. 

Porém, se ocorrer alguma atualização de coisas novas no font awesome e a versão que baixamos no nosso projeto não tem isso, teremos que baixar tudo de novo, nessa nova versão e colocar no projeto. Para projetos simples é tranquilo de utilizar, porém um site muito estruturado, com muitos ícones, não é indicado.



Indo no site do font awesome e clicando em "downloads for the web" (a opção à esquerda), será baixado um arquivo zip/war, basta só extrair o conteúdo dela para onde desejar.

![image-20241206155038656](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241206155038656.png)

Dentro da pasta terão diversos arquivos, mas nós só iremos precisar de alguns deles, que são: pasta css > all.min (agora é permitido alterar o nome do arquivo, se desejar) e pasta webfonts.



Na pasta da aula *(16-font-awesome)*, será criada uma nova pasta chamada "src" e dentro dessa pasta podemos colar os arquivos que baixamos e são importantes.

Feito isso, vamos fazer o link da pasta com o html/css. Dentro do head abrimos uma tag link e buscamos manualmente a pasta e o arquivo em questão.

![image-20241206160952557](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241206160952557.png)

Só isso não é suficiente para que a fonte funcione, pois dentro do font awesome ele busca uma pasta que se chama "webfonts". Então deve-se voltar ao arquivo zip baixado, copiar essa pasta "webfonts" inteira e colar dentro da pasta src.

![image-20241206161401438](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241206161401438.png)

Agora sim está pronto para uso. Lembrando que, em caso de atualizações, é necessário baixar e refazer o processo todo novamente.

**NÃO PODE RENOMEAR A PASTA "WEBFONTS"**



**IMPORTANTE: Para o funcionamento da biblioteca corretamente é necessário que siga a versão dos links que estão abaixo.** 

Link usado na aula: [CDN Font Awesome](https://cdnjs.com/libraries/font-awesome/5.15.4?_gl=1*14iz9c2*_ga*MTEwMjE3ODAuMTcyODM5NjEwNA..*_ga_37GXT4VGQK*MTczMzUwNTE4NC42Ni4xLjE3MzM1MDUyMDEuMC4wLjA.)

[Site Font Awesome](https://fontawesome.com/v5/search?_gl=1*14iz9c2*_ga*MTEwMjE3ODAuMTcyODM5NjEwNA..*_ga_37GXT4VGQK*MTczMzUwNTE4NC42Ni4xLjE3MzM1MDUyMDEuMC4wLjA.)

