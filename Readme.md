Oiee, estou criando este projeto para aprender a usar o git e github! 

Após a criação do arquivo, entrei com o Git Bash e digito o comando 'git init', ele configura o diretório atual para ser rastreado pelo Git, inicializando um repositório vazio.

    repositório vazio = ainda não há commit
    - commit são versões no arquivo
    
    comando.gitinit.png

segundo comando: git add
ele manda os arquivos para area de staging, assim o git add realmente não afeta o repositório de forma significativa pois as alterações não são realmente registradas até que você execute git commit
 
  - caso queira adicionar todos os arquivos e atualizaões use 
    git add .
  - caso seja um específico use
    git add "nome do arquivo"

git status
ele mostrar as mudanças a serem atualizadas ("na fila")

git commit 
 git commit -m "titulo do commit"

git branch -m "main"
 comando para renomear a branch principal para "main"
 > foi mostrado este comando pois o git está mudando sua nomeclatura

git checkout 
Alterne entre as branch ou restaure os arquivos da working tree
 > no exerc trocamos da branch main para a nova branch ("novo-botao") e com o checkout mudamos de branch, assim tudo será mudado apenas na nova branch ("novo-botao")
  