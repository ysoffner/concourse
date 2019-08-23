#### How-To Concource
Clonar esse exemplo basico 
```
git clone https://github.com/ysoffner/concourse
cd concourse
```
Iniciar o docker-compose (postgres e concourse)
```
docker-compose up -d
```
Executar o login com o fly (concourse-cli)
```
./fly -t local login -c http://127.0.0.1:8080 -u test -p test
```
Criar uma pipeline
```
./fly -t local set-pipeline \
    --pipeline my-pipeline \
    --config pipeline.yml
```