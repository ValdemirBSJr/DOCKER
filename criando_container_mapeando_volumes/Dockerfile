#Instala a versão 7 do CentOS
FROM centos:7

LABEL maintainer="Valdemir"

#Atualiza os pacotes prévios
RUN yum check-update && yum -y upgrade

#especificando o diretório de trabalhos
WORKDIR /home/Documents/

#Mapeia a pasta requerida para o container 
VOLUME /home/datacenter/Documentos/SCRIPTS/


