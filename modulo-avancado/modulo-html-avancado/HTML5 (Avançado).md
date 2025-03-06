# HTML5 (Avançado) :book:

:link: Notion: https://glowing-scilla-18d.notion.site/N-vel-AVAN-ADO-157bf6c7b63d80048f43fbe4718bb3fd?pvs=74



**Imagens responsivas usando a Tag Picture**

Ela é uma tag relativamente nova no HTML, vimos pela primeira vez no módulo de CSS na parte de responsividade, agora vamos nos aprofundar uma pouco mais sobre.

É um elemento HTML usado para definir diferentes versões de uma imagem para serem exibidas dependendo do tamanho da tela ou das condições do dispositivo.

Torna imagens responsivas, otimizando o carregamento e a exibição para melhorar o desempenho e a experiência do usuário em dispositivos variados (desktop, tablet, celular).

A desvantagem da tag picture é que pode deixar o código muito verboso.



**Método mobile first (prioriza dispositivos móveis)** 

No método mobile-first, as imagens responsivas com a tag picture priorizam carregar uma versão otimizada para dispositivos móveis primeiro, ajustando-se a telas maiores quando necessário.

Melhora o desempenho em dispositivos móveis, carregando imagens leves por padrão e trocando por versões maiores em telas maiores, economizando dados e tempo de carregamento.

![image-20241210151746002](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241210151746002.png)

A estrutura começa com a tag picture e depois uma tag source. 

O primeiro atributo da source é o media, que nos serve para definir em qual ponto do media querie será mostrado/carregada a imagem que definirmos. No exemplo temos min-width para sinalizar que naquela quantidade de pixels ou maior será exibida a imagem *"x"* (mid-width: 465px = tela de 465px ou MAIS terá aquela configuração de exibição)

O segundo atributo será o srcset que é o caminho/site da imagem que vamos utilizar.

A tag img é onde iremos definir a imagem menor.

![image-20241210152331116](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241210152331116.png)

*Nos exemplos de telas temos em primeiro a exibição da imagem 300x300, seguida pela imagem de 500x500 e por último uma 1200x1200.*



**Método desktop first (prioriza desktops)**

No método desktop-first, as imagens responsivas com a tag picture são carregadas para telas maiores (como desktops) primeiro, e versões menores são carregadas conforme a tela diminui. 

Permite otimizar o desempenho em telas grandes, carregando imagens de alta resolução por padrão e ajustando para versões menores em dispositivos móveis, garantindo um carregamento eficiente e uma boa experiência visual em diferentes dispositivos.

![image-20241210155333139](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241210155333139.png)

Ao contrário do que fizemos no mobile first, no desktop first vamos iniciar alterando o valor da media para "max-width" e ele dará prioridade para carregar as imagens deixando-as maiores até que o tamanho da tela diminua e fique menor do que o tamanho máximo, por exemplo, se o max-width está 768px, enquanto a tela não chegar nesse valor ou menos, a imagem não mudará para uma resolução menor, ou seja, ainda que fique com scroll dos lados e a imagem corte, ela não mudará para uma menor.

![image-20241210155405574](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241210155405574.png)

*Tela com 769px (o limite de max-width) e a imagem "cortada", com scroll, em tamanho 1200x1200*

![image-20241210155444127](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241210155444127.png)

*Tela com 768px (abaixo do limite de max-width) e a imagem reformatada para caber na tela, sem scroll, em tamanho 500x500*



**Quando usar max-width e min-width? (diferenças)**

- **max-width**: Significa que a condição se aplica **até** um determinado valor de largura de tela. Ou seja, a imagem X será carregada para telas **com largura igual ou menor** do que o valor definido.
  - Exemplo: (max-width: 768px) significa que a imagem será exibida para telas de até **768px de largura**, ou seja, para dispositivos móveis ou tablets pequenos.
- **min-width**: Significa que a condição se aplica **a partir de** um determinado valor de largura de tela. Ou seja, a imagem X será carregada para telas **com largura igual ou maior** do que o valor definido.
  - Exemplo: (min-width: 768px) significa que a imagem será exibida para telas **com 768px de largura ou mais**, ou seja, para tablets maiores, laptops e desktops.



Em resumo:

- **max-width** → Aplica-se a telas **menores ou iguais** ao valor.
- **min-width** → Aplica-se a telas **maiores ou iguais** ao valor.

Isso ajuda a carregar imagens otimizadas dependendo do tamanho da tela do usuário, economizando recursos e melhorando o desempenho.



**Criando um ícone de Favicon**

O favicon (ou ícone de favorito) é a pequena imagem que aparece ao lado do título da página no navegador, nas abas do navegador e nos favoritos.

Serve para melhorar a experiência do usuário, criando uma identidade visual para o site e tornando-o facilmente identificável nas abas ou nos favoritos do navegador. É inserido no HTML através da tag link.

![image-20241210162200823](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241210162200823.png)

*Cada uma dessas imagens ao lado dos nomes nas abas, são favicons.*



**Como criar um favicon de uma imagem de um logo**

Primeiramente vamos ao site [favicon.io](https://favicon.io/) que transforma imagens png para o formato .ico (de ícone), que é o formato que os favicons utilizam.

<img src="C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241210163130078.png" alt="image-20241210163130078" style="zoom:67%;" />



Assim que clicado, a próxima tela já trará um drag & drop onde vc pode soltar ou carregar seu arquivo de imagem ali para virar um ícone. Assim que o fizer, clique em "download"

![image-20241210163642498](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241210163642498.png)



O arquivo baixado será um zip/rar, basta extrair os arquivos onde desejar. Dentre esses arquivos, estarão várias imagens, vamos escolher a que for "favicon.ico", copiar e colar na pasta do projeto (criar uma pasta separada para imagens).

![image-20241210164056075](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241210164056075.png)	<img src="C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241210164126856.png" alt="image-20241210164126856" style="zoom: 67%;" />

*dev-quest/modulo-avancado/modulo-html-avancado/02-favicon/images*

![image-20241210164444391](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241210164444391.png)	*imagem ícone já é reconhecida pelo vs code*



A tag para criar o favicon deve vir **DENTRO DO HEAD**. Escrevendo "link:fav" o vs code já irá sugerir a abreviação. É necessário trocar o href para o caminho onde o favicon realmente se encontra.

![image-20241210170219824](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241210170219824.png)

![image-20241210165950538](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241210165950538.png)	ANTES

![image-20241210170053847](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241210170053847.png)	DEPOIS

Os tamanhos mais comuns de favicons são 32x32 ou 16x16 (formatos quadrados).

Pode ter fundo transparente (png) ou pode ter fundo preenchido também (jpg).



**Criando emojis**

A criação de emojis com entidades HTML utiliza códigos especiais para representar caracteres universais, como emojis, em páginas web. Permite adicionar emojis de forma consistente, garantindo compatibilidade com diferentes navegadores e dispositivos, mesmo que não suportem diretamente o caractere.

Para chamar uma entidade inicia-se com "&" seguido do nome do decimal ou hexadecimal e finaliza com um ; (ponto e vírgula)

Por exemplo, para escrever o copyright, escreve-se "\&copy;" e fica o símbolo &copy;

<img src="C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241210171653356.png" alt="image-20241210171653356" style="zoom:80%;" />

Caso já tenha o símbolo, é possível apenas copiar e colar ele no html/vs code, que irá funcionar, não sendo necessário chamar a entidade.

<img src="C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241210171834829.png" alt="image-20241210171834829" style="zoom: 67%;" />

Mas é bom saber escrever caso precise ou não tenho à mão o símbolo (também pode acontecer de um arquivo html vir escrito assim).

Uma entidade muito utilizada é o espaço *(barra de espaço/espaçar o texto)*, que é representado pela escrita "\&nbsp;". Se dermos vários espaços com o teclado no html, ele não vai entender e o texto continuará junto, para espaçar mais vezes utiliza-se essa entidade.

<img src="C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241210172239718.png" alt="image-20241210172239718" style="zoom: 80%;" />

*O html/navegador é capaz de renderizar e o "\&nbsp;" não vai aparecer para o usuário final.*



Também é possível colocar acentuação nas letras através das mesmas entidades. Por exemplo o "a" com acento agudo ficaria "\&aacute;", um "a" com acento til seria "\&atilde;"

![image-20241210173423204](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241210173423204.png)

Existe uma outra infinidade de entidades para escritas, como letras gregas, operações matemáticas e lógicas, todas estão no site do [DevMedia](https://www.devmedia.com.br/html-entities-html-symbols-html-characters/1011?_gl=1*yl90so*_ga*MTEwMjE3ODAuMTcyODM5NjEwNA..*_ga_37GXT4VGQK*MTczMzg2MDk1NC43MS4xLjE3MzM4NjExMTguMC4wLjA.).



Para escrever emojis a escrita da entidade fica sempre "\&#" seguido de um número que corresponde àquele emoji. Um coração, por exemplo, corresponde a entidade "\&#128151;", dentre outros. Há uma lista completa de emojis no [W3Schools](https://www.w3schools.com/charsets/ref_emoji.asp?_gl=1*1xa03m7*_ga*MTEwMjE3ODAuMTcyODM5NjEwNA..*_ga_37GXT4VGQK*MTczMzg2MDk1NC43MS4xLjE3MzM4NjExMTguMC4wLjA.).

![image-20241210174105916](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241210174105916.png)



**Adicionando áudio nas suas páginas**

É usada para incorporar áudio em uma página web. Permite reproduzir arquivos de áudio diretamente no navegador, com suporte a controles como play, pause e volume, sem a necessidade de plugins externos.

Para usar a tag audio basta escrever audio (ela tem abertura e fechamento), dar um atributo src (que vai ser o caminho onde está esse áudio) e um atributo controls *(SEM ESSE ATRIBUTO NÃO VAI APARECER NADA NO NAVEGADOR)* que habilita todos os botões referentes ao áudio (play, pular, volume etc).

![image-20241210175826672](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241210175826672.png)

Também é possível colocar um outro atributo chamado "autoplay" para que, assim que a página for iniciada, automaticamente o áudio comece a tocar, porém no google chrome isso não é permitido em tags de áudio, então se quiser usar autoplay de áudio na sua página, terá que usar alguma biblioteca de javascript para isso.



Outro atributo importante da tag audio é o preload, onde temos 3 valores para escolher, sendo auto, metadata ou none.

![image-20241210181824953](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241210181824953.png)

- "**Auto**" é o valor padrão (default), então se não colocar o atributo de preload, por padrão ele será auto. O problema dele é que, sempre que a página for aberta, o áudio será baixado pelo usuário, ou seja, independente se a pessoa que estiver navegando pelo site clicar para iniciar o áudio ou não, ele será baixado e gastará banda/internet do usuário desnecessariamente.

- "**Metadata**" serve para carregar algumas informações do áudio apenas, e não ele todo. Então, por exemplo, ao abrir o site, ele carrega apenas metade do áudio (é semelhante ao uso do youtube).

  ![image-20241210182026793](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241210182026793.png)

- "**None**" não vai carregar absolutamente nada do áudio. As informações serão baixadas apenas e somente se o usuário der play no botão. O único problema dessa versão é que pode haver um delay, dependendo do tamanho do áudio, se for muito grande, terá o tempo de espera entre baixar o áudio e começar a tocar.

  ![image-20241210182045994](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241210182045994.png)



Temos 3 tipos de extensões de áudio e cada navegador vai poder aceitar ou não, sendo elas o .mp3, .ogg e .wav, o Safari, por exemplo, não aceita extensão .ogg, então ele não dá suporte a ela e dessa forma os áudios que vierem nesse formato, não serão reproduzidos.

Na tag audio podemos fazer algo que permita que o navegador procure por diferentes extensões de áudio e comece a tocar a que ele realmente dá suporte. É sempre bom que tenhamos essas 3 extensões e use esse fallback para que não dê problema.

Vamos abrir uma tag audio, seguida da propriedade controls e dentro dessa tag audio, abriremos uma tag source, com a propriedade src, contendo o caminho de onde se encontra o arquivo mp3 e um type que vai ser o tipo do formato mp3. Esse mesmo passo-a-passo deve ser feito para cada um dos tipos de áudios.

![image-20241210184533588](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241210184533588.png)

Também podemos escrever um parágrafo para que, caso o navegador que a pessoa estiver acessando seja uma versão mais antiga e não dê suporte a uma tag de audio, ela consiga visualizar *(pode até ser colocada uma tag a com um link para o download de uma versão mais recente, por exemplo)*. Feito isso, o navegador vai tentar carregar os áudios de cima para baixo, se o ogg não funcionar, ele vai tentar o mp3 e assim por diante.



Site para converter arquivo mp3 para outros formatos (ogg, wav etc): [Convertio.co](https://convertio.co/pt/?_gl=1*5zqk1i*_ga*MTEwMjE3ODAuMTcyODM5NjEwNA..*_ga_37GXT4VGQK*MTczMzg2NjU0My43My4xLjE3MzM4NjY1NjkuMC4wLjA.)



**IMPORTANTE: sempre que for colocar qualquer áudio no site, certifique-se de ele tenha uma licença gratuita e, ainda assim, mesmo que seja liberado, o autor do áudio pode pedir para que dê os devidos créditos a ele (isso acontece com vídeos, imagens e áudios).**



**Adicionando vídeos às páginas com a tag video**

A tag video é usada para incorporar vídeos diretamente em páginas web. Permite reproduzir vídeos no navegador sem a necessidade de plugins externos, com opções de controles como play, pause e volume.

Sites para baixar videos e usar no site:

[Story Blocks](https://www.storyblocks.com/video?_gl=1*1o3nepb*_ga*MTEwMjE3ODAuMTcyODM5NjEwNA..*_ga_37GXT4VGQK*MTczMzg2NjU0My43My4xLjE3MzM4NjcyNTcuMC4wLjA.) (necessário se cadastrar para poder baixar os vídeos)

[Pexels](https://www.storyblocks.com/video?_gl=1*1o3nepb*_ga*MTEwMjE3ODAuMTcyODM5NjEwNA..*_ga_37GXT4VGQK*MTczMzg2NjU0My43My4xLjE3MzM4NjcyNTcuMC4wLjA.) (não é necessário cadastro)

[Convertio](https://convertio.co/pt/?_gl=1*c8vlev*_ga*MTEwMjE3ODAuMTcyODM5NjEwNA..*_ga_37GXT4VGQK*MTczMzkzMzgyNi43NC4xLjE3MzM5MzM4NTYuMC4wLjA.) (também serve para converter vídeos)

**Lembrando sempre de se atentar aos direitos autorais dos vídeos, ainda que sejam gratuitos.**



**Parte 1**

Para usar, basta abrir a tag video (que tem abertura e fechamento) e passar atributos a ela, o primeiro será o src (com o caminho para o vídeo), podemos diminuir a largura do vídeo com um width e também a altura com o height *(o ideal é deixar apenas o width)*.

![image-20241211125557336](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241211125557336.png)

Lembrando que, dessa forma, o vídeo ficará centralizado, para não perder qualidade, então, por exemplo, se der 300px de altura, a tag video terá esses 300px de altura, mas o vídeo em si ficará centralizado e não esticado.

<img src="C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241211125636173.png" alt="image-20241211125636173" style="zoom:80%;" />

Esses estilos também podem ser aplicados no CSS, inclusive se quiser colocar valores variáveis, como %.

Se colocar somente um width de 200px, por exemplo, ele já colocará a altura proporcional a largura, que, nesse caso foi de 112.5px. Essa é a forma ideal de se fazer.

![image-20241211130002869](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241211130002869.png)

<img src="C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241211130017575.png" alt="image-20241211130017575" style="zoom:80%;" />

Outro atributo que deve ser colocado é o controls, que funciona praticamente da mesma forma da tag audio ensinada anteriormente (permitindo dar play, pausar, aumentar tela etc).

<img src="C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241211131031894.png" alt="image-20241211131031894" style="zoom:80%;" />

Para que o vídeo seja reproduzido automaticamente ao abrir o site, é necessário dar o atributo autoplay e, no caso do Google Chrome, por exemplo, também é necessário dar o atributo muted (sem esse, o vídeo não rodará sozinho). 

Geralmente o autoplay muted é utilizado em sites que tem painéis com vídeos tocando atrás, em looping. Para que o vídeo fique tocando em looping, sem parar, é necessário dar o atributo loop.

![image-20241211131111823](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241211131111823.png)



Para colocar uma thumb *(imagem de entrada antes de dar play no vídeo, assim como é no youtube)*, usamos o atributo poster, seguido do caminho para a imagem. **Lembrando que é necessário desabilitar o autoplay muted para que o poster funcione!**

![image-20241211131543725](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241211131543725.png)

<img src="C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241211131557202.png" alt="image-20241211131557202" style="zoom:80%;" />



**Parte 2**

Continuando a aula anterior, nessa aula vamos mostrar os tipos de extensões dos arquivos de vídeos e como cada navegador se comporta com elas. 

E também explicar os prós e contras de usar a tag video no site e uma alternativa se quisermos utilizar a tag da forma original.

Diferentes tipos dos formatos de vídeos aceitos pela tag video:

![img](https://cdn.areademembros.com/files/instancia_3760/editor/ZHDfgkMElc3TfIhcfB0zPmiqMu9jr5MiL5CT7Pxy.jpg)



Semelhante ao passo a passo da aula sobre tag de áudio, para fazer com que cada usuário consiga ter acesso àquele vídeo, em formatos diferentes *(fallback)*, basta abrir outra tag video (com controls e width, dentro dela abrir uma tag source com um src (caminho) e um type (video/mp4, ogg ou webm).

Também podemos incluir um parágrafo indicando que o navegador não tem suporte a tag, caso o usuário esteja utilizando uma versão mais antiga.

![image-20241211133412864](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241211133412864.png)

*Dentro do .ogg, podem existir outros tipos de extensões, como o .ogv e o .ogm*



Assim como no audio, para converter os vídeos em outro formato, basta utilizar o site do Convertio (após baixado, basta colocar os arquivos em novo formato na pasta correspondente do projeto).

![image-20241211133822386](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241211133822386.png)

![image-20241211134025777](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241211134025777.png)



**Prós e Contras**

**Vantagens** da tag video (hospedando você mesmo, arquivo na pasta do projeto):

- Controle total: Você gerencia o vídeo, sem depender de plataformas externas.
- Personalização: É possível customizar a aparência e o comportamento.
- Sem anúncios ou branding: Não há marcas ou anúncios de terceiros.



**Desvantagens:**

- Custo alto: Hospedagem e largura de banda podem ser caros para vídeos grandes ou com muito tráfego.
- Manutenção: Você é responsável por compressão, compatibilidade e desempenho.
- Carregamento lento: Pode impactar o desempenho do site se não for otimizado.



**Alternativa:**

- Use plataformas como YouTube ou Vimeo, incorporando o vídeo no site via embed.
  - **Vantagem:** Reduz custos e garante performance (streaming otimizado).
  - **Desvantagem:** Exibe branding e pode incluir anúncios, dependendo da plataforma.



**Iframes**

É uma tag HTML usada para incorporar uma página web dentro de outra, criando uma janela ou frame *(vem de quadro)* que exibe conteúdo externo. Permite inserir conteúdos de outros sites, como vídeos, mapas ou formulários, sem sair da página atual.

Para utilizar, basta criar uma tag iframe (que possui abertura e fechamento), o primeiro atributo a ser passado será um src (que será "*embedado*", podendo ser uma página html dentro do próprio projeto, ou um site externo).



**Página Interna (HTML dentro do projeto)**

Nesse primeiro exemplo, vamos fazer como se fosse uma outra página (html) dentro do projeto. Então no src virá o caminho para essa outra página interna.

​		![image-20241211135822998](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241211135822998.png)			![image-20241211135948157](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241211135948157.png)

<img src="C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241211140016592.png" alt="image-20241211140016592" style="zoom:67%;" />	<img src="C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241211142159449.png" alt="image-20241211142159449" style="zoom:50%;" />

*Na esquerda com frameborder auto (com borda) e na direita com frameborder 0 (sem borda)*

*Também podemos definir outros atributos para a tag, como width, height.*



**Página Externa**

Basicamente é como os exemplos que vimos nas aulas passadas do embed do youtube. Nesse caso, basta ir ao site do youtube, clicar para compartilhar o vídeo e clicar em "incorporar", dessa forma, o próprio youtube vai gerar uma tag de iframe para copiar e colar no html (vc ainda pode escolher se quer que o vídeo comece em determinado minuto, se deseja mostrar os controles do players).

<img src="C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241211141326189.png" alt="image-20241211141326189" style="zoom:80%;" />	<img src="C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241211141343966.png" alt="image-20241211141343966" style="zoom: 67%;" />

<img src="C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241211141424591.png" alt="image-20241211141424591" style="zoom:67%;" />	<img src="C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241211142839928.png" alt="image-20241211142839928" style="zoom:67%;" />

![image-20241211141924131](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241211141924131.png)

width = largura (pode ser ajustado pelo css)

height = altura (pode ser ajustada pelo css)

src/source = caminho (link para o youtube)

title = titulo do iframe (já vem assim do youtube)

frameborder = está tirando toda e qualquer borda do iframe

allow = para permitir algumas coisas que o iframe pode fazer (coisas específicas do próprio youtube)

allowfullscreen = vai dizer se pode ou não usar o iframe com a tela inteira
