 
---------------------------------------------- node.js -----------------------------------------
* backEnd
* frontEnd
* micro servicos
* APIs
    * webApps
    * mobile
    * desktop
* scripts e automacoes
* machine learning
* A.I

* nao recomendado para procecos com muito uso de CPU
    * muitas fotos ou videos
    * grandes aplicacao ou servicos
    
vantagens
    * rapido
        * execucao 
        * prototipacao
    * alta escabilidade
    * aplicacao de ponta
    * JS everywhere
    * ecosistema gigante
    * casos de uso
        * netflix
        * paypal
        * nasa
        * linkedin

oque e o node.js
    * JS Runtime Environment
        * anbiente de execucao do JS
    * nao e um framework nem uma linguagem

v8 js engine
    * interpretador de JS
    * criado em c++
    * focado para chrome, mas feito com compatibilidade com node.js em mente
    * nao possui DOM, console ou file system

NPM = node package manager

> node
    * para entrar no node console
> .exit
    * para sair do node console

__grossary:
    dependencies,
    packages
    modules
npm install -g npm
    * para atualizar a versao do npm
    
npm init
    * para iniciar a criacao de um module
    
json
    * javaScrip object notation
    
npm install package_name:
    * istala modulos externos
    
npm i package_name
    * atalho para npm install
    
npm i pachage_name -D
    * para istalar o package apenas para desenvosvimento
    * '-D' = devDependecies
    
npm i package-name package_name2 package_name3
    * para installar varios de uma vez

npm update
    * para atualizar as dependecias do package.json

npm install
    * ira trazer todos as dependencias nescesarioas para os modulos instalados
    
* nao se envial a pasta node_modules com o git
    * use o .gitignore para ignora a pasta e nao enviala

* nao editar ou deletar o package-lock.json
    * ele mapeia os modulos e dependencias

npm run 'script_name'
    * usado para rodar o script dentro do package.json
    
npm i package_name -g
    * instala o package de maneira global(todo o sistema)

npm root -g
    * mostra o root do npm no systema
    
npm uninstall package_name
    * para disistalar o package istalado de maneira global
    
significado das versoes:
    * ex.: "^2.29.1"
    * sig.: "major.minor.patch"
        * major: atualizao da versao, pode quebrar a versao anterior
        * minor: alteracoes seguras, nao vai quebrar a utilizacao
        * patch: correcao de bugs e problemas, sem possibilidade de quebrar a utilizacao
        
    * '~' atualizacao do patch
    * '^' atualizacao do minor
    * '2.29.1' nunca vai mudar a versao
    * '*' vai sempre mudar a versao

npm i package_name@package_version
    * altera a versao do projeto do package
    * ex.: npm i cfonts@1.33.2
        * instala o cfonts na versao 1.33.2
        
npm outdated
    * mostra a versao usada, desejada e ultima dos packages instalados
    
npm i package_name@latest
    * instala a ultima versao de um package instalado

------- process --------
process.sdtout.write()
	* to print in the screen

process.sdtin.on()
	* to keep read what is hapening and response as coded for

process.on()
	* to read and answer what is coded for

process.exit()
	* to end a process runing

------ timers -------
setTimeout
	* usado para rodar a funcao apos x milissegundos
clearTimeout
	* usado para anular um timeOut
setInterval
	* usado para executar uma funcao n vezes, com um intervalo de x milissegundos entre as execucoes
	* ira rodar indefinidamente
clearInterval
	* usado para canselar um setInterval registrado
