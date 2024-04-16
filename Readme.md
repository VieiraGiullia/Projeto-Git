## Criar um projeto novo

* Criar um novo arquivo `README.md`

* Escrever dentro dele `Oiee, estou criando este projeto para aprender a usar o git e github!`

* Salva o arquivo

Após a criação do arquivo, entrei com o Git Bash e digito o comando `git init`, ele configura o diretório atual para ser rastreado pelo Git, inicializando um repositório vazio.

    repositório vazio = ainda não há commit
    - commit são versões no arquivo
    
![<alt-imagem dos comandos>](<E:\Programação\alura\projeto git-github\img\comando.gitinit.png>)

segundo comando: git add

 > Esse `add` é necessário antes de darmos o commit de fato

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

![<alt-imagem dos comandos>](<"E:\Programação\alura\projeto git-github\img\comando.gitaddGitstatus.png">)

 ## Repositório no Github

* Para passar o commit do meu repositório local (da minha máquina) para um repositório na plataforma do Github, usamos o `git remote add origin <link do repositório>`

* `origin` é o nome utilizado para referenciar o nosso repositório

Agora já temos o nosso repositório local conectado com o respositório do Github, porém o `commit` que damos na máquina não sobe automaticamente para a plataforma

* Para isso precisaremos empurrar, enviar para lá com o `git push -u origin main`

Agora se recarregarmos a página iremos ver o nosso arquivo aqui na plataforma!


## Alterando e adicionando arquivo

* Além disso iremos criar um novo arquivo `Projeto.md`, onde escreveremos `o projeto será desenvolvido aqui`

* Agora então precisamos subir essa alteração, pra isso seguiremos os mesmos passos de `git add .` (agora ponto `.` pois adiciona todos os arquivos) e `git commit -m "Primeira alteração"`

* Lembrando que para alterar algo no nosso respositório do Github precisamos dar o push, então `git push origin main` (sem o -u)

Se olharmos agora o nosso código no Github, ele terá sido alterado, e não só isso, se clicarmos no nome do `commit`, podemos ver exatamente as alterações que foram feitas nele.
O verde com `+` e o vermelho com `-` mostra, os conteúdos que foram adicionados e editados dentro do código.
No botão do arquivo 'commitado' poderemos ver todos os commits já feitos anteriormente, então se clicarmos em algum deles, veremos exatamente o que havia sido alterado, além de claro, vermos o código como era.

## Branch

git checkout 
Alterne entre as branch ou restaure os arquivos da working tree
 > no exerc trocamos da branch main para a nova branch ("novo-botao") e com o checkout mudamos de branch, assim tudo será mudado apenas na nova branch ("novo-botao")

caso queira voltar para a branch main, digite no git bash
git checkout "nome da branch"

![<alt-imagem dos comandos>](<"E:\Programação\alura\projeto git-github\img\comandogitcheckout.png">)

<img scr="E:\Programação\alura\projeto git-github\img\comandogitcheckout.png">

## Merge

git merge
O comando permite que você pegue as linhas de desenvolvimento independentes criadas pelo git branch e as integre em uma ramificação única

## Clone

Como vocês podem baixar meu código?

Sempre que você entrar em um repositório, seja o seu ou o de qualquer outra pessoa, terá esse botão `Code`, que quando você clica aparece um link:

<img src="https://media.discordapp.net/attachments/812313742192279612/836823564513705994/unknown.png">

* Você irá copiar esse link e levar ele lá pro nosso terminal

* O comando para puxar o projeto para a sua máquina é o `git clone https://github.com/rafaballerini/GitTutorial.git`

Não é necessário criar um repositório antes disso, como fizemos anteriormente com o `git init`. Dessa vez, basta abrir o terminal e clonar o projeto e tudo aparecerá!

## Pull

E se eu fizer uma alteração no repositório, como vocês podem atualizar na máquina de vocês?

* Basta vocês executarem o comando `git pull`, ele irá puxar todas as alterações feitas no repositório do Github para o seu repositório local

## Fork

Mas Rafa quando eu fiz o clone do seu repositório ele não apareceu no meu Github.
Existe a ferramenta `fork`, que é bem mais simples para fazer isso
Você só precisa apertar nesse botão dentro do repositório e TCHANAM! Ele aparece automaticamente lá na sua conta:

<img src="https://media.discordapp.net/attachments/831974152667398214/836826687634407434/unknown.png">

## Pull request

O último conceito que quero ensinar para vocês é o de Pull Request, vamos entender como ele funciona:

* Após você ter dado um fork no projeto e ele ter ido pra sua conta, você poderá alterar o projeto e adicionar as funcionalidades que deseja

* Você pode por exemplo dar um fork no meu repositório de `Formulário` para adicionar uma validação de campos ou qualquer outra coisa que acha válido

* Depois disso, você poderá salvar o projeto, dar o `git add .`, `git commit -m "validação de botões"` e `git push origin main`

Quando você for olhar o seu Github, verá que existe uma mensagem parecida com a seguinte:

<img src="https://media.discordapp.net/attachments/831974152667398214/838990983852458035/unknown.png">

Isso significa que a branch do seu repositório está 1 commit "na frente" da branch original

O que você deve perceber agora é esse botão que aparece em seguida:

<img src="https://media.discordapp.net/attachments/831974152667398214/838991711249235998/unknown.png">

Ele servirá para caso você deseje enviar para o dono do repositório original uma solicitação de pull, ou seja, fazer com que ele puxe as alterações que você fez no seu repositório para o repositório dele, original

Ao clicar nesse botão, você será direcionado para uma página que fará a avaliação se esse `pull request` terá conflitos ou não com o código no repositório original. Caso não tenha, bastão clicar no botão de `Create pull request`

<img src="https://media.discordapp.net/attachments/831974152667398214/838992584893399100/unknown.png">

Você irá colocar um nome intuitivo, que demonstre a funcionalidade adicionada e o ideal é que você também crie uma boa descrição do que desenvolveu, não somente explicando o que é, mas ensinando ao dono do repositório original a forma como ele poderá testar também

Depois disso, basta esperar para que o dono da branch original aceite o seu pull request