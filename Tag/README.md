# TAG
O commits recebem uma tag para identificar uma versão do projeto.
Podem ser criadas tags anotadas ou tags leves. As tags anotadas são recomendadas, pois elas contém mais informações sobre a tag, como por exemplo, quem criou a tag, quando foi criada, uma mensagem e o hash do commit que a tag aponta.

## Criar uma tag
### TAG lightweight
Marca uma tag na versão onde voce esta
``` 
git tab <nomeTag>
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