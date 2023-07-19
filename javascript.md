---------------------------- caracteristicas do js ------------------------------------

* Case-Sensitive               //maiosculo e minunsculo faz diferenca
* sequencial                  //o codigo e lido em sequencia
* weakly typed               //nao precissa definir previamente o type da variavel
* dynamic                   //pode-se mudar o type da variavel
* Unicode                  //aceita o padrao de caracteres Unicode

* data types
    * Primitive/ Primitive value
    * Structural
    * Structural Root primitive
    
- Primitive Type
    * String
    * Number
    * Boolean
    * Undefined
    * Symbol
    * BigInt
- Structural Type
    * Object
        # Array
        # Map
        # Set
        # Date
        #...
    * Function
- Structural Root primitive
    * Null
----------------------------- java script basic commands -------------------------------
window.alert("")       - abre uma janela com um texto ou alerta
window.confirm("")     - abre uma janela de comfirmacao
window.prompt("")      - abre um prompt interativo para o usuario
var nova_variavel      - declara uma variavel de escopo global
let nova_variavel      - declara uma variavel de escopo de bloco
const nova_variavel    - declara uma variavel de escopo de bloco imutavel

//        - para comentarios de uma linha
/**/      - para comentarios de mais de uma linha
``        - para quebras de linhas e interpolacao

typeof nome_variavel  = mostra o tipo da variavel
indexOf nome_variavel = mostra o indice da variavel

-------------------------------------------- variaveis -----------------------------------------

sao nomes simbolicos para receber ou guardar uma valor
- definicao de variaveis
    * var
    * let
    * const 

* podem comecar com 'letras', '$' ou '_'
* nao podem comecar com numeros
* pode-se usar letras, numeros, acentos e simbolos
* nao podem conter espacos ex: '  '
* nao podem conter palavras reservadas ex: 'alert, var, if, while...'
* escolha nomes coerentes
* camelCase  - usar uppercase no lugar de espacos  ex. checkIfNameExist
* snake_case - usar underscore no lugar de espacos ex. check_if_name_exist
* escreva em ingles

------ var -------
- global e local 
* hoisting         - eleva a variavel para antes do bloco cono undefined 
* existe e pode ser lido globalmente em todos os escopos
------ let -------
- local e block scope
* so existe e pode ser lido depois de declarado e no mesmo bloco
* pode ser 'portado' para um escopo inferior se declarado no escopo global
------ const -----
- local e block scope
* so existe no mesmo escopo
* imutavel
----------------------------------- string -------------------------------

var s = "nome_variavel"
var s = 'nome_variavel'
var s = `nome_variavel`

'eu estou usando' + r1 //concatenacao
`eu estou usando ${r1}` //template string com placeholder($)

s.Length  //faz uma contagem de caracteres da string
s.toUpperCase()  //converte para 'MAIUSCULA'
s.toLowerCase()  // converte para 'minuscula'

----------------------------------- number -------------------------------

33         - int(intergen)/ inteiros
3.6        - float(float point)/ reais
NaN        - Not a Number/ nao e um numero
Infinity   - infinito

var n = 5
var n = 5.8
var n = -5
var n = -5.9
var n = 5.0
var n = 0

> n.toFixed(2) //forca o numero para 2 casas decimais
> n.toFixed(2).replace('.', ',') //substitue o ponto por virgula

n.toLocaleString('pt-BR', {style: 'currency', currency: 'BRL'}) //formata o 'n' para a moeda especificada

---------------------------------- boolean --------------------------------

var b = true
var b = false

---------------------------------- null -----------------------------------
---------------------------------- undefined ------------------------------
---------------------------------- object ---------------------------------
---------------------------------- function -------------------------------

---------------------------------- conversao de tipos primitivos ---------------------------

> numero inteiro - Number.parseInt(n)
> numero real - Number.parseFloat(n)
> numero - tambem pode-se usar apenas Number(n)

> numero para string - n.toString()
> string - tambem pode-se usar apenas String(n)

------------------------------------ operadores e ordem de precedencia --------------------------- 

aritmeticos - +, -, *, /, %, **                       | () -> ** -> * -> ...
atribuicao - var n = 3, n = 5, n = n + 5, n += 5      | 
incremento - n++, n--, ++n, --n                       | >, <, >=, ...//nao possui precedencia
relacionais - >, <, >=, <=, ==, !=, ===, !==          |
logicos - !, &&, ||                                   | ! -> && -> ||
ternarios - ?, :                                      |
                                                      | ?, : //nao possui precedencia

------------------ aritmetica --------------

> * = soma                                | ()
> - = subtracao                           | 
> * = multiplicacao                       | **
> / = divisao fracionaria                 | 
> % = modulo ou resto da divisao          | *  /  %
> ** = exponenciacao ou potencia          | 
                                          | +  -

----------------- atribuicao ---------------

> var n = 5    -  atribuicao simples
> n = n + 4    - auto-atribuicao
> n += 5       - auto-atribuicao de soma simplificada
> n -= 5       - auto-atribuicao de subtracao simplificada
> n *= 5       - auto-atribuicao de multiplicacao simplificada
> n /= 5       - auto-atribuicao de divisao simplificada
> n **= 5      - auto-atribuicao de exponenciacao simplificada
> n %= 5       - auto-atribuicao de resto da divisao simplificada

---------------- encremento ----------------

var n = 10

n++           - ira somar 1 a variavel 'n'
n--           - ira subtrair 1 a variavel 'n'
--n           - ira pre-subtrair 1 a variavel 'n'
++n           - ira pre-somar 1 a variavel 'n'

-------------- relacionais -----------------

>             - maior que
<             - menor que
>=            - maior ou igual a
<=            - menor ou igual a
==            - igualdade
!=            - desigualdade
===           - igualdade restrita
!==           - desigualdade restruta

------ identidade ------

5 == 5        - true
5 == '5'      - true
5 === '5'     - false

------------- logicos ------------------------

!             - negacao (nenhuma)
&&            - conjuncao (e)
||            - disjuncao (ou)

---------------- tenarios --------------------

?             - true
:             - false

> var media = 5.5
> media > 7?'aprovado' :'reprovado'
<- 'reprovado'
------------------ function ---------------------

sao blocos de codigo que serao executadas apenas por eventos
ex.:

function acao(parametro){
    bloco
}

----------------- input ------------------------

<input type="button" value="click aqui" onclick="acao()"> - para criar um botao
<input type="number" name="n1" id="numero1"> - cria uma area interativa para numeros

------------------------------------------- condicionais -----------------------------------------

if (condition-true) {     | else (condition-false) {   | switch (expression) {              
}                         | }                          | }

------ tipos de condicoes -----------

   simple condition       compound condition      nested condition        multiple condition
        ↓                         ↓                      ↓                        ↓
  if (condition) {        if (condition) {        if (cond1) {            switch (express) {
    code block               code block              code block                case valor 1:
  }                       } else {                } else {                        code block
                             code block               if (cond2) {                break
                          }                            code block              case valor 2:
                                                      } else {                    code block
                                                         code block               break 
                                                      }                        default:
                                                  }                               code block
                                                                                  break
                                                                          }

---------------------------------------- repeticoes ou lacos ------------------------------------

estrutura de repeticao    estrutura de repeticao    estrutura de controle
com texte logico          com texte logico          com variavel de 
no inicio                 no final                  controle
          ↓                        ↓                        ↓
while (condition()) {     do {                      for (start;text;incr) {
    code block                code block                 clode block
}                         } while (condition())     }

------------ run through array ---------------
* to run through every element of an Array

let word = "john Santos";

for (const letter of word) {
	console.log(letter);
}
--------------------------------------------- array or 'lista' ---------------------------------------------

um array/variavel composta e uma variavel que tem varios elementos, cada elemento composto por um valor e por uma chave de identificacao

let a = ['aut1', 'aut2', 'aut3']
          0     1     2
  
               a             []              0,1,2...             'aut1', 'aut2', 'aut3'... 
               ↓              ↓                ↓                         ↓ 
             array         elemento         key/indice             conteudo/value

a[3] = 'aut4'   - adiciona um valor ao indice 3
a.push('aut4')  - outra maneira de adicionar um valor

a.length        - mostra a contagem de elementos de um array
a.sort()        - organiza os elementos em ordem crescente 
a[0]            - mostra o elemento indexado em 0
a.indexOf('aut3') - mostra o index de um elemento, se nao tiver retorna -1

pode-se usar 'in' no 'for' para simplificar um array

for (let count in a) {
    console.log(a[count])
}

------------------------------------------- object --------------------------------------------

let cadastro = {name:'jose', gender:'M', weigth:85.3, engordar(p){}}

cadastro  =  {'jose',    'M',      85.3,    [function]}
               nome     gender    weigth    engordar()

               cadastro      {}       name, gender, peso...        jose
                  ↓           ↓               ↓                      ↓
                  
cadastro.name    - retorna o valor presente no indice name dentro do objeto cadastro
-------------------------------------------- funcoes -------------------------------------------

funcoes sao -acoes- executadas assim que sao -chamadas- ou em decorrencia de algum -evento-
a funcao pode receber parametros e retornar um resultado

function action(param) {
    return result
}

action(5)

------------------------------------------------- DOM -------------------------------------------

DOM           - Document Object Model

--------- DOM Tree -------------

                                      window
                            ↓            ↓           ↓ 
                        location      document     history
                                         ↓ 
                                       html
                                     ↓      ↓
                                   head    body
                                ↓    ↓       ↓   ↓   ↓    
                              meta title    h1   p  div
                                                 ↓ 
                                              strong
------ selecionacao de elemento DOM --------------

----- by Tag ---------
getElementsByTagName()
----- by ID ----------
getElementByid()
----- by Name --------
gtElementsByName()
----- by Class -------
getElementByClassName()
----- by selector ----
querySelector()
querySelectorAll()
---------- ex.: ------
window.document.getElementByid('titulo');
var d = widow.document.querySelector('div#id_qualquer');


---------------------------------------- throw and try/catch -----------------------------------

//throw
function sayMyName(name = '') {
    if (name === '') {
        throw 'nome e obrigatorio' //interrompe a aplicacao e pega o erro
    }
    
    console.log('depois do erro')
}

//try...catch
try {
    sayMyName()        //se funcionar nao tera nenhum erro
    
} catch(e) {              //capitura o erro sem interromper a aplicacao
    console.log(e)
}

---------------------------------- selecionando conteudo do html pelo JS -------------------------

<p class="classe" id="identity"> frase </p>

document.getElementById('identity')             >> frase
    * permite selecionar um elemento pelo id
    * metodo mais seguro para manipular um elemento unico
    
document.getElementByClassName('classe')        >> frase
    * permite selecionar um elemento pela class
    * metodo que permite manipular varios elementos de uma so vez
    
document.getElementByTagName('p')               >> frase
    * permite selecionar um elemento pela tag
    * metodo que permite selecionar varios elementos pelas tags
    
document.querySelector('meta')
    * usa o querySelector para manipular uma tag
    * seleciona o primeiro que aparece
    * metodo mais versartil
    
document.querySelector('[src]')
    * usa o querySelector para manipular um elemento que possua src
    * seleciona o primeiro que aparece
    
document.querySelector('p.classe')
    * usa o querySelector para manipular um elemento de class dentro da tag p
    * seleciona o primeiro que aparece
    
document.querySelector('p#identity')
    * usa o querySelector para manopular um elemento de id dentro da tag p
    * seleciona o primeito que aparece

document.querySelectorAll('p#identity')
    * seleciona todos os elementos de id dentro da tag p
    * pode ser usado sem a referencia da tag
    * possui todas as propriedades usadas pelo querySelector
    * ex.:  '.'    :  class
            '#'    :  id
            '[]'   : busca a referencia listada
            ''     :   busca a tag listada
    
----------- tipos --------
getElementById              :Element
getElementByClassName       :HTMLcollection
getElementByTagName         :HTMLcollection
querySelector               :Element
querySelector               :NodeList

---------------------------------------- content manipulation -----------------------------------

<h1> my title </h1>

const element = document.querySelector('h1')
const header = document.querySelector('header')
const headerID = document.querySelector('#header')

//textContent
element.textContent += " hello" 
    *permite mudar ou adicionar um conteudo ao elemento selecionado pelo querySelector

    
//innerText
element.innerText = " hello" 
    * permite mudar o texto interno do html

    
//innerHTML
element.innerHTML = "<strong> hey there </strong>"
    * permite o uso de tags html dentro do string
    
    
//value
const element = document.querySelector('input')

element.value = "valor desejado"
    * permile adicionar uma valor 
    * permite verificar um valor ja adicionado no html
    * permite alterar o valor pre-existente
    
    
//attribute
header.setAttribute('id', 'header') 
    * permite adicionar ou atribuir um atributo ao html

headerID.getAttribute('id')
    * permite selecionar um atributo

header.removeAttribute('id')
    * permite remover um atributo
console.log(headerID) >> <header id="header"> - </header>
    
------------- alterando estilo no js -----------

const element = document.querySelector('body')

element.style.backgroundColor = "#000000"
    * permite mudar o style da pagina pelo js
    * so muda no local
    * a atribuicao deve ser feita entre ""

element.style.backgroundColor
    * seleciona os valores do style

// classList
element.classList.add('active')
    * adiciona uma class 
    
element.classList.remove('active')
    * remove a class
    
element.classList.toggle('active')
    * ira mudar o estado da class
    * de ativo para inativo
    * de inativo para ativo
    
--------------------------------- navegacao pelos elementos -----------------------------

const body = document.querySelector('body')

//parentNode, parentElement
body.parentNode
    * seleciona o no(node) pai(parent)
    * formato NodeList
    
    
body.parentElement
    * ira selecionar o elemento pai (parent)
    * formato element
    
    
//childNodes, children
body.childNodes
    * seleciona todos os no(node) filho(child)
    * formato nodeList
    * leva em consideracao os espacos vazis

body.children
    * seleciona todos os elementos filhos(children)
    * formato HTLMColection
    * nao leva em consideracao os espacos vazis

body.firstChild
    * seleciona o primeiro elemento filho
    * leva em conta espacos vazis
    
body.firstElementChild
    * seleciona o primeiro elemento filho
    * nao leva em conta espacos vazis
    
body.lastChild
    * seleciona o ultimo elemento filho
    * leva em conta espacos vazis
    
body.lastElementChild
    * seleciona o ultimo elemento filho
    * nao leva em conta espacos vazis
    
    
//Sibling, ElementSibling
body.nextSibling
    * seleciona os proximos elementos irmaos(sibling)
    * leva em consideracao o espaco vazio
    
body.nextElementSibling
    * seleciona os proximos elementos irmaos(sibling)
    * nao leva em consideracao os espacos vazis

body.previousSibling
    * seleciona os elementos irmaos(sibling) anteriores
    * leva em consideracao o espaco vazio
body.previousElementSibling
    * seleciona os elementos irmaos(sibling) anteriores
    * nao leva em consideracao os espacos vazis

    
-------------------------------------- criando e adicionado elementos -------------------------

const body = document.querySelector('body')

//createElement
const div = document.createElement('div');
div.innerText = "hello there"
    * criando uma div com um texto interno

//append
body.append(div)
    * adicionando a div como ultimo elemento do documento(depois do footer, se existir)
    
//prepend
body.prepend(div)
    * adicionado a div como primeiro elemento do documento(antes do header, se existir)
    
//insertBefore
const body = document.querySelector('body')
const script = body.querySelector('script')

body.insertBefore(div, script)
    * (elemento a ser adicionado, tag de referencia)
    * adiciona o elemento antes da tag de referencia

//para adicionar depois
const body = document.querySelector('body')
const script = body.querySelector('script')

body.insertBefore(div, script.nextSibling)
    * (elemento a ser adicionado, tag de referencia)
    * adiciona o elemento depois da tag de referencia
    * como nao existe um 'insertAfter' usa-se um pequeno truque aka.ganbiarra
    
    
-------------------------------------------------- eventos ---------------------------------------
                                     evento simples

--- html ---
<h1 onclick=|print()"> meu blog </h1>

--- js ---
function print() {
    console.log('print')
}
    
    * ira dispara o evento print() toda vez que o <h1> 'meu blog' for clickado
    * o evento disparado ira fazer um console log 'print'

                                     evento de teclado
                                     
--- html ---
<input type="text" onkeydown="function()">

--- js ---
const input = document.querySelector('input')

input.onkeydown = function() {
    console.log('teclado down')
}
    
    *ira disparar o evento function() toda vez que uma tecla for pressionada
    
                                     evento constante
                                
--- html ---
<h1> my blog </h1>

--- js ---
const h1 = document.querySelector('h1')

h1.addEventListener('click', print)

function print() {
    console.log('print')
}
    * dispara o evento pelo addEventListener
    * defina o evento pelo js nao pelo html
    * permite varios event listener 
    
                                            
                                            
//event
input.onkeypress = function(event) {
    console.log(event.key)
}

    * permite ler as propriedader do event
    * por exemplo qual key foi digitada
