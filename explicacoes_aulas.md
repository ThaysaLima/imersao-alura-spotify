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