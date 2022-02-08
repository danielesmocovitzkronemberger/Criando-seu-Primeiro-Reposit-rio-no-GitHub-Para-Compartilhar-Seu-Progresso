# Iniciando o Git e criando um commit

 ## Criando um repositório 

##### Seguindo passo a passo do professor

##### 1 - Usar a pasta criada na aula de terminal "workspace"

###### Usando o Git Bash

Dani@Dani-PC MINGW64 ~
$ cd c:
Dani@Dani-PC MINGW64 /c
$ ls - para listar as pastas
Dani@Dani-PC MINGW64 /c
$ ls
'$Recycle.Bin'/             NVIDIA/                       Users/
'$WINDOWS.~BT'/             PerfLogs/                     Windows/
'$Windows.~WS'/            'Program Files'/               WirelessDiagLog.csv
'Arquivos de Programas'@   'Program Files (x86)'/         dell/
'Documents and Settings'@   ProgramData/                  hiberfil.sys
 ESD/                       Recovery/                     pagefile.sys
 Intel/                    'System Volume Information'/   workspace/
Dani@Dani-PC MINGW64 /c
$ cd workspace
Dani@Dani-PC MINGW64 /c/workspace (main)
$ crtl +l = limpar a tela
Dani@Dani-PC MINGW64 /c/workspace (main)
$ mkdir resumo-aula-git - para criar uma pasta 
Dani@Dani-PC MINGW64 /c/workspace (main)
$
Se não aparecer nada é que deu certo
Dani@Dani-PC MINGW64 /c/workspace (main)
$ cd resumo-aula-git
Dani@Dani-PC MINGW64 /c/workspace/resumo-aula-git (main)
$
Dani@Dani-PC MINGW64 /c/workspace/resumo-aula-git (main)
$ git init 
 git init - para poder inicializá-lo e possibilitar que o GIT comece de fato a gerenciar e a versionar o nosso código
Initialized empty Git repository in C:/workspace/resumo-aula-git/.git/
Essa mensagem diz: "olha foi inicializado um repositório vazio dentro de C:/workspace/resumo-aula-git/.git/
Dani@Dani-PC MINGW64 /c/workspace/resumo-aula-git (master)
$
Dani@Dani-PC MINGW64 /c/workspace/resumo-aula-git (master)
$ls 
Dani@Dani-PC MINGW64 /c/workspace/resumo-aula-git (master)
$
Vai aparecer que não tem nada dentro da pasta, mas na verdade se  reparar no que GIT retornou, ele tá falando que dentro de "C:/workspace/resumo-aula-git/.git/" tem uma outra pasta chamada ".git" e porque que ela não está aparecendo? Ela não está aparecendo, porque esssa pasta é uma pasta oculta, ela é uma pasta gerencial do GIT, onde fica todo código do GIT e ele versiona os objetos que a gente vai estar manipulando, e como ver está a pasta com a flag -a
Dani@Dani-PC MINGW64 /c/workspace/resumo-aula-git (master)
$ list -a 
./  ../  .git/
Dani@Dani-PC MINGW64 /c/workspace/resumo-aula-git (master)
$ cd .git/
Dani@Dani-PC MINGW64 /c/workspace/resumo-aula-git/.git (GIT_DIR!)
$ ls
HEAD  config  description  hooks/  info/  objects/  refs/
Dani@Dani-PC MINGW64 /c/workspace/resumo-aula-git/.git (GIT_DIR!)
$cd .. voltar para a pasta resumo-aula-git

--------------------------------------------------------------------------------
Antes temos que fazer a configuração inicial, se é a primeira vez que você tá usando o GIT, ele vai pedir algumas configurações, ele vai pedir de fato seu "user name", um name e um email, que são usados no github, quando o objeto "commit" é criado, ele é criado com um autor? Então é exatamente isso que a gente vai fornecer. Para que lá na frente quando gere o "commit" ele tenha um autor atrelado a ele. Então a gente vai rodar o seguinte comando: "git config --global"...
Dani@Dani-PC MINGW64 /c/workspace/resumo-aula-git (master)
$ git config --global user.email "danikronen@gmail.com"
Dani@Dani-PC MINGW64 /c/workspace/resumo-aula-git (master)
$
Dani@Dani-PC MINGW64 /c/workspace/resumo-aula-git (master)
$ git config --global user.name danielesmocovitzkronemberger
Dani@Dani-PC MINGW64 /c/workspace/resumo-aula-git (master)
$
Podemos fazer essa configuração de forma global, ou apenas para esse repositório.

Então agora já está feito a configuração inicial que o GIT iria pedir para gente caso a gente esquecesse de configurar isso.

##### 2 -Adicionando um arquivo - Criar um arquivo com a extensão markdown- usamos extensão .md

 VAmos usar um tipo de arquivo diferente chamado Markdown.
Markdown é nada mais é do que uma forma mais humana de se escrever um arquivo HTML, então para colocar textos de tamanhos diferentes nós temos a tags HTML:"h1,...h6", e transpondo isso para o Markdown,´para escrever um título grande, um título de nível um, coloca antes do texto uma hashtag  "#"  significa que está  usando o h1,  se colocar duas hashtags "##" significa que está usando o h2, e assim sucessivamente. 

O Markdown é uma forma humanizada de se escrever HTML sem que voçê tenha que entender como que o HTML funciona de fato.

Ir na pasta resumo-aula-git e criar um arquivo "resumo" com o typora

Agora realizar o "commit" desse arquivo
Dani@Dani-PC MINGW64 /c/workspace/resumo-aula-git (master)
$ git add *
Dani@Dani-PC MINGW64 /c/workspace/resumo-aula-git (master)
$git commit -m "commit incial"
-m é uma flag no commit, "..."e passar uma string(um texto)
Dani@Dani-PC MINGW64 /c/workspace/resumo-aula-git (master)
$ git commit -m "commit inicial"
[master (root-commit) da9b68d] commit inicial
 1 file changed, 84 insertions(+)
 create mode 100644 resumo.md
O professor disse na aula anterior, os commits que eles são os objetos do git que dão significado as alterações? E que esses objetos em si, carregam uma mensagem de texto, juntamente com outros metadados como o autor.. a hora que o commit foi criado...então é essa mensagem que vamos escrever agora. "commit inicial".
Depois que tiver acesso a essa lista de alterações, consegue facilmente indentificar qual arquivo que adicionamos, qual commit foi feito, e até mesmo ter acesso a essa mensagem curta para conseguir entender o que aquele commit significa dentro das nossas alterações, dentro no nosso projeto.
E acima ele traz algumas informações como: A master e o início de um número que fizemos já lá atrás da9b68d esses números são os números iniciais do "sha1", lembrar de objetos, que cada objeto ele passa por esse algoritimo de encriptação que gera esses caracteres indentificadores de 40 dígitos, que é o "sha1", ai está esse caractere indentificando esse commit realizado.
Até aqui aprendemos a criar um repositório, a iniciar a estrutura do git, para que ele comece a versionar de fato código, primeiro contato com o markdown, e está feito o commit inicial do nosso projeto.



Ciclo de vida dos arquivos no Git
Passo a passo no ciclo de vida
Git Init
Esse comando além de criar aquela pasta ".git/", ela inicializa um conceito do git chamado "repositório", quando usamos o "git init" estamos de fato criando um repositório dentro de um diretório, dentro de uma pasta.
.... voltar no começo da aula
Dani@Dani-PC MINGW64 /c/workspace/resumo-aula-git (master)
$mkdir aulagitgithub
Dani@Dani-PC MINGW64 /c/workspace/resumo-aula-git (master)
$ ls
aulagitgithub/  resumo.md
Dani@Dani-PC MINGW64 /c/workspace/resumo-aula-git (master)
$ mv resumo.md ./aulagitgithub
mv - serve para mover um arquivo para uma pasta
Dani@Dani-PC MINGW64 /c/workspace/resumo-aula-git (master)
$ git status
On branch master
Changes not staged for commit:
  (use "git add/rm <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)

        deleted:    resumo.md
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        aulagitgithub/
no changes added to commit (use "git add" and/or "git commit -a")
 .... voltar nessa parte pra entender melhor
Dani@Dani-PC MINGW64 /c/workspace/resumo-aula-git (master)
$ git add resumo.md aulagitgithub/
Dani@Dani-PC MINGW64 /c/workspace/resumo-aula-git (master)
$
Dani@Dani-PC MINGW64 /c/workspace/resumo-aula-git (master)
$ git status
On branch master
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        renamed:    resumo.md -> aulagitgithub/resumo.md
Dani@Dani-PC MINGW64 /c/workspace/resumo-aula-git (master)
$ git commit -m "cria pasta aulagitgithub, move arquivos resumo para aulagitgithub"
[master 220be0c] cria pasta aulagitgithub, move arquivos resumo para aulagitgithub
 1 file changed, 17 insertions(+), 1 deletion(-)
 rename resumo.md => aulagitgithub/resumo.md (72%)
Dani@Dani-PC MINGW64 /c/workspace/resumo-aula-git (master)
$
Dani@Dani-PC MINGW64 /c/workspace/resumo-aula-git (master)
$ git status
On branch master
nothing to commit, working tree clean
Dani@Dani-PC MINGW64 /c/workspace/resumo-aula-git (master)
$ echo > README.MD
Dani@Dani-PC MINGW64 /c/workspace/resumo-aula-git (master)
$ ls
README.MD  aulagitgithub/
Dani@Dani-PC MINGW64 /c/workspace/resumo-aula-git (master)
$ git status
On branch master
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        README.MD
nothing added to commit but untracked files present (use "git add" to track)
Dani@Dani-PC MINGW64 /c/workspace/resumo-aula-git (master)
$
Abrir o arquivo README.MD no typora e digital a introdução como se fosse a capa.
Dani@Dani-PC MINGW64 /c/workspace/resumo-aula-git (master)
$ git status
On branch master
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        README.MD

nothing added to commit but untracked files present (use "git add" to track)
Dani@Dani-PC MINGW64 /c/workspace/resumo-aula-git (master)
$ git add *
warning: LF will be replaced by CRLF in README.MD.
The file will have its original line endings in your working directory
Dani@Dani-PC MINGW64 /c/workspace/resumo-aula-git (master)
$ git status
On branch master
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   README.MD
Dani@Dani-PC MINGW64 /c/workspace/resumo-aula-git (master)
$ git commit -m "adiciona index"
[master afe9dfe] adiciona index
 1 file changed, 8 insertions(+)
 create mode 100644 README.MD
Dani@Dani-PC MINGW64 /c/workspace/resumo-aula-git (master)
$
voltar na aula 

Resolvendo Conflitos
Como os conflitos acontecem no Github e como resolvê-los
Fazer alteração no meu README.MD