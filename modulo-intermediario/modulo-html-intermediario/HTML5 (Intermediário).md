# HTML5 (Intermediário) :book:

:link: Notion: https://glowing-scilla-18d.notion.site/HTML5-Intermedi-rio-132bf6c7b63d810a8563d4b274d6184e

Nesse módulo veremos tags importantes e aprofundaremos na semântica.

[Link do W3S com a lista de inputs](https://www.w3schools.com/tags/tag_input.asp?_gl=1*1qd7sj3*_ga*MTEwMjE3ODAuMTcyODM5NjEwNA..*_ga_37GXT4VGQK*MTczMjIwODQzMi4zOS4xLjE3MzIyMDg0MzIuMC4wLjA.)



**Tag input TEXT**

Para escrever uma tag de input, primeiro precisamos abrir a tag "<input...>" e dizer qual é o tipo (que pode ser vários), mas nesse caso queremos o text, então ficaria \<input type="text">.

As tags de input também podem ser escritas sem fechamento (assim como a tag "img", por exemplo).

Ao fazer a inclusão dela e dar um alt + o, podemos observar que é criada uma caixinha para escrever um texto. Quando isso estiver dentro de um formulário e for preenchido e enviado (*submit*), os dados então serão recebidos por um servidor, uma página php etc.

![image-20241107163941907](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241107163941907.png)

O padrão do input é text, então se deixar apenas \<input> ele ainda reconhecerá como text, sem a necessidade de escrever *type="text"*. PORÉM, se for utilizar outro tipo de input, deve-se sempre fazer a alteração do tipo.



**Atributo NAME**

O atributo "name" dentro da tag de input é muito importante para poder distinguir os campos de input text que tem no formulário.

É com essa tag name que poderemos pegar depois qual foi o texto enviado para o back ou front end e tratar os dados que vem dentro dele.

É interessante observar que, ao colocar o atributo "name", caso vc já tenha preenchido algum formulário com o valor que está sendo requerido, automaticamente o navegador já te dá opções para preenchimento automático. Por exemplo, ao colocar \<input *type*="text" *name*="nome"> o navegador reconhece os nomes que vc já colocou em outros formulários anteriores e te dá opções para auto completar.

![image-20241121132504656](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241121132504656.png)

O mesmo acontece com atributos de email, senha etc.



**Atributo VALUE**

Outro atributo que podemos dar ao input é "value", que basicamente é o valor desse campo, então seria um padrão já preenchido que viria na página. Por exemplo, se vc deixar o value="Letícia" ao abrir o site, o campo de nome já estaria preenchido como Letícia. 

É importante lembrar que, mesmo colocando um padrão no value para vir preenchido, caso o usuário altere o texto no input, o que vai valer é o que o usuário escreveu, e nao o padrão do html, ou seja, se está como padrão vir escrito LETÍCIA, mas o usuário trocar para MARIA, o que vai valer é o MARIA.

![image-20241121133742985](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241121133742985.png)



Também podemos dar o atributo "id" que vai ser um identificador para esse campo. Isso é muito importante pra quando formos criar um *label* para esses valores. 

![image-20241121134414471](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241121134414471.png)

*O valor do id e do name podem ser os mesmos.*

A **diferença do atributo NAME para o ID** é que o ID serve pra identificar de maneira única um atributo, ou seja, ele só pode ser utilizado em um elemento por vez, já o NAME serve para identificar o dado que será enviado.



**Atributo PLACEHOLDER**

Um outro atributo importante para o text é o "placeholder", que será um texto que aparecerá no campo a ser preenchido, como se fosse uma "instrução" ao que se deve fazer/escrever ali. Não é um texto de fato, ele é apenas um placeholder informativo, uma marcação.

![image-20241121134915022](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241121134915022.png)

É importante se atentar que, caso a tag esteja com o atributo *value* preenchido com algo, mesmo colocando um *placeholder*, não aparecerá nenhuma marcação informativa (*pois o campo já está padronizado para vir preenchido*), então é necessário deixar sem o *value* no input OU o placeholder aparecerá somente caso o usuário apague o texto padrão do *value*.



Podemos usar o vs code para criar as tags de input de forma rápida, ao escrever "*input:*" ele já vai sugerir as opções com alguns atributos devidamente escritos, faltando apenas preencher. 

![image-20241121135649756](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241121135649756.png)

![image-20241121135727158](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241121135727158.png)



**O que é LABEL**

O elemento *label* no html é usado para associar um rótulo a um elemento de formulário (para qual propósito é aquele campo no formulário), como um *input*. Ele melhora a acessibilidade, permitindo que o usuário clique no rótulo para focar no campo associado. A associação é feita pelo atributo "*for*", que **deve ter o mesmo valor do atributo id** do campo.

Ele é exibido na página ao lado ou acima do campo e melhora tanto a usabilidade quanto a acessibilidade.

![image-20241121143834373](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241121143834373.png)

*É bem legal para campos com checkbox/radio, que veremos um pouco mais a frente.*



**Input NUMBER**

Ele é bem parecido com o input text, porém nesse poderemos digitar apenas números.

Para começar, abrimos a tag <input...> como anteriormente, porém agora o tipo será NUMBER, ficando então \<input type="number">

Percebe-se que vai aparecer um campo para preenchimento no site, porém ele não permite que sejam digitadas letras, apenas numerais e/ou também utilizar as setinhas para cima e para baixo que aparecem na lateral direita do campo.

![image-20241121140959475](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241121140959475.png)



**Input PASSWORD**

Como o nome já diz, é um campo para colocar a senha e ele é bom pois esconde o que está sendo digitando, mantendo o sigilo dela. É sempre importante se lembrar de colocar ele quando tratamos de dados sensíveis.

![image-20241121144147020](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241121144147020.png)

![image-20241121144202356](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241121144202356.png)



**Input SUBMIT**

Vai criar um botão no formulário para que seja feito o envio *(submit)* dos dados para um servidor/backend, por exemplo. Para poder funcionar, esse input **precisa estar DENTRO da tag \<form> \</form>** *(que é uma tag que será utilizada para criar um formulário, que veremos posteriomente)*, senão não será possível enviar os dados.

Então basta criar a tag de input do tipo submit que ela já aparecerá na tela. Por padrão,  ela já vem escrita como "ENVIAR", mas podemos alterar isso colocando um atributo value diferente, como por exemplo *value="Salvar"*.

![image-20241121145124766](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241121145124766.png)



**Input CHECKBOX**

Checkbox é aquela caixinha dos formulários que fica disponível para marcar e desmarcar a opção. Como exemplo, faremos um formulário para marcar as linguagens que conhecemos. Para que fique melhor, é interessante utilizar um *label* para cada linguagem, pois, desta forma, o texto ficará "ligado" a checkbox.

Um comparativo:

**SEM LABEL**

![image-20241121150527563](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241121150527563.png)

![image-20241121150427621](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241121150427621.png)

Ao clicar com o mouse só no texto da linguagem, o html não reconhece como se vc estivesse querendo selecionar/marcar aquele campo. Sem o label só é possível marcar a caixinha quando, de fato, clicar nela.



**COM LABEL**

![image-20241121151218775](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241121151218775.png)

![image-20241121151250132](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241121151250132.png)

Com o label é possível clicar tanto na própria checkbox quanto no texto para selecionar a caixa.

É importante lembrar que para utilizar o label o atributo FOR deve ter o mesmo valor que o ID do input. Como nesse exemplo: for="C#" e id="C#".

O texto em questão também precisa ser escrito entre a tag label, do contrário, ao clicar no texto não será reconhecido que deseja marcar a caixinha (ficando, assim, igual ao input sem label).



CADA "FOR" E "ID" DEVEM TER VALORES **DIFERENTES**, DO CONTRÁRIO, AO CLICAR EM UMA CAIXINHA QUE TENHA UM *FOR* IGUAL AO DE OUTRO LABEL, ISSO FARÁ COM QUE A CAIXINHA ERRADA FIQUE MARCADA. Por exemplo, deixando o label com o for="C#" igual ao anterior, quando clicar em "JavaScript" a caixinha do C# será marcada.

![image-20241121152530326](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241121152530326.png)

![image-20241121152637492](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241121152637492.png)



**Atributo CHECKED**

É semelhante ao atributo *value*, ou seja, ele faz com que a checkbox já venha marcada por padrão, então toda vez que recarregar a página, essa caixinha já estará selecionada.

![image-20241121153814955](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241121153814955.png)



Uma particularidade importante do *checkbox* e do *radio* é que o atributo *name* precisa ser **igual** nos inputs, ou seja, seguindo o exemplo, não terá um name com valor C#, outro com JavaScript etc, o name utilizado em todos seria "linguagens".



**Input RADIO**

Ao contrário da checkbox, além da mudança estética *(checkbox é um quadrado e radio é uma bolinha)*, no radio não é possível desmarcar a opção após selecionar e só é possível selecionar um radio por vez.

![image-20241121155125354](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241121155125354.png)

*Observa-se que o name deve ser o mesmo nas duas tags, caso tenham name's diferentes isso significa que eles estariam em grupos diferentes, ou seja, seria possível marcar mais de uma bolinha no formulário.*



No radio o **atributo CHECKED** também é utilizado exatamente da mesma forma *(dentro da tag de input)* caso queira que uma bolinha venha selecionada.



DICA: é possível utilizar a tag input DENTRO da tag label. Isso facilita a usabilidade e pode ficar esteticamente mais interessante.

![image-20241121155829898](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241121155829898.png)

![image-20241121155841710](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241121155841710.png)



**Tag SELECT**

Serve basicamente para selecionar um ou mais valores para mandar para o servidor do backend ou qualquer outro lugar dentro do nosso formulário.

A tag select deve ter abertura e fechamento. Ela cria um menu suspenso *(dropdown)* para o usuário escolher uma entre várias opções. As opções dentro do menu são definidas com a tag "option".

Dentro da *tag option* tem um atributo muito importante, que é o VALUE, que vai definir qual é o valor da option.

![image-20241121161118856](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241121161118856.png)

Uma coisa bem importante é que, quando for feito o submit da opção selecionada , o que vai ser enviado para o servidor é o que está **dentro do VALUE** e não o texto entre o fechamento e abertura da tag. *Ou seja, se dentro do value está "Senhor dos Anéis" e no texto da tag está "Harry Potter", quando for enviado, o servidor receberá senhor dos anéis e não harry potter.*

![image-20241121161225398](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241121161225398.png)

Para que o option não fique com um filme pré-selecionado devemos criar um option com value vazio e dentro da tag escrever "Selecione um filme". 

![image-20241121161919363](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241121161919363.png)

*Ou seja, nesse caso de exemplo, sempre está marcado "Senhor dos Anéis" como padrão, mas como queremos que o usuário marque uma opção, então devemos criar essa outra tag de option. Posteriormente veremos como deixá-la tag inválida.*



Para fazer com que uma outra opção fica selecionada como padrão quando a página for (re)carregada, basta colocar o atributo "selected" no option que desejar.

![image-20241121165307585](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241121165307585.png)



Também é possível deixar o usuário marcar múltiplas opções, basta colocar o atributo "multiple" na tag select.

*Para selecionar vários é necessário segurar a tecla CONTROL no teclado e ir clicando nas outras opções.*

![image-20241121165416839](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241121165416839.png)



**Tag TEXTAREA**

Diferente do input text, ela é utilizada sempre que queremos que o usuário insira um texto GRANDE, onde haverá quebra de linha, parágrafos etc.

![image-20241121170008025](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241121170008025.png)

![image-20241121170017773](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241121170017773.png)

No *textarea* podemos colocar os atributos de colunas e linhas para demarcar qual tamanho que ele terá por padrão.

**COLS** = colunas

**ROWS** = linhas

![image-20241121194032285](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241121194032285.png)

*Também é possível deixar um texto pré escrito como padrão no textarea, mas, assim como já dito anteriormente, o que é realmente válido será o que o usuário digitar no campo, então se ele apagar o texto e escrever qualquer outra coisa, o texto padrão do html não terá mais valor.*



**Tag BUTTON *(e input type button)***

Para criar um button basta abrir a tag \<button> \</button> e ele já será criado na página, porém sem nada escrito, sendo necessário colocar um texto entre a abertura e fechamento da tag.

![image-20241121195757148](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241121195757148.png)

![image-20241121195829677](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241121195829677.png)

O button serve para criar um **elemento clicável** na tela, que pode servir para fazer várias coisas, como por exemplo ao clicar no botão aparece um aviso na tela ou acontecer uma animação etc.

[Link do botão usando a tag button no W3Schools](https://www.w3schools.com/tags/tryit.asp?filename=tryhtml_button_test&_gl=1*1v9wrnk*_ga*MTEwMjE3ODAuMTcyODM5NjEwNA..*_ga_37GXT4VGQK*MTczMjIyODg3MC40My4xLjE3MzIyMjk1MDguMC4wLjA.)



**Tag INPUT TYPE BUTTON**

Ao invés de abrir uma tag dedicada para o button, também é possível abrir uma tag de input e colocar o tipo como button. Fazendo dessa forma, também será necessário atribuir um value, que será o que virá escrito no botão.

![image-20241121200621780](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241121200621780.png)

Usando como exemplo o mesmo botão do W3S, também iremos atribuir um onclick="alert('Olá')" para aparecer uma mensagem na tela ao clicar no botão.

![image-20241121200708610](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241121200708610.png)



**Quando usar button e quando usar input type button?**

É mais indicado utilizar a tag button, pois ela faz mais sentido e é **mais semântica** do que o input type button.



**Formulário na Prática**

Servem basicamente para pegar os dados que foram inputados pelo usuário e enviar isso para algum lugar, que geralmente é um backend, que fará algum tratamento nesses dados.

Eles possuem dois tipos de envio diferentes, que serão o **GET** e o **POST**.

O **GET** é pra buscar dados de um servidor, tipo páginas web, sem alterar nada (buscando no mesmo domínio). Ele vai passar as informações que colocarmos no formulário (inputs) por parâmetro na url, ou "querry string". O que é exatamente o que o google faz. 

No exemplo abaixo, ao pesquisar "netflix" no google, podemos ver que a url ficou "q=netflix"

![image-20241121204926732](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241121204926732.png)



Já o **POST** é pra quando você precisa enviar dados pro servidor pra criar ou atualizar algo, como ao enviar um formulário.



**Tag FORM**

A tag form tem abertura e fechamento, o primeiro atributo mais importante é o METHOD, onde colocamos se se trata de um get ou um post *(o próprio emmet do vs code já nos dá a opção de escolher e completar isso ao iniciar a tag).*

![image-20241121204030591](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241121204030591.png)



**Atributos GET e POST** 

Ao criar uma tag de form, automaticamente o vs code vai preencher com o action e method.

O **action** serve pra dizer para o nosso formulário pra onde queremos enviar nossos dados. Geralmente é o caminho para um arquivo backend, como o *index.php*, que vai pegar esses dados, tratar e salvar em um banco de dados, ou pode ser também para outra sessão do site, como no google, onde ele simplesmente manda para o mesmo domínio (google.com) porém colocando um "/search...", pesquisando e mostrando os resultados, sem necessariamente salvar em algum banco de dados.

O **method** sempre será *get* ou *post*, basta apenas verificar qual dos dois atende as suas necessidades nesse html.

![image-20241122000129402](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241122000129402.png)

O post faz o envio de forma mais sigilosa, ao preencher o formulário com post e enviar, ao contrário do GET em que a url é alterada, no post isso não acontece. Ele é indicado para quando, por exemplo, o usuário está fazendo login com e-mail e senha, então passar a senha como um querry string não seria nada seguro.



**Praticando**

Tendo como inspiração a página de cadastro do Facebook, vamos montar um formulário de envio *(apenas o HTML, sem contar a estilização e responsividade feitos no CSS e JS).*

![img](https://cdn.areademembros.com/files/instancia_3760/editor/HQsfb5XeM4rxT4UAx1oxdgNyZJqn8kvhp7YLHFOP.jpg)

Usando as tags *form*, *input*, *label* e *options* daremos corpo ao formulário e utilizando os atributos necessários, os campos ficarão devidamente etiquetados (*type*, *name*, *id*, *placeholder*, *value* etc).

![image-20241122005231669](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241122005231669.png)

Para incluir os dados da data de nascimento (dia, mês e ano), por enquanto, foi utilizado o método de ir um a um, mas existem algumas maneiras melhores e mais rápidas de se fazer, porém veremos mais pra frente no curso. 

**DIA**

![image-20241122004402257](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241122004402257.png)

**MÊS**

![image-20241122004429069](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241122004429069.png)

**ANO**

![image-20241122004448438](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241122004448438.png)

E para a criação dos botões de gênero foi utilizada a tag de input radio com um label para facilitar o clique e "etiquetar".

É importante também se atentar em colocar um value nas tags, para que seja reconhecido o que está sendo enviado.

![image-20241122005308226](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241122005308226.png)

**LEMBRANDO QUE TODOS ESSES DADOS DEVEM ESTAR DENTRO DA TAG FORM, DO CONTRÁRIO, NÃO FUNCIONARÃO.**



Simulando que preenchemos os dados do formulário e enviamos, é possível ver como a url modifica de acordo com o que respondemos.

![image-20241122005648669](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241122005648669.png) ANTES

![image-20241122005756804](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241122005756804.png) DEPOIS

**ATENÇÃO: a senha apareceu na url pois foi utilizado o método GET, mas, para formulários que incluem senhas/dados sigilosos, o correto seria utilizar o POST.**



**Tag Input File *(enviar arquivos de imagem no formulário)***

Utilizando a tag de input file é possível habilitar que o usuário escolha um arquivo do próprio computador para poder enviar (como uma foto de perfil, por exemplo).

![image-20241122011359609](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241122011359609.png)

Sempre que utilizar input file no formulário devemos incluir também um novo atributo a tag form, que é o "enctype". O vs code nos dará 3 opções e a correta será "multipart/form-data" e então o formulário estará preparado para enviar arquivos de imagem. **Se não colocar esse enctype o campo de file não vai funcionar quando enviar para algum servidor backend.**

![image-20241122011249631](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241122011249631.png)

![image-20241122011314983](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241122011314983.png)

O *enc* é de "encode" que é como os dados do formulário serão codificados quando forem enviados para algum lugar.



**Marcando campos como obrigatórios**

Normalmente esse é um processo feito através do JavaScript, mas também é possível realizar essa marcação de obrigatoriedade de preenchimento de campo no html puro.

Para fazer isso é bem simples, basta ir em cada campo que seja de cunho obrigatório e atribuir "required" dentro da tag.

![image-20241122011820151](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241122011820151.png)

Por não ser esteticamente bonito, não é recomendado e nem usualmente utilizado esse tipo de atributo. É melhor e mais bonito fazer pelo JS.



**Tags Semânticas**

A palavra semântica significa a ciência que estuda o significado/sentido e a interpretação desse significado das palavras. Além de estruturar documentos para a web, o html hoje tem uma outra função, que é descrever da melhor forma possível o significado do conteúdo desses documentos. Fazemos isso utilizando as tags semânticas.



**Header**

Geralmente é utilizada para construir o cabeçalho da página ou agrupar alguns títulos. Pode-se ter mais de uma tag header no site.

Dentro da header normalmente teremos uma tag h1.

Podemos ter uma tag nav *(navegação)*, ul *(lista não ordenada)*, li *(lista)* com uma tag a *(âncora)* de link, para criar um menu de navegação;

![image-20241122105607658](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241122105607658.png)



**Main**

Será onde colocaremos o conteúdo principal da página, de maior relevância. Ela só deve aparecer uma vez na página *(o que é bem parecido com o que acontece com a tag h1)*. Geralmente vai englobar todas as outras tags semânticas.

Dentro do main podemos ter uma tag de section *(seções)*, nela todas as tags precisam conversar entre si, então podemos ter um cabeçalho h2, h3 *(títulos)*, uma tag img *(imagem)*, uma p *(parágrafo)*.

*Na section também pode existir uma tag header, não precisa necessariamente ser apenas uma por página, uma header na section ficaria até bem semântico.*

![image-20241122110947177](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241122110947177.png)



**Footer**

É ideal para definir o rodapé na página, mas não serve apenas para isso, ela também pode definir um rodapé de uma section, por exemplo. *Ela fica fora da tag main.*

Nela geralmente ficam informações como endereço, links de contato, telefones, políticas de privacidade, termos etc.

Todas essas tags de dentro do footer poderiam ser substituídas por uma div, MAS ficaria menos semântico, pois div é uma tag muito genérica e as outras tem um significado/função muito forte, um peso maior na página.

![image-20241122112019856](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241122112019856.png)



**Article**

É usada para marcar um conteúdo independente e autocontido, como uma notícia, post de blog ou artigo. Ela ajuda na organização e semântica da página, indicando que o conteúdo pode ser reutilizado ou distribuído isoladamente. Faz sentido por si só, mesmo fora da página onde está inserido, tem um propósito claro.



**Use article quando o conteúdo:**

- Puder ser reutilizado ou distribuído de forma independente.
- Tiver um significado semântico claro (notícias, posts, tutoriais, etc.).

*Uma div com h2 e parágrafo dentro não é semântico, é genérico.*

*Um article com h2 e parágrafo dentro é semântico (ajuda a comunicar ao navegador e a ferramentas como buscadores que é um artigo).*

É recomendado que cada article tenha uma tag de título dentro dela.

![image-20241122114627551](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241122114627551.png)

[Exemplo tag ARTICLE](https://developer.mozilla.org/pt-BR/docs/Web/HTML/Element/article?_gl=1*1453a3z*_ga*MTEwMjE3ODAuMTcyODM5NjEwNA..*_ga_37GXT4VGQK*MTczMjI4NTI0Ny40NS4xLjE3MzIyODUyNzEuMC4wLjA.)



**Aside**

Bastante usada para quando queremos criar uma div de conteúdo adicional ao nosso conteúdo principal. Por exemplo, se estamos fazendo uma página que fala de finanças, essa tag pode ser a indicação de sites de finanças, financeiras, corretoras, sugestões de investimento. É como se fosse uma leitura complementar àquele nosso conteúdo principal. Geralmente aparece como uma coluna lateral nos sites.

É ideal para informações como barras laterais, links relacionados, anúncios ou notas adicionais.



**Quando usar aside:**

- Para barras laterais com links relacionados.
- Para informações de rodapé extras (notas ou referências).
- Para anúncios ou widgets que não são o foco principal da página.

[Exemplo tag ASIDE](https://developer.mozilla.org/pt-BR/docs/Web/HTML/Element/aside?_gl=1*gw62dd*_ga*MTEwMjE3ODAuMTcyODM5NjEwNA..*_ga_37GXT4VGQK*MTczMjI4NTI0Ny40NS4xLjE3MzIyODUyNzEuMC4wLjA.)



**Figure**

Geralmente serve para definir uma caixa de imagem onde terá uma imagem e um texto dentro. 

É usada para agrupar conteúdo relacionado, como imagens, gráficos ou tabelas, juntamente com uma legenda ou descrição. Ela tem um propósito semântico, indicando que o conteúdo faz parte do corpo principal da página, mas é tratado como uma unidade independente.

Usando o mesmo exemplo de img nesse html, podemos englobar a tag img dentro de uma tag figure e, utilizando a tag figcaption, colocamos uma legenda na imagem.

Figcaption é uma tag semântica que terá a descrição da nossa imagem.



![image-20241122120938429](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241122120938429.png)

**Por que usar figcaption e não um parágrafo?**

- **Semântica:** O figcaption é projetado para fornecer uma legenda para o conteúdo dentro do figure, deixando claro o relacionamento entre eles. Já o p é apenas um parágrafo genérico.
- **Acessibilidade:** Ferramentas como leitores de tela entendem que o figcaption descreve o conteúdo do figure, melhorando a experiência para pessoas com deficiência visual.
- **Organização:** Mantém o código mais claro e estruturado, ajudando navegadores e buscadores a interpretar melhor a página.

[Exemplo tag FIGURE](https://developer.mozilla.org/pt-BR/docs/Web/HTML/Element/figure?_gl=1*fml565*_ga*MTEwMjE3ODAuMTcyODM5NjEwNA..*_ga_37GXT4VGQK*MTczMjI4NTI0Ny40NS4xLjE3MzIyODUyNzEuMC4wLjA.)



**Address**

Podemos definir várias coisas como telefone, endereço, e-mail, redes sociais etc. Ela pode ser colocada dentro da tag footer, seguida por uma tag âncora, por exemplo.

![image-20241122121723750](C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241122121723750.png)

[Exemplo tag ADRESS](https://developer.mozilla.org/pt-BR/docs/Web/HTML/Element/address?_gl=1*19ovek4*_ga*MTEwMjE3ODAuMTcyODM5NjEwNA..*_ga_37GXT4VGQK*MTczMjI4NTI0Ny40NS4xLjE3MzIyODUyNzEuMC4wLjA.)