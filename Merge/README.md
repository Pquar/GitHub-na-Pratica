# Merge
Merge serve para unificar os commits de duas branches diferentes.
user o commando 
```
git merge <branch>
```
Para unificar as branches, a unificação deve ser feita dentro da branch que voce quer unificar.
Exemplo: estou na branch main e quero unificar a branch develop entoa, então uso git merge develop.

Como saber quais branch's ainda não foram margeadas
```
git branch --no-merged
```
Quais branch foram mergeadas a onde estou?
```
git branch --merged
```
## Problemas com merge
Quando se tenta merger duas branches que possuem commits diferentes, o git não sabe qual commit deve ser mantido, então ele cria um commit de merge.(merging)
Normalmente o conflito e resolvido na mão, mas o git tem uma ferramenta para ajudar a resolver o conflito.
para abortar o merge
```
git merge --abort
```
ou reset o merge
```
git reset --hard
```

## Rebase
Rebase serve para unificar os commits de duas branches diferentes.
user o commando 
```
git rebase <branch>
```
