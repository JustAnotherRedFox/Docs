                                            - HTML & CSS -
HTML – HyperText Markup Language
CSS – Cascading Style Sheets

HTML[conteudo], CSS[estilo], JS[interatividade]

front-end[client-side]
back-end[server-side]

SEO –  search engine optimization

================================================= HTML ===========================================
                                              
Estrutura basica:

<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1,0"> 
    <title>titulo do site</title>
    <link rel="stylesheets" href="style.css"
</head>
<body>
    <header>
        <h1>titulo da pagina</h1>
        <nav>barra de navegacao</nav>
    </header>
    
    <main>
        <section>
        
            <article>
                <p>artigo do site</p>
            </article>
            
            <aside>
                <p>artigo lateral</p>
            </aside>
            
        </section>
    </main>
    
    <footer>
        <p>roda-pe do site</p>
    </footer>
    
    <script src="script.js"></script>
    
</body>
</htlm>

<header>  - usado para criar o cabecario do site, somente atributos globais
<nav>     - usado para criar a navegacao do site, somente atributos globais
<main>    - conteudo principal da pagina, somente um por pagina, somente atributos globais
<section> - sessoes do site, geralmente comportam o article, apenas atributos globais
<article> - artigos ou posts de uma pagina, apenas atrubutos globais
<aside>   - conteudos levemente relacionados ao conteudo principais
            explicacoes, sidebars, informasoes de pefil, grosarios, links extras,
            apenas atributos globais
<footer>  - geralmente no final da pagina, informacoes do autor, copyright, sitemap, voltar ao 
            topo, somente atributos globais
<div>     - usado se nao achar um elemento de bloco semantico,
            * usa-se 'id' e 'class' para entregar maior significado
<span>    - usado se nao achado um elemento de texto semantico, 
            * usa-se 'id' e 'class' para entregar maior significado

<h1> - titulo de uma pagina
<p> - paragrafo
<img src="foto.png" alt="foto alternativa"> - coloca uma imagem, com o source 'foto.png' e 	
alternativa 'foto alternativa'
<hr> - horizontal row, cria uma linha horizontal
<br> - break row, quebra o paragrafo para a proxima linha
&lt;[<], &gt;[>], &uparrow; ou &uarr;
<em> ou <u> - usa uma underline/emphasis
<b>  ou <strong>- usa negrito ou bold
<mark> - usa marcaçao de background
<small> - deixa o texto com letras pequenas
<sup> e <sub> - sobrescreve e subscreve o texto
<ol> - cria uma lista ordenada
<ul> - cria uma lista nao ordenada
<li> - cria um item em uma lista
<dl> - cria uma lista de definiçao
<dt> - cria um termo de definiçao
<dd> - cria uma descriçao para um termo
<a href="link" target="_blank" rel="external">link txt</a> - cria um link de redirecionamento em 
outra pagina
<picture> - abre um espaço para criar imagens dinamicas
<source media="(max-width:750px)" srcset="image/image.png" type="image/png"> - usado dentro do 
<picture> define a condiçao de criaçao das imagens dinamicas
<audio> - pode-se usar do mesmo modo que <picture>
<blockquote> e <cite> - citacao de uma fonte externa

------------------------------------------------ media ----------------------------------------

-------------------- video -----------------

<video controls width="640" height="480" autoplay preload="auto">
   <source src"./assets-exemple/exemple.mp4" type="video/mp4">
   <source src"./assets-exemple/exemple.mkv" type="video/mkv">
   <p>seu browser nao suporta video</p>
</video>

    * permite adicionar videos ao html
    
    atributos
    
    - src
        * source do video
    - controls
        * adiciona o controle de execucao do video
    - fallback content
        * se o video nao poder ser carregado pode-se colocar outro video com outros formatos como
          backup
        * se nenhum formato de video funcionar, pode-se adicionar uma frase de explicacao
    - source
        - src
            * source, fonte do video
        - type
            * tipo de video
    - width e height
        * defina a largura e altura do video
    - autoplay
        * executa o video automaticamente ao carregar a pagina
    - preload
        - auto
            * baixa o video automaticamente ao carregar a pagina
        - metadata
            * baixa apenas o necessario do video ao carregar a pagina
        - none
            * apenas comeca a baixar quando o video for iniciado
    - loop
        * executa o video em loop
    - muted
        * faz o video iniciar mutado, alguns navegadores permitem a execucao automatica apenas
          quando o muted esta ativo
    - poster
        * ex.: poster="./icon.png"
        * coloca uma foto selecionada com thumbnail

------------------- audio ------------------

<audio controls>
    <source src="./assets-exemple/exemple.mp3" type="audio/mp3">
    <source src="./assets-exemple/exemple.ogg" type="audio/ogg">
    <p>seu navegador nao suporta audio</p>
</audio>

    * permite adicionar audio ao html
    
    atributos
    
    - src
    - controls
    - fallback content
    - source
        - src
        - type
    - autoplay
    - preload
        - auto
        - metadata
        - none
    - loop
    - muted
    
------------------- media externa ------------------

<iframe 
    src="https://www.youtube.com/embed/AqJKAJ0TKms" frameborder="0"
    width="640"
    height="480"
    frameborder="0"
    allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture"
    allowfullscreen
    title="titulo do video">
</iframe>
    
      * inline frame element
      * permite adicionar mapas, videos, sons, etc... 
      * cuidado com seguranca e copyright

    atributos
    
    - src
    - width e height
    - title (acessibilidade)
    - allowfullscreen
        * permite tela-cheia
    - frameborder
        * borda do video
    - gyroscope
        * permite giro automatico da tela

------------------- imagem -------------------------

<a href="https://google.com">
    <img 
        src="https://source.unsplash.com/random" 
        alt="imagem de titulo" 
        title="titulo da imagem"
    >
</a>
    atributos
    
    - src
    - alt
    - title
        * coloca um titulo para a imagem
        * ativado quando o mouse esta em cima
    - width
    - height
    - <a>
        * permite usar a imagem como um link para redirecionamento ou download
    
---- titulos visiveis ----

<figure> e <figcaption>

<a href="https://google.com">
    <figure>
        <img
            src="https://source.unsplash.com/random"
            alt="imagem de titulo"
            title="titulo da imagem"
            height="250px"
        >
        
        <figcaption> titulo da imagem </figcaption>
    </figure>
</a>

----- SVG -------

<svg>
    * e uma tag, estilo html, mas nao para textos mas para imagems
    * possui elementos para gerar formas
    
    beneficios
        * mais leve
        * mais detalhado
        * maior acessibilidade e SEO
        * pode ser editada via css ou atributos
        * diminui as calls http externas
        
    desvantagens
        * pode ser mais complicado de usar
        * quanto mais complexa a imagem, mais trabalho para o navegador
        * navegadores mais antigos nao suportao esta tags
        * sem cache
        * nao recomendavel para fotografias, mais recomendado usar imagems rasterizada
        
    rasterizada
        * imagems feitas via pixels
        * mais faceis de usar
        * mais detalhado em maiores resolucoes
    vetorizada
        * imagems feitas via algoritimo
        * mais leve
        * mais detalhadas em todas as resolucoes independente do zoom
        * melhor SEO
        
<svg
    width="200" height="200">
        <circle cx="150" cy="150" r="80" stroke="red"
        stroke-width="6" fill="blue" />
</svg>
    * criando um circulo azul com bordas vermelha

-------------------------------------------- formularios -----------------------------------------

<form> defina um formulario
    container estilo <section> <footer>
        
    atributos basicos
        - action
        - method
            - GET
            - POST   
    nao crie <form> dentro de <form>

<fieldset>
        - agrupamento de campos 
        - mesmos proposito
        - semantico
        - acessibilidade
    atributos especiais
        - desabled
            - desabilita todos os elementos internos
            - nao serao enviados ao submeter o formulario
        - form
            - o id de um formulario ao qual esse fieldset pertence
            - nao precisa estar dentro do formulario
        - name
            - nome do grupo
        
        <legend>
            - nome do fieldset
            - primero elemento do fieldset
    
<label>
    - associar e indentificar uma ou mais tags de entrada de dados(input)
    - acessibilidade
    - voce poderar clicar para mudar o foco da entrada de dados
    
    atributos
    - for
        - para fazer a conexao entre este label e a tag de input
        - feita atraves do id do input
        - so funciona com elementos especificos
            - button, input(not hidden), meter, output, progress, select, textarea
            
<button>
    - representa um botao
    - usado para enviar formularios
    - estilizado pelo user agent (normalmente o browser)
    
    atributos comuns
    - type
        - submit
        - reset
        - button
    - autofocus
    - disabled
    - name
    - value
    - form
    
<datalist>
    - lista de valores como sugestao a uma tag <input>
    - valores sugestivos e nao obrigatorios
    - usuario pode selecionar um dos valores, ou colocar um valor diferente da sugestao

    list
    - recebe como valor o id de um <datalist> residente no mesmo documento

    tipos de input suportados
    - text, search, url, tel, email, date, month, week, time, datetime-local, number, range e 
    color
    * valores de datalist nao compatives nao seram apresentados
    tipos de input nao suportados
    - hidden, password, checkbox, radio, file, ou qualquer tipo de button
    
<input>
    - um dos mais usados em formularios
    - aceita os mais diversos tipos de dados
    - um dos mais poderosos e complexos
    - elevados numero de combinacoes
    
    atributos
    - type
    - name
    - id
    - email
    - password
    - number
    - file
    - pattern
    - size
    - autocomplete
    - disabled
    - readonly (quase todos)
    - form (quase todos)
    - required (quade todos)
    - placeholder (password, search, tel, text, url)
    
<input type="password">

    - coloca uma senha de forma segura
    - esconde oque esta sendo digitado
    - o estilo do campo depende do user agent
    
    atributos
    
    - minlength/maxlength
        * minimo e maximo de caracteres contidos no campo
    - size
        * numero aceitavel de catacteres contidos no campo
    - pattern
        * expressao regular para validar o campo
        * altamente recomendado para uso de um padrao de seguranca alta de senhas
        * exemplo: queremos que a senha contenha caracteres hexadecimais de no minimo 4 e maximo 8 
        caracteres
            * pattern="[0-9a-fA-F]{4,8}"
    - placeholder
        * mostra um exemplo de texto a ser digitado no campo
    - readonly/disabled
        * atrubuto boolean que indica se o campo esta habilitado ou nao
    - required
        * o campo sera obrigatorio
    - inputmode
        * podera alterar o uso do teclado em smartphones
        * exemplo: queremos que adicione apenas numeros
            * inputmode="numeric"
    - autocomplete
        * on: permite sugestao de: new-password ou current-password
        * off: desabilita a opcao de autocompletar
        * new-password: o navegador pode sugerir uma nova senha
        
<input type="email"/>

    - espera que o usuario digite um email
    - ira validar se o valor digitado e uma email
    
    atributos
    
    - placeholder
    - readonly/disabled
    - value
    
    - required
    
    - multiple
        * o campo ira receber 1 ou mais emails, separado por vircula
    - minlength/maxlength
        * minimo e maximo valor contido no campo
    - size
        * valor numerico indicando a quantidade de caracteres mostrado no campo
    - pattern 
        * uso de expressao regular para validar o campo
        * exemplo: o usuario so podera colocar email do dominio gmail.com.br
            * pattern=".+@gmail\.com\.br"
    - list 
        * o id de uma tag <datalist> que esta no mesmo documento
        * <datalist> ira conter uma lista de valores pre definidos a fim de sugerir ao usuarios, 
        quais valores estao disponiveis
            * os valores do <datalist> que nao forem conpativeis com o campo nao serao 
            apresentados como sugestao
            
<input type="url" />

    - espera que o usuario digite uma url
    - ira validar se o valor digitado e uma url
    
    atributos
    
    - placeholder
    - readonly / disabled
    - value
        * pode ser usado como exemplo ou dica ao usuario
        * exemplo: http://www.google.com.br    
    - required
    
    - minlength/maxlength
        * o minimo e maximo valor que o campo deve conter
    - size
        * valor numerico indicando quantos caracteres esse campo deveria conter, modificando o 
        tamanho do campo para o usuario
    - pattern
        * uso de expressao regular para validar o campo
        * exemplo: o usuario so pode colocar dominios do tipo  .com.br
            * pattern="*\.com\.br.*"
    - list
        * o id de uma tag <datalist> que esta no mesmo documento 
        * <datalist> pode conter quaiss valores estao disponiveis
            * os valores do <datalist> que nao forem compativeis nao setam apresentados
    - spellcheck
        * habilita a verificacao ortografica para este input
        
<input type="file" />

    - usuario podera escolher 1 ou mais arquivos para enviar ao formulario
    
    atributos
    
    - value
        * contem o arquivo a ser enviado
    - accept
        * descreve que tipo de atquivos serao aceitos
        * exemplo: .doc, .docx, .pdf, .audio/*, image/png, .png
    - files
        * a lista de arquivo ou arquivos
    - multiple
        * permite o envio de multiplos arquivos
    
    envio de arquivos
    
    para envio dos arquivos o formulario devera utilizar o metodo POST e o atributo enctype como 
    "multpart/form-data"
    
<input type="color" />

    - interface para selecionar cor
    - color picker
    
    atributos
    
    - value: RGB
        * se invalido, o preto sera exibido
    - list
        * o id de uma tag <datalist> que esta no mesmo documento
        * o <datalist> ira conter valores pre-definidos
            * os valores nao compativeis nao seram exibido
            
<input type="checkbox">

    - caixas que podem ser marcadas
    - seleciona uma valor para ser enviado
    - se nao selecionado, nao sera enviado nenhum valor
    
    atributo
    
    - globais
    - value
        * valor que aquele campo contem
        * se nao presente o padrao e 'on'
    - checked
        * para deixar o campo marcado por padrao
    multiplos valores
        * usa-se o atributo 'name' com o mesmo nome para os diversos campos
        
<input type="hidden">

    - exemplo:
        * <input type="hidden" id="timestamp" name="timestamp" value="4543543543">
    
    caracteristicas
    
        * invisivel para o usuario
        * sera enviado junto do formulario
        * nao recebera foco
        * leitores de tela nao percebem este campo
        
<input type="radio">

    - projetado para selecionar uma unica opcao de um grupo de opcoes
    
    atributos
    
    - checked
        * indica que o campo foi marcado
    - value
        * valor que o campo contem
        
<textarea>

    - mais de uma linha
    - util para textos grandes
    
    atributos
    
    - id
    - name
    - rows e cols (linhas e colunas)
    - maxlength e minlength
    - wrap (quebra de linha automatica)
        * wrap="soft" (defaut)
        * wrap="hard"
        * wrap="off"
    - ... outros comuns aos <input>s
        - autocomplete, autofocus, disabled, placeholder, readonly, form, required

<select>

    - controle que fornece um menu de opcoes
    
<option>
    - comtem as opcoes a serem selecionadas
    - atributos necessarios
        * value
    
    atributos
    
    - multiple
        * habilita multiplas opcoes
    - size
        * quantidade de opcoes visiveis
    - <optgroup label="group_name">
        * para agrupar os options
        
<input type="search" />

    - para campos de busca
    
    atributos
    
    - list / <datalist>
    - pattern
    - arial-label 
        * funciona como um label porem sem ser mostrado na tela
        
<input type="number" />

    - entrada de numeros
    
    atributos
    
    - min/max
        * numaro minimo e maximo aceito
    - step
        * de quantos em quantos numeros a serem pulados
    - ... outros comuns aos <input>s
        - autocomplete, autofocus, disabled, placeholder, readonly, form, required
        
<input type="range" />

    - controle para selecionar um valor numerico
    - slider ou dial control
    
    atributo
    
    - min/max 
    - step
        * modifica a gradualidade do slider
        
inputs com pouco suporte

- <input type="date">
    * obrigatoriamente deve ser value="yyyy-mm-dd"
- <input type="datetime-local">
- <input type="month">
- <input type="week">

----------------------------------- DOM (Document Object Model) ----------------------------------

    * e o html convertido para um objeto javaScript
    * API qu representa e interage com o html
    * estrutura de dados tipo arvore, criada pelo browser
    *propriedades e metodos
    
    Uso
    * JS usa a DOM para se conectar ao html
    * manipular o html com o JS
    
    exemplo:
    
    <!DOCTYPE html>
    <html lang="pt-br">
        <head>
            <meta charset="UTF-8">
            <meta name="viewport" content="width=device-width, initial-scale=1.0">
            <title> titulo da pagina </title>
        </head>
        <body>
            <h1>titulo</h1>
        </body>
    </html>
    
                                      Document Object Model
                                      
                                            Document
                             ↓                                      ↓ 
                            head (parent)                          body (parent)
        ↓          ↓                ↓                               ↓ 
      meta       meta (brother)    title  (child)                   ↓ 
                                                                 title  (child)
                                                                 
============================================= CSS ================================================
@charset=UTF-8; - declaraçao obrigatoria em todo .css

h1{
    font-family: Arial;        | declara o valor fonte
    font-size: 20pt;             | declara o valor tamanho
    color:blue;                    | declara o valor cor
  declaraçao[font-family:Arial] / propriedade[font-family] / valor[Arial] / seletor[h1]
}

body {
    height: 100vh;
    width: 100vw;
}

.class  = '.' representa a class criada no html
#id     = '#' representa a id criada no html

-------------------------------------- valores e unid. de medida ---------------------------------

* cada propriedade possui valores 'property: value'
* os termos podem variar. 'values' ou 'data types'
    * <length> <color>
    
Tipos numericos
    * <interger>        numeros inteiros: -23, 233
    * <number>          numeros decimais: -3.4, 345.00, 0.22
    * <dimension>       um <number> com uma unidade junto: 90deg, 2s, 8px
    * <percentagem>     representa a fracao de um outro numero: 50% de ...

unidades comuns
    * <length>          valor de distancia: px, em, vw
    * <angle>           valor de angulo: deg, rad, turn
    * <time>            valor de tempo: s, ms
    * <resolution>      valor de resolucao para dispositivos: dpi
    
distancias absolutas <length>
* sao fixas e nao alteram seu valor

  unidade  |       nome       |    equivalencia
  cm       | centimetros      | 1cm = 96px/2.54
  in       | inches(polegadas)| 1in = 2.54cm = 96px
  px       | pixels           | 1px = 1/96th of 1in
  
* o mais utilizado e o 'px'
* nao recomendado usar o cm

distancias relativas
* sao relativas a algum valor, pode ser ao elemento pai, root, ou tamanho da tela

* beneficioo: melhor adaptacao a telas de tamanho diferentes

unidade  |   relativo a          
em       | tamanho da font do pai
rem      | tamanho da font do elemento raiz (root/html)
vw       | 1% da viewport width
vh       | 1% da viewport height

porcentagems
* em muitos casos tratado da mesma maneira que distancias <length>
* sempre relativo a algum valor
* ira usar como referencia o valor pai

posicoes
* <position>

* representa um conjunto de coordenadas 2D:
    * top, right, bottom, left, center
    
* usado para alguns tipos de propriedades
* nao confundir com a propriedade 'position'

funcoes
* sao reconhecidas por causar um reaproveitamento de codigo.

* rgb(255, 255, 255)
* hsl()
* url(http://exemple.com)
* calc(50% + 20px)

strings e identificadores
* strings: textos envoltos em quotation mark("");
* identificadores: red, black, gold;

--------------------------------------------- seletores ------------------------------------------
* conecta um elemento html com css, a fim de alterar este elemento

tipos
* element selector
    * todos os elementos html
    
* id selector
    * um elemento que tenha um atributo 'id'
    * deve ser unico
    * caracterizado por '#'
    * exemplo: #id {}
    
* class selector
    * os elementos que possuam um atributo 'class'
    * pode-se ter mais de uma class
    * caracterizado por '.'
    * exemplo: .class {}
    
* attribute selector
    * um elemento que possua um atributo especifico
    * caracterizado por '[]'
    * exemplo: [title] {}
    
* pseudo-class selector
    * elementos em um estado especifico
    * caracterizado por ':'
    * exemplo: h1:hover {}
    
multiplos
* pode-se selecionar multiplos elementos e aplicar alguma regra css a eles 
* usa-se uma separacao de comma(,) para isso

* exemplo: h1, p, a {}

combinators
* combinadores, trabalham para buscar e combinar seletores a fim de apllicar uma estilizacao

descendant combinator
* identificado por um espaco entre os seletores
* busca um elemento dentro de outro

exemplo: body article h2

child combinator 
* identificado pelo sinal '>' entre dois seletores
* seleciona somente o elemento filho direto do elemento pai
* elementos depois do filho direto seram desconsiderados
* a busca sera feita e seguida de maneira estrita

exemplo: body > ul > li

adjacent sibling combinator
* identificado pelo sinal '+' entre dois seletores
* seleciona apenas o elemento do lado direto que e irmao direto na hierarquia
* aquele que esta diretamente abaixo do elemento a direita

exemplo: h1 + p

general sibling combinator
* identificado pelo sinal '~' entre dois seletores
* seleciona todos os elementos irmaos ao lado do elemento a direita

exemplo: h1 ~ p

utilizacao de combinators
* seletores muito especificos tendem a causar dificuldades no reuso sas regras de estilizacao
* muitas vezes, um simples uso de classk, torna o trabalho mais eficiente

exemplo: ul > li[class="exemple"]

--Pseudo-classes
* e um tipo de seletor que ira selecionar um elemento que estiver em um estado expecifico

exemplo: o primeiro elemento de uma caixa, ou o elemento que esta com o mouse em cima

* pseudo-classes comecam com colon(:) sequido do nome da pseudo class: ':pseudo-class-name'

selecionado elementos com pseudo-class
* :first-child
    * seleciona o elemento first-child
    * exemplo: article p:firt-child
        * seleciona o first-child <p> se ele existir e for o first-child
        * se o elemento selecionado nao for firs-child o seletor sera ignorado
        
* :nth-of-type()
    * peque o elemento n child do parent
    * exemple: article p:nth-of-type(2)
        * seleciona o segundo <p> dentro do <article>
        
* :nth-child()
    * seleciona o n child do parent
    * exemple: article p:nth-child(3)
        * ira selecionar o terceiro child do parent se ele existir, nao inporta qual for
        * se nao existir o seletor sera ignorado

acoes do usuario
* :hover
    * usado para mudar as propriedades e estilo do elemento emquanto o mouse estiver em cima
    
* :focus
    * usado para mudar as propriedades e estilo do elemento enquanto ele estiver selecionado

atributos
* :disabled
* :required
    
--Pseudo-elements    
* usado para adicionar elementos html pelo proprio css, 
* pseudo-elements comecam com 2 colons(::) sequido do nome do pseudo-element
exemple: '::pseudo-element-name'
    
* ::before
    * seleciona para alteracao oque vem antes do elemento selecionado
    * exemplo: p::before {content: ">"}
        * >paragrafo
    * o content deve ser colocado na primeira linha obrigatoriamente
* ::after
    * seleciona para alteracao oque vem depois do elemento selecionado
    * exemplo: p::after {content: "<"}
        * paragrafo<
    
* ::first-line
    * seleciona para alteracao a primeira linha de um texto
    
---------------------------------------- box model ----------------------------------------------
* fundamental para fazer layouts para a web
* maior facilidade para aplicar o css

caracteristicas
* e uma caixa retangular
* possui as propriedades de uma caixa 2D

- tamanho (largura x altura)     width | height
- conteudo                       content
- bordas                         border
- preenchimento interno           padding
- espacos fora da caixa           margin

* cada elemento na pagina sera considerado uma caixa

Box-sizing
qualculo do tamanho da caixa
* usando o border-box o tamanho sera limitado ao width e height
* se nao usa-lo o tamanho de borda sera adicionado ao width e height
- content-box | border-box

exemple: div {box-sizing: border-box;}

Display: block e Display: inline
* como as caixas se comportam em relacao a outras
* comportamento externo das caixas

- block
    * ocupa toda a linha, o proximo elemento sera empurrado para a linha de baixo
    * width e height sao respeitados
    * paddig, margin, border irao funcionar normalmente
    
- inline
    * elemnto ira continuar um ao lado do outro
    * width e height nao funcionam
    * somentes valores horizontais de margin, padding e border
    
exemple: block: '<p> <div>', todos os headings '<h1><h2>...'
         inline: '<a> <strong> <span> <em>'

Margin
espaco entre os elementos

- margin-top | margin-right | margin-bottom | margin-left
- value: '<length>' | '<percentage>' | auto

exemple: shorthand:
         margin: 12px 16px 10px 4px;    * top, right, bottom, left
         margin: 12px 16px 0;           * top, right-left, bottom
         margin: 8px 16px;              * top-bottom, right-left
         margin: 6px;                   * top-right-bottom-left
         margin: auto;                  * centraliza o elemento no centro da tela
        
* cuidado com margin collapsing (top se ajunta ao bottom)

Padding
preenchimento interno da caixa

- padding-top | padding-right | padding-bottom | padding-left
- value: '<lenght>' | '<percentage>' | auto

exemple: shorthand:
         padding: 12px 16px 10px 4px;    * top, right, bottom, left
         padding: 12px 16px 0;           * top, right-left, bottom
         padding: 8px 16px;              * top-bottom, right-left
         padding: 6px;                   * top-right-bottom-left
         padding: auto;                  * centraliza o elemento no centro da tela

* padding podera causar diferenca na largura de um elemento

Border e outline
as bordas da caixa

- value: '<border-style>' | '<border-width>' | '<border-color>'
        - style: solid, dotted, dashed, double, groove, ridge, inset,outset
        - width: '<lenght>'
        - color: '<color>'

exemple: shorthand:
         border-top: solid 2px;  * top | right | bottom | left
         
         style:
         border: solid;
         
         width <lenght> | style:
         border: 2px dotted;
         
         style | color:
         border: outset #f33;
         
         width | style | color
         border: medium dashed green;

outline
difere em 4 sentidos:
    * nao modifica o tamanho da caixa
    * podera ser diferente de retangular
    * nao permite ajuste individual
    * mais usado pelo user agente para acessibilidade

---------------------------------------- fontes no css ------------------------------------------
tipografia transmite mensagem
    * negrito
    * tamanho 
    * estilo
    
basic font properties
    * font-family
    * font-weight
    * font-style
    * font-size
    
font family
* tipo de fonte de um elemento
* lista de fontes e ordem de prioridade
* inclui fallback fonts

exemplo:
    p {
        font-family: "Times New Roman", Times, serif;
    }
 * serif
 * sans-serif
 
font weight
* peso da fonte

exeplo:
    p {
        font-weight: bold;
    }

font style
* o estilo da fonte

exemplo:
    p {
        font-style: italic;
    }
    
font size
* o tamanho da fonte

exemplo:
    p {
        font-size: 10px;
    }
    
web fonts
* fontes do sistema x fontes da web
    * @font-face
    * @import
    * link

font variant
* variacoes na apresentacao da fonte

exemple:
    p {
        font-variant: small-caps;
    }

font stretch
* alargamento ou encolhimento da fonte
* aceita palavras-chaves como: expanded, condensed, normal
* aceita porcentagems de 50% a 200%

exemplo:
    p {
        font-stretch: expanded;
    }
    
letter spacing
* espacamento entre letras

exemplo: 
    p {
        letter-spacing: 2px;
    }

word spacing
* espacamento entre caracteres

exemplo:
    p {
        word-spacing: 4px;
    }

line height
* espaco entre linhas
* pode ser com unidades ou sem unidades de medida
* comuns: 1.5 ou 2

exemplo:
    P {
        line-height: 1.4;
    }

text transform
* transformacao do texto
* pode ser usado: capitalize, lowercase, none ...
exemplo: 
    p {
        text-transform: uppercase; 
    }
    
text decoration
* aparencia decorativa do texto
* line: underline, overline, line-through
    * pode-se aplicar mais de um valor
* style: wavy, dotted, double, dashed, solid
* color: '<color>' values

exemple:
    p {
        text-decoration: underline dotted red;  //shorthand
    }

text align
* alinhamento do texto

exemple:
    p {
        text-align: center;  //left, right, center, justify
    }
    
text shadow
* sombra aplicada a um texto
* permite multiplos valores

exemplo: text-shadow: 1px 1px 1px black,
                      2px 2px 2px red;  //offset-x, offset-y, blur-radius, color
                      
shorthand 
* font-style, font-variant, font-weight, font-stretch, font-size, line-height, 
font-family

exemple:
    p {
        font: italic normal bold normal 3em/1.5 Helvetica, Arial, sans-serif;
           //style, variant, weight, stretch, size, line-height, family
    }
    
---------------------------------------- page layouts -------------------------------------
- table
- floats e clear
- frameworks e grid system
- flexbox
- grid

possicionamento
* controlar onde, na pagina o elemento devera ficar
* alterando o fluxo normal dos elementos

- name: position
- value: static, relative, absolute, fixed

relative
    * top, right, bottom, left, z-index
    
absolute
    * top, right, bottom, left, z-index
    
fixed
    * top, right, bottom, left, z-index
    
element stacking
    * z-index

--- flexbox ---
    * nos permite posicionar os elementos dentro da caixa
    * controle em uma dimensao (horizontal e vertical)
    * alinhamento, direcionamento, ordernar, tamnhos
    
    exemple:
        div.parent {
            display: flex;
        }
        
flex-direction
    * qual a direcao do flex: horizontal or vertical
    * row | column
    
alinhamento
    * justify-content
    * align-items
    
--- grid ---
* posicionamento dos elementos dentro da caixa
* posicionamento horizontal e vertical ao mesmo tempo
* pode ser flexivel ou fixo
* cria espacos para os elementos filhos habitarem

    exemple: 
        body {
            display: grid;
        }
        
