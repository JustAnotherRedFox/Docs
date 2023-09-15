============================================= CSS ================================================ @charset=UTF-8; - declaraçao obrigatoria em todo .css

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
 
