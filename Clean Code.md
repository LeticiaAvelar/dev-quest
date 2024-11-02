# **Clean Code** :arrows_clockwise:

:link: Notion: https://glowing-scilla-18d.notion.site/Clean-Code-131bf6c7b63d80baa541ecba68e54dcc?pvs=4



É uma série de princípios, padrões e práticas que, se aplicados corretamente, tornam o nosso código muito mais fácil de entender, dar manutenção e escalar.

Resumindo, seria criar software de qualidade que favoreça o crescimento do produto, ao invés de ser um peso pro crescimento de um negócio.



### **Como surge um código ruim**

Alguns dos motivos seriam:

- Prazos apertados e pressão (pois normalmente não são os devs que estimam os projetos, eles já vem com um prazo definido);
- Falta de responsabilidade do dev em dizer não (para um prazo impossível, uma funcionalidade que sabemos que não dará certo), temos que ser firmes;
- Falta de profissionalismo e/ou ignorância (ignorar algum preceito, padrão, tecnologia que poderiam ajudar no crescimento do projeto);
- Falta de experiência da equipe.



### **Como criar um código limpo desde o início**

- Primeiramente é importante ter o PLANEJAMENTO, não adianta querer colocar a mão no código por ansiedade. É melhor gastar um tempo planejando e depois aplique no projeto.
- Também é importante SABER DIZER NÃO, não ceder à pressão, é melhor fazer da forma certa do que do jeito mais rápido/fácil. Pensando futuramente, é melhor um projeto com código limpo para dar manutenção e menos problemas.
- Sempre INVISTA EM CONHECIMENTO, para poder aplicar padrões/princípios em algum momento e salvar o seu projeto.
- Quebrar um PROBLEMAS EM PEDAÇOS MENORES, ou seja, não queira abraçar o mundo com as mãos, é melhor resolver aos poucos.

LEMBRE-SE: UM CÓDIGO RUIM, ESCRITO COM PRESSA, PRA ENTREGAR UM PROJETO NO PRAZO, VAI VOLTAR PRA TE ASSOMBRAR NO FUTURO.



### **A regra do escoteiro**

Uma vez que você sai do lugar onde está acampando, deve deixar esse lugar mais limpo do que quando chegou. Na nossa área de programação isso significa que quando formos mexer no código de outra pessoa (ou em algum que fizemos no passado), podemos deixar ele melhor do que encontramos, isso pode ser melhorar o nome de uma classe, melhorar o nome de uma variável, dar mais contexto para o código etc.

É importante tomar cuidado, pois às vezes não é necessário e nem viável querer refatorar todo o código só porque a gente achou ele ruim. Por exemplo, um código que tenha JavaScript não é simples de mexer, pois precisa de uma bateria de testes, senão vai dar algum problema nessa modificação.



### **Como saber quando refatorar**

- Avalie o custo/benefício da refatoração;
- Refatore só o código onde estiver mexendo (por exemplo, se estiver mexendo no estilo de uma div de produto, para mudar o background, vc pode refatorar coisas que estejam no escopo dessa div);
- Não tente refatorar tudo de uma vez só.



### **Nomes são importantes (quais as principais características de bons nomes)**

Dar bons nomes é uma arte!

Sempre que for nomear algo, evite colocar nomes específicos em que as propriedades podem se modificar futuramente, por exemplo, produtos que estão em promoção no site precisam de um fundo vermelho, então ao invés de criar uma "class=fundo-vermelho" é muito melhor, recomendado e limpo criar uma "class=promocao".

Bons nomes precisam ser:

- Concisos;
- Descritivos;
- De fácil entendimento;
- Nos dão contexto dentro do código.

<img src="C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241101150215484.png" alt="image-20241101150215484" style="zoom:67%;" />

Nesse exemplo foi utilizado o JavaScript (os comentários no código são as explicações, logo no final é possível ver como seria a melhor nomeação)

<img src="C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241101150548384.png" alt="image-20241101150548384" style="zoom:50%;" />

*const = constante* | *function* = são trechos de código que devem realizar alguma ação

<img src="C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241101150919192.png" alt="image-20241101150919192" style="zoom:67%;" />

<img src="C:\Users\letic\AppData\Roaming\Typora\typora-user-images\image-20241101151014591.png" alt="image-20241101151014591" style="zoom:67%;" />



### **Desenvolvimento gradual e refatoração**

Nós não estamos acostumados a quebrar grandes problemas em problemas menores, isso faz com que muitos devs iniciantes travem.

Um dev experiente, ao se deparar com um problema/teste técnico seguiria os passos:

1. Adquirir uma visão do todo (ler todo o problema, entender, pegar os requisitos etc);
2. Quebrar o problema em pequenos pedaços (tendo uma ideia clara do que consegue resolver primeiro -a parte mais fácil, a parte mais difícil, como desejar);
3. Resolver um de cada vez (pegando problema por problema e resolvendo separadamente);
4. Pedir ajuda se necessário (mesmo sendo experiente vc pode precisar de ajuda);
5. Refatorar (para deixar o código melhor, mais fácil de ler, de dar manutenção, mais performático, menos linhas de código etc);
6. Partir para o próximo desafio (voltaria para o passo 3, resolvendo outro pedaço do problema e assim por diante).



### **Vantagens do desenvolvimento gradual e refatoração**

- Foco de energia (focando em um ponto de cada vez);
- Comprometimento de ir até o fim de pequenos pedaços;
- Nos livra da culpa de não terminar nada;
- Elimina a confusão de ter que resolver mil coisas ao mesmo tempo;
- Chance de refatorar pequenos pedaços do código e deixá-lo limpo.