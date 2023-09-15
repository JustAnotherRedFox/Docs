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
                                                                 
       
