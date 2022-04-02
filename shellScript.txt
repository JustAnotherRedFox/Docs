========================= Shell Script ==========================

criacao de arquivo shell script:
touch shellArchive.sh && chmod +wrx shellArchive.sh && vim shellArchive.sh

criar, permitir execucao e abrir o arquivo

para executar o arquivo usa-se sh ou diretamente aponta para o arquivo ex:
1: sh ./shellArchive.sh
2: ./shellArchive.sh

modelo de archivo

#!/bin/zsh    
os # fazem comentarios, a linha acima mostra ao script qual o interpretador usar ex.:zsh, bash

-- commands --
os arquivos shell permitem usar comandos terminais
ex.: whoami, uptime, pwd, echo

echo: printa na tela uma string ou variavel
whoami: mostra o usuario logado atualmente
uptime: mostra algumas informacoes do sistema
pwd: mostra o caminho absoluto da pasta atual

-- variaveis --
definicao de variavel:
#importante nao separar o '=' do valor ou da variavel
variavel="valor_da_variavel"

uso da variavel:
echo "a variavel possui o valor: $varivel"

#pode-se usar o '\' para anular o proximo caracter
#pode-se usar o '\n' para quebrar para a proxima linha

guardar comando em uma variavel:
#pode-se usar '$()' para guardar um comando em uma variavel
variavel=$(top)

-- input de usuario --
#usa-se 'read' para ler um input do usuario
#inportante colocar o colon(:) depois do read
echo "digite o nome: "
read nome_usuario;
echo $nome_usuario

-- condicional --
#simples
if [condicao];
then
    code block
fi

#composto
if [condicao];
then
    code block
else
    code block
fi

#if, else, elif
if [condicao];
then
    code block
elif[condicao];
then
    code block
        .
        .
        .
else
    code block
fi

#case
case $variavel in 
caso_1)
    code block
    ;;
caso_2)
    code block
    ;;
esac

-- loop de repeticao --
#loop for
for num in {10..0};
do
    echo "$num"
done     

#loop while
while [condicao];
    do
        block code
    done

-- funcoes -- 
nome_da_funcao() {
    code block
}  

ex.:
main() {
    echo "hi, there"
}

-- argumentos --
$0 - contem o nome do script executado
$1 ... $n - contem os argumentos em ordem em que foram passados
$# - contem o numeros de argumentos passados
$* - retorna todos os argumetos de uma so vez

-- parametros --
n: comprimento e diferente de zero
z: comprimento e zero
=: igual a
!=: diferente de
-eq: possui o mesmo valor que
-ne: nao possui o mesmo valor que
-gt: maior que
-ge: maior ou igual a
-lt: menor que
-le: menor ou igual a
e nome_do_arquivo: verifica se existe
d nome_do_arquivo: verifica se e um diretorio
f nome_do_arquivo: verifica se e um arquivo regular(texto, imagem, programa, docs, etc...)
