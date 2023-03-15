# GIT 
                                   
* working directory
	> onde fica todos os arquivos
	> working tree
* stage area
	> preparacao dos arquivos, para o commit
	> index
	> stage tree
* repository[local]
	> banco de dados dos arquivos
	> onde ficaram os pontos na historia ou historico

## criando um novo repositorio

* $git init
	> cria ou reinicia um repositorio git
* $git add .
	> adiciona todos os arquivos para a stage area
* $git add archive.txt                                    
	> adiciona um arquivo especifico(in this case 'archive.txt) a stage area
* $git commit -m "Title" -m "Message"                               
	> prepara todos os arquivos da fila para serem enviados
* $git branch -M main                                     
	> Cria a branch principal chamada main
* $git remote add origin <link.git>                       
	> cria uma conecção com o repositorio remoto
* $git push -u origin main                                
	> envia os arquivos do 'commit' para o repositorio remoto
* $git pull origin main				       
	> puxa os arquivos do repositorio remoto para o local
* $git clone <link.git>                                   
	> clona um diretorio remoto
* $clear                                                  
	> limpa o terminal

* $git remote set-url                                     
	> muda a URL de um remote ja existente, pode mudar de https para ssh ou vice-versa
* $git remote -v                                          
	> verifica a conecção remote
* $git remote rename <old_name> <new_name>                
	> renomeia a conecção remote
* $git remote rm <remote_name>                            
	> remove a URL do remote indicado
* $git config --global user.name 'user_name'              
	> configura o nome de usuario 
* $git config --global user.email 'user_email'            
	> configura o email do usuario

 
* $ssh-keygen -t ed25519 -C "your_email@example.com"      
	> gera uma nova ssh key
* Enter a file in which to save the key (/home/you/.ssh/id_ed25519): [Press enter]
* Enter passphrase (empty for no passphrase): [Type a passphrase]
* Enter same passphrase again: [Type passphrase again]
* $eval "$(ssh-agent -s)"                                 
	> inicia o ssh agent
* Agent pid 59566
* $ssh-add ~/.ssh/id_ed25519                              
	> adiciona a ssh key ao ssh agent

* $git log                                                
	> mostra o log de commits
* $git log --oneline                                      
	> filtra o log de commit de maneira resumida
* $git log -n 5                                           
	> filtra os ultimos 5 logs de commits
* $git log --since=aaaa-mm-dd                             
	> filtra o log a partir da data especificada
* $git log --until=aaaa-mm=dd                             
	> filtra o log ate a data especificada
* $git log --author=author_name                           
	> filtra o log pelo nome do autor
* $git log --grep="commit_name"                           
	> filtra o log pelo nome do commit
* $git rm --cached <file>                                 
	> remove um arquivo commitado do stage area
* $git diff                                               
	> conpara as modificacao entre o stage area e repositorio
* $git rm <file>                                          
	> remove um arquivo do repositorio local
* $git mv <file> <new_name>                               
	> renomeia um arquivo
* $git mv <file> <folder/file>                            
	> move o arquivo

* $git restore <file>                                     
	> restaura as modificacoes 
* $git restore --staged <file>                            
	> restaura os arquivos na stage area

* $git clean -n                                           
	> mostra quais untracked files irao ser permanentemente apagado
* $git clean -f                                           
	> permanentemente apaga untracked files
* $git revert HEAD~5                                      
	> ira recuperar commits anteriores em forma de uma novo commit
* $git show <5e9c8f9d66>                                  
	> mostra todas as modificacoes de um commit
* $git rm -r --cached .                                   
	> limpa todos os arquivos cached para usar o gitignore
