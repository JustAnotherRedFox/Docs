----------------------- terminal ---------------------
command (-parameter) {argument}

wildcards:
  > * = substitue um ou mais caracteres, ex.: rm ./*.jpg = remove do diretorio atual todos os .jpg
  > ? = substitue um caracter, ex.: rm ./aula_?? = remove do diretorio atual todos as pastas que terminam com dois digiteos qualquer
  > [] = usado para selecionar intervalos, ex.: [a-z, A-z, 0-9] seleciona todos os arquivos nestes intervalos de letras
  > {} = usado para selecionar padroes, ex.: {hr, conf, jp} ira selecionar todos os arquivos que possuem estes padroes especificos

arg for applications:
	> -b
		* e.g picom -b 
		* allowed a application to run as daemon, then the shell will not freese nor will the app stop when the terminal is closed
permicoes:
  > chmod +x nome_do_arquivo
	* da permicao de execucao(execute) a um arquivo
  > chmod +w nome_do_arquivo
        * da permicao de escrita(write) a um arquivo
  > chmod +r nome_do_arquivo
        * da permicao de leitura(read) a um arquivo

alterar terminal:
  > update-alternatives --config x-terminal-emulator
	* permite escolher um terminal padrao

para verificar imformacoes de um aplicativo:
  > xprop
  
para verificar informacoes de execucao e uso do sistema
	> htop
	> ps

para aplicar as alteracoes dentro do arquivo .Xresources:
  > xrdb ~/.Xresources

AUR packages:
  - sem AUR helper:
	> git clone URL-package
	> cd URL-package && makepkg -si
  - com AUR helper:
	- se nao possui yay:
	  > git clone https://aur.archlinux.org/yay.git
	  > cd yay && makepkg -si
  	- se possui yay:
	  > yay -S package_name

para saber o shell:
    > ps -p$$ -ocmd=
    > $BASH_VERSION, $ZSH_VERSION ...
    > $SHELL

para modificar as comfiguracoes de monitor:
    > xrandr
	* mostra os monitores conectados
    > xrandr --output HDMI-1 --off
	* desativa o output selecionado (HDMI-1)

para monitorar o sistema:
    > ps -e
	* mostra todos os processos ativos 
    > top
	* monitora os processos ativos e uso dos recursos do sistema
    > htop
	* versao melhorada e colorida do top

para tirar screeshots:
    > import -window root ./screenshot.jpg
	* precissa do app ImageMagik
	* tira um screenshot da tela atual
	* quarda a screenshot na pasta atual com o nome screeshot.jpg

para colocar um wallpaper
    > feh --bg-scale /path/to/wallpaper


manipulacao basica do sistema:
  > sudo su
	* muda para user root
  > pwd
	* mostra o caminho absoluto para o diretorio atual
	* Stand for Print Work Directory
  > ls
	* lista os arquivos do diretorio especificado
	* -l = mostra de uma forma longa, como data e tipo dos arquivos
	* -a = mostra todos os arquivos incluindo os ocultos
	* -h = mostra os numeros de forma Human readable, dividindo em MB, GB ...
	* -R = mostra os diretorios de forma recursiva
	* -S = ordena por tamanho
	* Stand for List
  > cd
	* muda de diretorio
	* ./ = diretorio atual, ../ = diretorio parent, -/ = diretorio por onde veio
	* / = diretorio root, ~/ = diretorio home
	* Stand for Change Directory 
  > cp
	* copia arquivos
	* -r = copia recursivamentes pastas
	* Stand for CoPy
  > rm
	* remove arquivos
	* -r = remove recurcivamente, -f = remove forcado
	* -rf = pode ser usado para remover diretorios com arquivos dentro
	* Stand for ReMove
  > mv
	* move arquivos e pastas
	* pode ser usado para renomear arquivos e pastas
	* Stand for MoVe
  > mkdir 
	* remove um diretorio vazio
	* -p = cria os diretorios parents se estes nao existirem
	* Stand for MaKe DIRectory
  > rmdir
	* remove um diretorio vazio
	* Stand for ReMove DIRectory
  > touch
	* altera registro de data e hora de um arquivo ou pasta
	* cria um ou mais arquivos
  > cat
	* seleciona o conteudo de um arquivo e mostra no output padrao, o terminal
  > less
	* seleciona o conteudo de um arquivo e mostra em um arquivo de paginacao
  > file
	* mostra o tipo de arquivo
  > stat
	* mostra o dono, as modificacoes e o tamanho do arquivo

nomeclatura dos diretorios:
./   - diretorio atual
../  - diretorio anterior
~/   - diretorio home
/    - diretorio root



--- debian based ---
> apt install item_name
    * instala os programas listados
    
> apt search search_term
    * pesquisa o termo listado
    
> apt update && apt upgrade
    * atualiza o sistema e os programas nele
    
> apt remove item_name
    * remove o item listado
    
> apt autoremove 
    * remove todas as dependecias nao nescessarias

--- arch based ---
pacman -S <pkg>
    * instala os programas listados
    
pacman -Rsc <pkg>	
	* unstall the pakeges and it's unneeded dependencies
	
pacman -Qdt
	* list unneeded packages

pacman -Rns $(pacman -Qdtq)
	* remove unneeded packages
	
pacman -Gs search_term
pacman -Ss <pkg>
    * pesquisa o termo listado

pacman -Syu
    * atualiza o sistema e os programas nele
