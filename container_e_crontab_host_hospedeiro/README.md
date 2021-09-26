# Iremos criar um container que irá rodar internamente o crontab para executar uma determinada tarefa

### Note que neste caso, o container terá o fuso horário setado para ficar semelhante a minha máquina local e ficará rodando pra executar a tarefa, mas não dependerá do crontab do host hospedeiro, rodará completamente isolado do host.

###Iremos seguir os seguintes passos:

- Cria o container

- Atualiza os pacotes

- Instala os pacotes necessários na máquina

- Seta no host hospedeiro o comando para execução da tarefa


### Para rodar scripts pelo container usando a máquina local, use uma regra como:

_O primeiro bloco inicia o container, o segundo executa a tarefa, o terceiro para o container e imprime erro de execução, caso haja_

```*/5 * * * * docker container start <ID CONTAINER> && docker exec -t <ID CONTAINER> date >> /home/Documents/saida.txt && docker container stop <ID CONTAINER> 2> /home/Documents/erros_crontab/log_ERRO-DOCKER_PGP_SRV_PRI.txt``` 

