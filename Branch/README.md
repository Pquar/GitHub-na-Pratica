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


Deleta uma branch
```
git branch -d <nomeBranch>
```

### Enviar a branch para o repositório remoto
Caso não tenha enviado a branch para o repositório remoto, voce pode usar o comando abaixo para enviar a branch para o repositório remoto.
```
git push --set-upstream origin <nomeBranch>
```
ou
```
git push -u origin <nomeBranch>
```