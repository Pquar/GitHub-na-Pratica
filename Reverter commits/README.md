### Reverter commits
O git revert não deleta o commit so faz um novo commit revertendo as alterações do commit.
```
git revert <hashCommit>
```
Reverter o ultimo commit.
```
git revert HEAD
```

### Desfazer commits
O git reset remove o commit e as alterações do commit.
```
git reset --hard HEAD~<numeroCommitsParaReverter>
```
Exemplo: Reverter o ultimo commit. 
```
git reset --hard HEAD~<1>
```
Volta o commit e as alteração permanecem na area modificadas.
```
git reset --mixed HEAD~<numeroCommitsParaReverter>
```
Volta o commit e as alteração permanecem na area de preparação.
```
git reset --soft HEAD~<numeroCommitsParaReverter>
```