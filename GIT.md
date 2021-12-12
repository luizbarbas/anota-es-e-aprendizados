# Como utilizar o GIT :computer:



**comandos básicos**

- **CD** - abre o diretório

- **CD**  ..- volta ao diretório anterior

- **MKDIR** - cria um diretório

- **DIR** - mostra os diretórios existentes

- **RMDIR** - remove o diretório

--------------------------------------------//--------------------------------------

**SHA** - é uma forma curta de representar um arquivo de forma encriptada com um conjunto de 40 caracteres.

- para saber o sha do arquivo digite no GIT - 'open ssl sha1 <nome do arquivo>

-------------------------------------------//----------------------------------------

**BLOB/ TREE/ COMMIT**

BLOB - contém metadados do GIT como tipo de objeto, tamanho e etc...

TREE - armazena os blobs, as trees podem apontar para blobs ou para outras trees. quando o sha de um blob muda por exemplo todos os blobs e trees também mudam o sha.

COMMIT - os commits possuem as trees e blobs e também possui um sha. O commit identifica o autor das alterações.

-------------------------------------------//----------------------------------------

**Chave SSH**

No GIT BASH digite:

ssh -keygen -t ed25519 -C <email>

após ir ao diretório ssh:

cd /c/users/nome do diretório/.ssh

após:

cat id_ed25519.pub (copiar a chave gerada e colar no GITHUB)

voltar ao GIt e digitar:

eval $(ssh -agent -s)

após:

ssh -add id_ed25519 

-------------------------------------------//----------------------------------------

**Iniciando o GIT**

na pasta que deseja usar aperte o botão direito e clique em GIT Bash here.

ao iniciar digite "GIT INIT"

- adicionando uma identificação no GIT

git config --global user.email <email>

git config --global user.name <apelido>

GIT add *

GIT commit -m "commit inicial"

o repositório está pronto para ser usado e copiado para o github

-------------------------------------------//----------------------------------------

**EMPURRANDO DO GIT PARA O GITHUB**

git remote add origin <link>

git push origin master

<sempre que algo for incluido ou alterado dar 'git add .' antes de commitar