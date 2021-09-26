# Iremos criar um container que irá rodar internamente o crontab para executar uma determinada tarefa

### Note que neste caso, o container terá o fuso horário setado para ficar semelhante a minha máquina local e ficará rodando pra executar a tarefa, mas não dependerá do crontab do host hospedeiro, rodará completamente isolado do host.

####Iremos seguir os seguintes passos:

- Cria o container

- Atualiza os pacotes

- Instala o crontab na máquina

- Seta o fuso horário localtime

- Cria um arquivo com as tarefas

- Aponta o arquivo para ser reconhecido pelo daemon do crontab

- Executa o programa do crontab no início do container


_Importante:_ 

> Caso queira forçar a inicialização do crontab no container já criado, basta acrescentar ```/usr/sbin/crond``` no arquivo ```/root/.bashrc``` 
