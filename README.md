## Verificação de instalação
git --version

## Configuração de Usuario
Configurar usuario do git
git config --global user.name "Seu nome"
git config --global user.email "seuemail@gmail.com"

Retorna usuario/email do git
git config --global user.name
git config --global user.name

Retorna as demais configuraçoes do git
git config --list

Muda o editor padrao do git bash(vim)
git config --global core.editor "code --wait"

Muda o editor padrao do git
##Repositorio Local
inicia uma pasta de arquivos em /.git/ que contrala o versionamento do arquivos.
git init

Renomear o nome da Branch
git config --global init.defaulBranch <novoNome>

Retorna oque foi addicionado ou mudanças nos arquivos
git status

Adiciona um arquivo especifico
git add <file>

Adiciona todos os arquivos modificados
git add --all
git add .
git add -A

Remove o arquivo adicionado no rastreamento do Git
git rm --cached <file>

Remove todos arquivos adicionados no rastreamento 
git rm --cached -r .

Envia um Comit a branch seguida por uma mensagem
git commit -m "initial commit"
git commit -m "titulo do commit" -m "descricao"

Diferença entre arquivos modificado entre o arquivo commitado
git diff

Diferença entre arquivos staged e arquivos comitados
git diff --cached
git diff --staged

## Historioco de commits
Listagem do commits que foram feito, em ordem decrescente.(indetificador feito por SHA-1)
git log

Listagem de commits com o hash e cometarios do commit
git log --oneline

Lista os ultimos commits de forma limitada.
git log <numeros de commits>
git log -2

Traz a listagem da ultimos commits e as differenças que acontecerão
git log -p
git log --patch

Traz a listagem da ultimos commits e as modificaçoes
git log --stat
Traz a modificaças que foram feitas e os commits de forma abreviada
git log --shortstat

Renomear o commit anterior
Subistui o commit anterior e escrevendo um novo com outro hash de indetificaçãogi
git commit --amend -m "Novo commit"
Subistui o commit anterior sem alterar os comentarios
git commit --amend --no-edit

Altera o commit anterior com o editor padrao(vim) que pode ser alterado tambem
git commit --amend

Navega entre as linha do tempo dos commits anteriores
git checkout <hash>
Volta na ultima versao da branch
git checkout <nome da Branch>

Volta na ultima versao do arquivo no head
git checkout <file>

Remove arquivo não rastreaveis
git clean -f

podem ser usado para restaurar para ultima versao.
git checkout .
git clean -f

Remove do arquivos em staged (add)
git rm --cached <file>

Remove os arquivos em staged (add) na linha do tempo
git restore --staged <file>

Remove todos arquivos modificados da area de modified e staged
git reset --hard

##Git ignore
Cria um arquivo .gitignore
touch .gitignore

todos arquivos bmp sao ignorados
*.bmp
Ignora arquivos especificos
#<file>
https://github.com/github/gitignore

Atualiza o controle do git sobre os arquivos
git update-index --skip-worktree <file>
git update-index --no skip-worktree <file>


## Git Clone

git clone <arquivo> <nome do Arquivo Novo Clonado>

git clone <origen do repositorio>

## Git com repositorios

Para saber se tem um repositorio vinculado
git remote -v

Anexa um repositorio a um arquivo git ja existente
HTTPS git remote add <origin> <https://github.com/Usuario/nomeDoArquivo>

Alteraçao do repositorio
git remote set-url origin <https://github.com/Usuario/novoNomeDoArquivo>





Abre um pagina web com comandos do git log
git log --help




## Remover o repositorio
Não deve ser feito a não ser se vc for um profissional habilitado.
rm -fr .git/


Ciclo de vida dos arquivos

Untracked(não rastrado)
Unmodified(não modificado)
Modified(modificado)
Staged(preparado)

Exemplos:
Untracked--(add)-->Staged
Modified--(add)-->Staged
Staged--(commit)-->Unmodified

