# Aula1 
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