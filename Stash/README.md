### Git Stash
Git Stash serve para salvar as alterações que você fez no seu código, mas ainda não quer dar commit.
O commando git stash salva as alterações na memoria do git.
```	
git stash
```
O git stash list mostra as alterações salvas.
```
git stash list, quanto maior o numero mais antigo e mais recente é o numero menor. 
```
O git stash apply aplica as alterações salvas. Aplica o ultimo stash salvo.
```	
git stash apply
```
Aplicar um stash especifico.
```
git stash apply stash@{numero}
```
Aplicar um stash especifico e remove-lo da lista.
```
git stash pop stash@{numero}
```
Remova um stash especifico.
```
git stash drop stash@{numero}
```
Aplicar um stash a um branch especifico.
```
git stash branch <nomeBranch> stash@{numero}
```

O git reset --hard remove as alterações salvas.
```
git reset --hard
```
