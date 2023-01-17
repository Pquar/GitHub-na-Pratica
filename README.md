# Principais Comandos Git
### Verificar se o Git esta instalado
``
   git --version
``
## Configuração de Usuário
Configurar usuário do git 

``
git config --global user.name "Seu nome" 
``

``
git config --global user.email "seuemail@gmail.com"
``

Retorna usuário/email do git

``
git config --global user.name
``

``
git config --global user.name
``



Retorna as demais configurações do git

``
git config --list
``

Muda o editor padrão do git bash(vim) para Visual Studio code

``
git config --global core.editor "code --wait"
``


## Repositório Local

Inicia uma pasta de arquivos em /.git/ que controla o versionamento do arquivos.

``
git init
``

Renomeá o nome da Branch

``
git config --global init.defaultBranch <novoNome>
``

Retorna oque foi adicionado ou mudanças nos arquivos

``
git status
``

Adiciona um arquivo especifico

``
git add <file>
``

Adiciona todos os arquivos modificados

``
git add --all
``

``
git add .
``

``
git add -A
``

Remove o arquivo adicionado no rastreamento do Git

``
git rm --cached <file>
``

Remove todos arquivos adicionados no rastreamento 

``
git rm --cached -r .
``

Envia um Commit a branch seguida por uma mensagem

``
git commit -m "initial commit"
``

``
git commit -m "titulo do commit" -m "descrição"
``

Diferença entre arquivos modificado entre o arquivo comitato

``
git diff
``

Diferença entre arquivos staged e arquivos comitatos

``
git diff --cached
``

``
git diff --staged
``

## Histórico de commits
Listagem do commits que foram feito, em ordem decrescente.(identificador feito por SHA-1)

``
git log
``

Listagem de commits com o hash e cometários do commit

``
git log --oneline
``

Lista os últimos commits de forma limitada.

``
git log <números de commits>
``

Exemplo:
``
git log -2
``

Traz a listagem da últimos commits e as diferenças que acontecerão

``
git log -p
``

``
git log --patch
``

Traz a listagem da últimos commits e as modificações

``
git log --stat
``

Traz a modificação que foram feitas e os commits de forma abreviada

``
git log --shortstat
``

### Renomear o commit anterior
Subsistiu o commit anterior e escrevendo um novo com outro hash de identificação

``
git commit --amend -m "Novo commit"
``

Substitui o commit anterior sem alterar os comentários

``
git commit --amend --no-edit
``

Altera o commit anterior com o editor padrão(vim) que pode ser alterado também

``
git commit --amend
``

Navega entre as linha do tempo dos commits anteriores

``
git checkout <hash>
``

Volta na ultima versão da branch
``
git checkout <nome da Branch>
``

Volta na ultima versão do arquivo no head

``
git checkout <file>
``

Remove arquivo não rastreáveis

``
git clean -f
``

podem ser usado para restaurar para ultima versao.

``
git checkout .
``
``
git clean -f
``

Remove do arquivos em staged (add)

````
git rm --cached <file>
````

Remove os arquivos em staged (add) na linha do tempo
````
git restore --staged <file>
````
Remove todos arquivos modificados da area de modified e staged
```
git reset --hard
```

## Git ignore
Cria um arquivo .gitignore
```
touch .gitignore
```
todos arquivos bmp sao ignorados
*.bmp
Ignora arquivos especificos
 #<file>
Mais sobre o .gitignore em: https://github.com/github/gitignore

Atualiza o controle do git sobre os arquivos
```
git update-index --skip-worktree <file>
git update-index --no skip-worktree <file>
```


## Git Clone
```
git clone <arquivo> <nome do Arquivo Novo Clonado>

git clone <origen do repositorio>
```
## Git com repositórios

Para saber se tem um repositorio vinculado
```
git remote -v
```
Anexa um repositório a um arquivo git ja existente
```
HTTPS git remote add <origin> <https://github.com/Usuario/nomeDoArquivo>
```
Alteração do repositório
```
git remote set-url origin <https://github.com/Usuario/novoNomeDoArquivo>
```




Todos os camandos com git 
```
git log --help
```



## Remover o repositório
Não deve ser feito a não ser se vc for um profissional habilitado.
```
rm -fr .git/
```

## Ciclo de vida dos arquivos

Untracked (não rastreado)

Unmodified (não modificado)

Modified(modificado)

Staged(preparado)

---

Exemplos:

Untracked--(add)-->Staged

Modified--(add)-->Staged

Staged--(commit)-->Unmodified

