## Branch
Branch e uma ramificação no projeto que permite que funcionalidades sejam desenvolvidas separadamente sem impactar funcionalidades estáveis no projetos.

## Comandos
### Lista e Mostra as branch's do projeto
```
git branch 
```
ou
```
git branch --list
```
### Criar uma nova branch
---
Criar uma nova branch
```
git branch <nomeBranch>
```
Mudar para uma branch
```
git checkout <nomeBranch>
```
Cria uma nova branch e muda para ela
```
git checkout -b <nomeBranch>
```
---
### Switch
Mudar para um branch ja existente
```
git switch <nomeBranch>
```
ao usar novamente o comando switch ele volta para a ultima branch
```
git switch -
```
Criar uma nova branch e muda para ela
```
git switch -c <nomeBranch>
```
---
### Mudança de branch
Muda para uma branch sem seguir com mudanças pendentes na branch atual e desfaz o trabalho não comitato adicionando as mudanças na branch no estado de staged. Caso tenha mudanças não rastreadas pelo git voce pode levar as mudanças para outra branch.
```
git checkout -f <nomeBranch>
```


## Remover ou Deleta uma branch
```
git branch -d <nomeBranch>
```
Força a remoção da branch
```
git branch -D <nomeBranch>
```
Remover uma branch remota
```
git push origin --delete <nomeBranch>
```
## Renomear uma branch
```
git branch -m <nomeBranch> <novoNomeBranch>
```
se voce estiver dentro da branch
```
git branch -m <novoNomeBranch>
```

Para alterar um nome de branch remoto e deletada a branch remota e cria uma nova branch com o novo nome. lembrando que precisa notificar os demais que também estão trabalhando na branch.

### Enviar a branch para o repositório remoto
Caso não tenha enviado a branch para o repositório remoto, voce pode usar o comando abaixo para enviar a branch para o repositório remoto.
```
git push --set-upstream origin <nomeBranch>
```
ou
```
git push -u origin <nomeBranch>
```
### Fetch
Baixa as branch's do repositório remoto para o repositório local. Porem não faz o merge com a branch local.
```
git fetch
```