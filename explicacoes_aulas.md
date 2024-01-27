# Aula1 - Revisão: HTML, CSS e JS na Prática.
Começamos com o HTML.
Começamos com a estrutura básica, ! + enter
head = cabeça da página
body = corpo da página

title = título que vai aparecer na aba da página

Como colocar o ícone? 

para carregar o css dentro do html precisamos colocar um link
    <link rel="stylesheet" href="styles.css"> isso é dentro do head.
    
agora podemos já modificar os estilos. 
dentro do css usamos as tags para podes estilizar tudo.
    body {
        background-color: #000; 
    }

        lá na página ela vai ter um fundo preto. 

DICA DE OURO. 
se escrevermos 
    div.sidebar = ele vai automaticamente ciar uma CLASSE dentro da div Oo 
        = <div class="sidebar"></div>

    essa classe é para chamar ela lá no css.

nav = tem peso semântico, ela já diz que vai ser a funcionalidade que colocarmos nela.

assets é onde contem as imagens. 

o ./ serve para sair dessa página e entrar em outra para buscar o arquivo desejado.


Qunado formos clonar uma página, devemos ir olhando pelo devtools para poder entender onde cada parte entra. 

DICA DE OURO. 
quando fomos criar uma lista com 2 itens dentro, podemos criar assim 
ul>li*2 = 
    <ul>
        <li></li>
        <li></li>
    </ul>

<span> = serve para estilizar algo específico.

icons e fontes gratuitas = font awesome
como ultilizar? 
importar CDN que é onde o iconi vai ser hospedado. 

PADDING = espaçamento que ele vai ter, em px (pixels)
    16px 0 0 15px 
    cima - lado direito - baixo - lado esquerdo, pensar no relógio no sentido horário. 
    quando colocamos só um valor, ele irá repetir em todos os lados.
    quando colocamos apenas 2 valores o primeiro valor vai ser cima e baixo, o segundo valor vai ser esquerdo e direito.

POSITION = para saber se ele vai ficar fixo na página ou vai se mexer junto com ela. 
    no caso position:fixed; ele irá ficar fixo. 

TOP E LEFT = 0, para ficar paradinha na posição 0, usamos sempre junto com o position

.log img {} = aqui queremos mexer apenas na imagem da classe logo
.log, img {} = logo e imagem

DICA DE OURO.
como não confundir os width e high
                o width é largura pq o W deixam ele mais deitadinho
                o high é altura pq o L deixa ele mais alto


como tirar as bolinhas da lista. 
dar um reset no css

a ordem do css importa!!

IMPORTANTE! 
    imagina que sem querer demos um git init numa pasta mãe. 
    para desfazer basta escrever rm -r .git

# Aula 2 - Estilo Avançado e Posicionamento: Transformando Layouts.

Bloco do menu lateral de biblioteca. 

Criamos uma div para a biblioteca, library. 
e dentro dela criamos outra div que vai ter o conteúdo dessa library, chamada library_content

PESQUISAR SOBRE 'PADRÃO BEM PARA CSS', METODOLOGIA DE ORGANIZAÇÃO DE ESCRITA DE CSS.
    Basicamente funciona assim:
        temos a class library e dentro da library vamos mexer no conteúdo então temos o library_content, se tivessemos outra coisa para mexer dentro desse conteúdo iriamos escrever library_content_x = x para outro conteúdo.

analogia
as div é a casa e as section são os cômodos. 

Podemos ter mais de uma classe por elemento, até 3 classes é ok.  
    exemplo: 
         <span class="text title"></span>

         mas pq repetimos? pq vamos ter pontos comuns e ai podemos apenas criar outra div com os sub titulos.

sobre o (display) flexbox/flex, foi uma maneira que o css encontrou de fazer um alinhamento mais flexível.
junto com o display flex usamos outras propriedades como o justify-content: ; para deixar na posição que queremos
tb usando junto com o display flex a propriedade flex-direction, e diz assim "esse posicionamento vai ficar flexível para qual direção?" - no caso aqui em colunas/column serve para separar eles em colunas, quando vemos lá no devtools, podemos notar que ele ta "separado em colunas totalizando 4, que são as 4 div e setion que temos dentro do library

margin-top: ; - serve para ele não ficar colado com a outra box de cima. 


colocamos .library .library_content porque precisamos específicar que o library_content esta dentro de outra classe, se não colocarmos da maneira correta (.library .library_content) ele não irá aplicar corretamente. = isso serve para qualquer classe que esteja dentro de outra

entender melhor sobre o flex-start. 


DESAFIO DA AULA: 
FAZER O FOOTER. 

# Aula 3 - Layout Flexbox, Pseudo-classes e Responsividade em CSS. 

Aqui organizamos as páginas onde criamos a pasta src com os nossas assets que contem os icons e imagens. 
depois temos que ir mudar os nossos links com os novos caminhos. 

criamos tb a pasta styles para conter todos os css. 

renomeamos o arquivo que estava styles.css para um que condizesse mais com o que tinha no arquivo que vai ser sidebar_footer.css


criamos o arquivo vars.css, nele vamos colocar todas as variáveis que vamos criar.  
    a primeira que criamos vai ser uma variável para a principal fonte do site (para quando for necessária trocar,s er mais fácil).
        :root{
                    /*FONT*/
            --font-dm-sans: "DM Sans", sans-serif; /*declaramos uma variável que vai receber uma fonte.*/
        } 

    agora temos que ir la no nosso css principal e colocar no .body a nossa variável criada. 
        body {
            font-family: var(--font-dm-sans); /*isso serve para não termos problemas com a fonte que tem que ser igual em toda a página.*/
        }.

VAMOS FAZER A BUSCA AGORA: 

O id é como se fosse um RG, não vai existir outro igual. 
maxlength é para quantos caractéres no máximo vai poder se colocado naquele input

placeholder é o texto que já fica ali no input antes de escrevermos algo. 



quando temos RGBA significa que o vermelho, verde e azul vão ser mais opacos (A)


# DICA DE OURO
    O ALLIGN-ITENS E JUSTIFY CONTENT, SÓ FUNCIONAM SE O DISPLAY FOR FLEX.

o justify-content só arruma com as suas propriedades horizontalmente. 
        flex-start: Items align to the left side of the container.
        flex-end: Items align to the right side of the container.
        center: Items align at the center of the container.
        space-between: Items display with equal spacing between them.
        space-around: Items display with equal spacing around them. 

o align-items só arruma com as suas propriedade verticalmente. 
        flex-start: Items align to the top of the container.
        flex-end: Items align to the bottom of the container.
        center: Items align at the vertical center of the container.
        baseline: Os itens são exibidos na linha de base do contêiner.
        stretch: Os itens são esticados para caber no contêiner.

Flex-direction essa propriedade define em qual direção eles irão ocupar no conteiner. 
        row: Items are placed the same as the text direction.
        row-reverse: Items are placed opposite to the text direction.
        column: Items are placed top to bottom.
        column-reverse: Items are placed bottom to top.

Quando você define a direção para uma linha ou coluna reversa, start e end também são reversos.

!Note que quando a direção é em coluna, justify-content muda para a vertical e align-items para a horizontal.
    então no caso, usamos o flex-direction column então a direção agora é para baixo.

!Às vezes, reverter a ordem de uma coluna ou de um container não é suficiente. Nesses casos, podemos aplicar a propriedade order para itens individuais. Por padrão, itens tem um valor de 0, mas nós podemos usar essa propriedade para alterar para um valor inteiro positivo ou negativo. 
    order: 1;

!Outra propriedade que você pode aplicar para itens individuais é align-self. Esta propriedade aceita os mesmos valores que align-items e seus valores são usados para o item específico.

Flex-wrap aceita os seguintes valores:
        nowrap: Todos os itens são apertados em uma única linha.
        wrap: Itens se separam em linhas adicionais.
        wrap-reverse: Itens se separam em linhas adicionais em reverso.

!As duas propriedades flex-direction e flex-wrap são usadas tão frequentemente juntas que uma propriedade abreviada flex-flow foi criada para combiná-las. Essa propriedade aceita o valor das duas propriedades separados por um espaço.
Por exemplo, você pode usar flex-flow: row wrap para aplicar a direção de linha e quebrar em múltiplas linhas.

align-content para definir como múltiplas linhas devem ser espaçadas uma das outras. Essa propriedade recebe os seguintes valores:
        flex-start: Linhas são agrupadas no topo do container.
        flex-end: Linhas são agrupadas no fundo do container.
        center:Linhas são agrupadas no centro vertical do container.
        space-between: Linhas são posicionadas com espaço igual entre elas.
        space-around: Linhas são posicionadas com espaço igual em torno delas.
        stretch: Linhas se esticam para preencher o container.
                Isso pode ser confuso, mas align-content determina o espaçamento entre linhas, enquanto align-items determina como as linhas como um todo são alinhadas dentro do container. Quando há só uma linha, align-content não tem nenhum efeito.