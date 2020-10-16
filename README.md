# aws-stream-kinesis
#### Instalando o AWS CLI
```
apt install awscli
```
#### Criando um streaming atraves do terminal
```console
AWS_ACCESS_KEY_ID=X AWS_SECRET_ACCESS_KEY=X aws --endpoint-url=http://localhost:4567 kinesis create-stream --stream-name Foo --shard-count 1  --region eu-west-1
```
#### Verificando todos os streams de uma regiao
```console
AWS_ACCESS_KEY_ID=X AWS_SECRET_ACCESS_KEY=X aws --endpoint-url=http://localhost:4567 kinesis list-streams --region eu-west-1
```
#### Verificando a criaçao do streaming
```console
AWS_ACCESS_KEY_ID=X AWS_SECRET_ACCESS_KEY=X aws --endpoint-url=http://localhost:4567 kinesis describe-stream-summary --stream-name Foo --region eu-west-1
```
#### Postando Mensagem
```console
AWS_ACCESS_KEY_ID=X AWS_SECRET_ACCESS_KEY=X aws --endpoint-url=http://localhost:4567  kinesis put-record --stream-name Foo --partition-key 123 --data testdata --region eu-west-1
```
