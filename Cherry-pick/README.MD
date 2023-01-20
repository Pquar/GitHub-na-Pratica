# Cherry pick
Cherry pick é uma forma de pegar um commit de uma branch e aplicar em outra branch.
```	
git cherry-pick <hashCommit>
```

# Bisect
Busca binaria, o bisect é uma forma de encontrar um commit que causou um problema.
Falamos que vamos começar a busca binaria.
Coloca a ultimo commit que não tem o problema como bom.
Coloca o commit que tem o problema como ruim.
```
git bisect start
git bisect good <hashCommit>
git bisect bad <hashCommit>
```
Se a busca resulta em um commit bom, digite:
```
git bisect good
```
Se a busca resulta em um commit ruim, digite:
```
git bisect bad
```
Para para a investigação, digite:
```
git bisect reset
```