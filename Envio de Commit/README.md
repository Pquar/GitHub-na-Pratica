## Forçando o envio
força o envio de um commit, mesmo que ele não esteja atualizado com o repositório remoto.
```
git push --force
```
Força o envio de um commit, mesmo que ele não esteja atualizado com o repositório remoto, mas verifica se o repositório remoto não foi atualizado. Garanti que nenhuma alteração sera perdida. 
```
git push --force-with-lease
```

## Traz mudanças do repositório remoto
Traz mudanças do repositório remoto para o repositório local.
```
git pull
```

### Rebase
O rebase pega as alterações do repositório remoto (alterações de outra branch)e aplica no repositório local. (Altera o histórico do repositório local)
```
git rebase <Branch>
```
OBS: O rebase não deve ser usado em branch's que já foram enviadas para o repositório remoto ou repositórios públicos.
Leva alterações do repositório remoto para o repositório local e aplica no repositório local. (Altera o histórico do repositório local)
```
git pull --rebase
```

Pega Vários commit's e transforma e um so commit.
```
git rebase --interactive ~HEAD~<numeroCommitsParaReverter>
```
Exemplo: Pega os 3 últimos commit's e transforma e um so commit.
```
git rebase --interactive ~HEAD~<3>
```
- pick = pega o commit, 
- squash = pega o commit e transforma em um so commit.
- reword = pega o commit e altera a mensagem do commit.
- edit = pega o commit e permite alterar o commit.
- fixup = pega o commit e transforma em um so commit, mas não altera a mensagem do commit.
### Trazes informações do repositório remoto
Trazes informações de uma branch no repositório remoto para o repositório local.
```
git fetch origin develop
``` 
Traz informações de todas as branch' s do repositório remoto para o repositório local.
```	
git fetch
```