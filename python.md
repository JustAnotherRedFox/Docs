------------------------------ caracteristica do python -----------------------------------------

* Case-sensitive    #Maiusculo e Minusculo faz diferenca
* sequencial        #O codigo e lido sequecialmente
* Dynamic typed     #AS variaveis aceitam todos os tipos independente do type atual
* Unicode           #aceita o padrao de caracteres unicode
* orientada a objeto #aceita os paradigmas OOP(Object Oriented Programing)
* orientada a script #pode ser usada para automatizar tarefas via script
* multiparadigma     #aceita varios tipos de paradigmas como: OOP, functional, imperative, interpreted, etc.
* interpretada       # usa um interpretador

- Buit-in Data types
    - text type:
        * str(string)

    - numeric type:
        * int(intergen)
        * float(float point)
        * complex

    - sequence type:
        * list
        * tuple
        * range

    - mapping type:
        * dict

    - set type:
        * set
        * frozenset

    - boolean type:
        * bool

    - binary type:
        * bytes
        * bytearray
        * memoryview

--------------------------- python basic commands ---------------------------------

print()                - mostra na tela o texto ou valor dentro
print(f"{}")           - permite colocar uma variavel no meio do texto
print('''''')          - permite usar espacos e quebras de linhas no meio da funcao
print('{}'.format())   - permite usar um placeholder
print('phase', end='') - stop the default newline

input()					- to receive a keyboard input
input('question: ')     - to print a message and receive a keyboard input
input().upper()[0]      - to receive a filtered input, .upper() = to upperCase, [0] = only the char of index 0
int(input())            - to cast a input to one especific data type e.g.: int(input()), str(input()), float(input())

#       - para comentarios de uma linha
''''''  - para comentarios de mais de uma linha
\n      - para quebras de linha

type()  - mostra o tipo de dado
index() - mostra o index de uma lista

------------------------- Variables ---------------------------------

sao nomes simbolicos que guardam um valor
- definicao de variavel
    * no python nao existe palavra chave para definir uma variavel
    * ela e feita de maneira direta, guardando o valor diretamente na variavel
    * ex.: var_name = var_value

* podem comecar com 'letras' ou '_'
* nao podem comecar com numeros
* pode-se usar letras, numeros e acentos
* nao podem conter espacos
* nao podem conter palavras reservadas ex.: 'if', 'while', 'def', 'in', 'is'..
* escolha nomes coerentes
* camelCase: usar upperCase inves de espaco
    UpperCamelCase: usar upperCase no inicio. recomendado para nome de classes
    lowerCamelCase: usar lowerCase no inicio. usado para a maioria das variaveis

* snake_case: usar underscore no lugar do espaco
* e recomendado escrever o codigo em ingles

--------------------------------- string ----------------------------------

var = 'var_name'
var = "var_name"
var = """var_name"""
var = '''var_name'''


'im using' + var  #concatenation
"i'm using {}".format('a placeholder') #with the method 'format()'

len(var)     #contagem de caracteres
var.upper()  #convert the string to uppercase
var.lower()  #convert the sting to lowercase

var.isupper() #verify if the variable is uppercase
var.islower() #verify if the variable is lowercase
var.isspace() #verify if the variable is only space
var.isalpha() #verify if the variable only contains letters
var.isnumeric() #verify if the variable only contains numbers
var.isalnum() #verify if the variable contain only numbers and letters

------------------------------ numbers ---------------------------------

33     - int(intergen)
3.4    - float(float point)

var = 4.5
var = 33
var = -3
var = -3.4

f'{var:.2f}'  #converte um numero para 2 casas decimais

int(var)      #converte o numero para inteiro
float(var)    #converte o numero para real
str(var)      #converte o numero para string

----------------------------- boolean ---------------------------------

var = True
var = False

sao representado por True e False Captalized

--------------------------------- function -----------------------------------------

para definir uma funcao usa-se 'def'

def funcion_name:
    pass   #usa-se 'pass' para deixar uma zona livre pra edicao posterior sem interferir com o codigo

usa-se return quando se quer que algo retorne da funcao

-------------------------------------- operadores e ordem de precedencia -------------------

aritimeticos = +, -, *, /, %, **     | () -> ** -> * -> / -> // -> % -> + -> -
atribuicao =   =, +=, -=...          |
relacionais = >, <, >=, <=, ==...    |
logicos = not, or, and               |

--------------------- aritmeticos -----------------

> +  = soma
> -  = subtracao
> *  = multiplicacao 
> /  = divisao
> // = divisao inteira
> %  = modulo  da divisao ou resto
> ** = exponenciacao ou potencia

----------------- atribuicao ---------------------

> var = 5       - atribuicao simples
> var = var + 1 - auto-atribuicao 
> var += 1      - auto-atribuicao simplificada

---------------- relacionais --------------------

>      - maior que
<      - menor que
>=     - maior ou igual a
<=     - menor ou igual a
==     - igual a 
!=     - diferente de

---------------- logicos ------------------------

not    - negacao(contrario, negativo, nao)
or     - conjuncao(ou, este ou o outro, True or False)
and    - disjuncao(e, este e o outro, True and True)

---------------------------------- condicionais ----------------------------------
if condition-True:       |   elif condition-True:       | else:

----- tipos de condicoes ------

simple condition     compound condition     nested condition          minimal statement

if condition:        if condition:              if condition:         if B else C
    statement           statement                   statement
                     else:                      else:
                        statement                   if condition:
                                                        statement
                                                    elif condition:
                                                        statement
                                                    else:
                                                        statement

------------------------------------ loops ------------------------------------------
while True:
	statement
		Break
	
while codition:
	statement
	
for i in tuple_name:
	statement

for i, v in enumerate(values):						#will search the index and value
	print(f'on index{i} was find the value{v}.')
	
# greater than and less than
numbers = [10, 2, 3, 7, 9, 1]
greater = 0
lesser = 0

for c in numbers:
	if c == 0:
		greater = lesser = c
	else:
		if c > greater:
			greater = c
			
		if c < lesser:
			lesser = c
------------------------------------ Tuples ---------------------------------------
* Tuplas sao variaveis constantes ou seja imutaveis 

## Basic Manipulation
lunch = ('rice', 'soda', 'salad', 'meat') #to define a tuple
or
lunch = 'rice', 'soda', 'salad', 'meat' #can be defined withou parentesis

del(lunch)   #delete the tuple from memory, work for any variable

## Reading
print(lunch)			#will print the whole tuple
lunch[1]         #the element of index 1
lunch[-1]    #the last element
lunch[1:3   #from the element 1 to element 3 except for element 3 
lunch[:2]     #from first element to element 2 except for element 2 
lunch[2:]    #from element 2 to last element
sorted(lunch)      #tuple will be sorted in alphabetic order
lunch.index("soda") #will show the index of "soda"

---------------------------------- Lists -------------------------------------
* Listas sao variaveis compostas similaris a tuplas, porem mutaveis

## Basic Manipulation
lunch = ['rice', 'soda', 'salad', 'meat'] 	#to define a list with the especified values
numbers = list(range(4, 11)) 				#define a list using the method 'list' with the values from 4 to 10(using method range)

lunch[2] = 'juice'			#change the value of specified index
lunch.append('cookie')   #append the item to the end of the list, a.k.a adding a new item
lunch.insert(0, 'bread') #insert the item in the specified index, deslocating all others item to the right

del lunch[3]			#remove a item by index using the command del
lunch.pop()				#remove the last item
lunch.pop(3)			#remove a item by index using the method pop()
lunch.remove('meat')    #remove the first occurrence of a item by value

numbers.sort()			#will sort the values in ascending order
numbers.sort(reverse=True)	#will sort the values in descending order
len(numbers)				#get the lenght(number of items) of the list

## Link and Duplicates
a = [1, 3, 4, 7]
b = a				# B is being linked to A, acting as reference, so the changes in B will affect A
c = a[:]			# C is inheriting all values in A, so C is just a copie of A
	
## Composed Lists
person = ['john', 19]		
people = []
people.append(person[:])		#append a copy of person inside people, people become: [['john', 19]]
person[0] = 'mary'				#change the value of person index 0
person[1] = 60					#change the value of person index 1
people.append(person[:])		#append a copy of person inside people, people become: [['john', 19], ['mary', 60]]
....
people = [['jj', 20], ['hh', 54], ['cj', 34]] 	#composed list can also be created like this

print(people[0])    $['jj', 20] #print the list of index 0 inside the list people
print(people[0][0]) $jj 		#print the item of index 0 in list of index 0
------------------------------ Libraries -------------------------------------
* import libName   						# import the full library
* from libName import funcName			# import only a function from a library

# Random Lib
* Import Random       

random.choice(seq)   					#Return a random element from the non-empty sequence seq.
random.randint(a, b) 					#Return a random integer N such that a <= N <= b.
random.seed(a=None, version=2)			#Initialize the pseudo-random number generator.
