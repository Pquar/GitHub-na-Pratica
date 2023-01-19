# TAG

O commits recebem uma tag para identificar uma versão do projeto.
Podem ser criadas tags anotadas ou tags leves. As tags anotadas são recomendadas, pois elas contém mais informações sobre a tag, como por exemplo, quem criou a tag, quando foi criada, uma mensagem e o hash do commit que a tag aponta.

## Criar uma tag

### TAG lightweight

Marca uma tag na versão onde voce esta

```
git tab <nomeTag>
```

### TAG em versão especifica(antiga)

Marca uma tag em uma versão especifica

```
git tag <nomeTag> <hashCommit>
```

Tag anotada

```
git tag -a <nomeTag> -m "mensagem" <hashCommit>
```

ou

```
git tag -a -m  "mensagem" <nomeTag> <hashCommit>
```

### TAG anotada

Leva um rastreio de quem criou a tag, quando foi criada, uma mensagem e o hash do commit que a tag aponta.

```
git tag -a <nomeTag> -m "mensagem"
```

ou

```
git tag -a -m  "mensagem" <nomeTag>
```

Para visualizar todos as tags

```
git tag
```

ou

```
git tag --list
```

Visualizar as tags de forma mais detalhada

```
git tag -n
```

Para visualizar uma tag especifica

```
git show <nomeTag>
```

### Enviar tags para o repositório remoto

Envia uma tag especifica

```
git push origin <nomeTag>
```

Todas as tags

```
git push --tags
```

### Navegar entre tags
Navegar entre tag e nada mais que navegar entre commits, pois as tags são apenas um ponteiro para um commit.
```
git checkout <nomeTag>
```
Outra coisa que podemos fazer e ver a diferença entre duas tags
```
git diff <nomeTag1> <nomeTag2>
```

### Deletar uma tag
Deleta uma tag local
```
git tag -d <nomeTag>
```
Deleta uma tag remota
```
git push --delete origin <nomeTag>
```