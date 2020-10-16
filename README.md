# aws-stream-kinesis

#### Instalando o kinesis via docker
```
docker run -d -p 4567:4567 vsouza/kinesis-local --port 4567 --createStreaMs 5
```
#### Instalando o AWS CLI
```
apt install awscli
```
#### Criando um streaming atraves do terminal
```
AWS_ACCESS_KEY_ID=X AWS_SECRET_ACCESS_KEY=X aws --endpoint-url=http://localhost:4567 kinesis create-stream --stream-name Foo --shard-count 1  --region eu-west-1
```
#### Verificando todos os streams de uma regiao
```
AWS_ACCESS_KEY_ID=X AWS_SECRET_ACCESS_KEY=X aws --endpoint-url=http://localhost:4567 kinesis list-streams --region eu-west-1
```
#### Verificando a criaçao do streaming
```
AWS_ACCESS_KEY_ID=X AWS_SECRET_ACCESS_KEY=X aws --endpoint-url=http://localhost:4567 kinesis describe-stream-summary --stream-name Foo --region eu-west-1
```
#### Postando Mensagem
```
AWS_ACCESS_KEY_ID=X AWS_SECRET_ACCESS_KEY=X aws --endpoint-url=http://localhost:4567  kinesis put-record --stream-name Foo --partition-key 123 --data testdata --region eu-west-1
```
