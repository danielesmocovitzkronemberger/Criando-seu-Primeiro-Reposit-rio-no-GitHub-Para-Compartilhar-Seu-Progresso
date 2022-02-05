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



