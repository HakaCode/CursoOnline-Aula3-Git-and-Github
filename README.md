
# O que é o git?

![logo do git](https://github.com/natalyapeixoto/git-and-github/blob/master/git.jpeg)

Git é um __sistema de controle de versões__ , usado principalmente no desenvolvimento de software.
 O Git é um software livre, foi inicialmente projetado e desenvolvido por Linus Torvalds para o desenvolvimento do kernel Linux.



# O que é o GitHub?

![logo do github](https://github.com/natalyapeixoto/git-and-github/blob/master/github.jpg)

GitHub é uma plataforma de hospedagem de código-fonte com controle de versão usando o Git. Ele permite que programadores ou qualquer usuário cadastrado na plataforma contribuam em projetos privados e/ou Open Source de qualquer lugar do mundo.


## Linha de comando 


![linha de comando](https://github.com/natalyapeixoto/git-and-github/blob/master/linha-de-comando.png)


### Comandos mais usados:
* ls - list (lista todos os arquivos presentes no diretório MAC/LINUX)
* dir - list(Windows) 
* dir /b - mostra lista de maneira simplificada
* pwd - Present working directory (MAC/LINUX)
* cd - change directory 
* cd ~ - volta para a raiz
* cd .. - volta uma pasta 
* cd nome-da-pasta - para entrar em uma pasta 
* code . - abre o visual studio code na pasta local. 
* mkdir nome-da-pasta - para criar uma pasta
* history - mostra histórico de comandos (LINUX)
* f7 - history no Windows


## Instalação do Git 

O git já vem instalado na maioria dos computadores Mac e Linux, se for o seu, apenas digite na linha de comando: git --version
Caso esteja instalado, esse comando mostrará a versão do git.

tutorial: https://woliveiras.com.br/posts/instalando-o-git-windows/

* git para mac: https://git-scm.com/download/mac
* git para windows: https://gitforwindows.org/
* git para plataformas Linux/Debian, como o Ubuntu: digite na linha de comando ````sudo apt-get install git ```` 


### Git configuração

Para adicionar usuário:

```
git config --global user.name "Natalya Peixoto"
git config --global user.email “natalya_peixoto@hotmail.com” 
```

Para remover usuário:

```
git config --global --unset user.name "Natalya Peixoto"
git config --global --unset user.email “natalya_peixoto@hotmail.com” 
```

## Criar conta e perfil no GitHub

[link GitHub](https://github.com/)

Lembre-se que o github é onde as empresas vão ver seu trabalho. 
Então mantenha tudo organizado e use bom senso na hora de escolher seu nome de usuário.


## Subindo projeto local para o GitHub

* Criar novo repositório no seu github e dar nome a ele. 
* no sua máquina, pela linha de comando, vá até a pasta do projeto. 
* dentro da pasta do projeto rode o comando: ````git init```` (pasta git oculta é criada)
* ````git add .```` para adicionar todos os arquivos que estão na sua pasta de uma vez, caso queria adicionar apenas um digite ````git add caminho-do-arquivo````
* ````git commit -m"mensagem para explicar o que voce fez no código"```` 
* ````git remote add origin url-que-voces-copiaram-do-github````
* ````git remote -v```` mostra as url que o git está apontando
* ````git push origin master```` 

#### Files stages (Estágios do arquivo)

* *untracked files* nao deu instrução ao git do que fazer com or arquivo
* *changes to be committed* adicionou, mas não deu o commit
* *commited*  commit foi feito


## Git Clone

serve para baixar, na sua máquina, um projeto que está hospedado no github.

* Acesse o repositório do projeto que quer baixar 
* clicar no botão ```` clone or download ```` 
* copiar url 
* Na sua máquina abra a linha de comando e vá até a pasta onde deseja colocar o projeto
* rode o comando: ```` git clone url-do-repositorio ```` 

## Branch 

Branch significa, galho, ramificação. 
Usando branches podemos trabalhar paralelamente nos projetos sem alterar a versão principal(master).
![branch](https://github.com/natalyapeixoto/git-and-github/blob/master/branch.png)


* ````git checkout -b nome-da-branch```` cria uma nova branch e entra nela
* ```` git branch ```` mostra as branchs que existem no projeto/repositório, destacando a branch atual
* ````git checkout nome-da-branch```` para mudar de branch


#### git pull 

como diz o nome, para __puxar__ atualizações de uma branch remota para a branch atual(local). 
```` git pull origin master```` atualiza a branch que você está trabalhando com a master. 


## Pull request (a famosa PR)

Na Pull request, você está simplesmente solicitando ao responsável(ou responsáveis) do repositório aprovação para que as alterações que você fez sejam integradas. 
Na pull request, precisamos escrever o que fizemos. 
Cabe ao responsável aceitar, negar, pedir correções, fazer um code review da sua solicitação e etc. 

## Git Merge

Merge acontece quando pegamos duas branchs diferentes e juntamos o código. 
Muitas vezes, existem partes diferentes nesses arquivos, nesse momento 
existe um conflito que deve ser resolvido.


## Readme.md MARKDOWN

Arquivo essencial para todo repositório no github. 
onde explicamos o projeto e damos algumas instruções, caso necessário. 

https://guides.github.com/pdfs/markdown-cheatsheet-online.pdf

## Fork 

cria uma cópia de um repositório qualquer no seu github.

![fork](https://github.com/natalyapeixoto/git-and-github/blob/master/fork.png)

#### trabalhando com o fork:

* No repositório 'forkado' no seu github pegue a url e dê um clone na sua máquina
* trabalhe à vontade 
* Terminou? ``git add .`` , ``git commit -m''`` . 
* Mas antes de darmos o push, algumas configurações são necessárias. 
* ````git remote -v```` para vermos para onde estamos enviando e de onde estamos pegando arquivo. 
* Note que só estamos enviando e recebendo do nosso próprio repositório. 
* Caso o respositório raiz tenha sofrido alterações, não vamos conseguir pegá-las. Precisamos mudar isso. 
* ````git remote add upstream url-do-repositorio-que-voce-forkou````
* ````git remote -v```` novamente. Agora podemos ver algo como: 

```
origin  https://github.com/natalyapeixoto/labcar.git (fetch)
origin  https://github.com/natalyapeixoto/labcar.git (push)
upstream        https://github.com/denisecaze/labcar.git (fetch)
upstream        https://github.com/denisecaze/labcar.git (push)
```
- o 'upstream' se refere ao projeto original que foi forkado. 
- já o 'origin' é o seu repositório. 

* Ainda antes do push, vamos ver se tem alguma mudança que precisamos pegar. 
* ````git pull upstream master```` 
* Agora damos o ````git push origin master````

* Feito isso, vamos no nosso github, no repositório forkado, vamos ver a informação que está em amarelo na foto abaixo:

![fork](https://github.com/natalyapeixoto/git-and-github/blob/master/forked.png)

'This branch is 1 commit ahead of nome-do-usuário:branch'.
e então, vamos clicar em pull request. 



### links úteis:

* https://medium.com/reprogramabr/git-e-github-por-onde-come%C3%A7ar-ca88a783c223 -> Medium Reprograma. Escrito por Thaylla <3 

* https://git-scm.com/book/pt-br/v1/Primeiros-passos-Sobre-Controle-de-Vers%C3%A3o -> Documentação oficial do git em português. 

* https://rogerdudler.github.io/git-guide/index.pt_BR.html -> git - guia prático 

* https://dillinger.io/ -> Markdown preview (ajudinha para fazer o README.md)

