# jarbas
Automação do ambiente de desenvolvimento.
# Steps
## Step 1
```
docker-compose -f env_devel.yaml up -d
```
## Step 2
```
screen -S devel -d -m -t shell bash
```
## Step 3
Aqui criamos um screen para cada um dos containers.
``` 
screen -S devel -X screen -t docker exec -t -i app-env bash
screen -S devel -X screen -t docker exec -t -i celery-env bash
screen -S devel -X screen -t docker exec -t -i node-env bash
screen -S devel -X screen -t docker exec -t -i shell-env bash
```
## Step 4
Depois inserirmos o usuário na sessão ``` screen -r user ```.
# Primeira versão
```
apt-get install screen
```
Ler mais sobre (docker)[[https://docs.docker.com/compose/gettingstarted/]].
# Referencias
- (GNU Screen)[https://en.wikipedia.org/wiki/GNU_Screen] - (Site oficial)[https://www.gnu.org/software/screen/]
- (Docker)[https://www.docker.com/what-docker]
