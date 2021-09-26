#Instala a versão mais atual do CentOS e dá um nome
FROM centos:lastest AS centOS_crontab_scripts_hospedeiro

LABEL maintainer="Valdemir"

#Atualiza os pacotes prévios
RUN yum check-update && yum -y upgrade

#Instala 
RUN yum -y install openssh-server openssh-clients expect perl 'perl(Net::SSLeay)' 'perl(IO::Socket::SSL)' zip

#especificando o diretório de trabalhos
WORKDIR /home/Documents/

#Mapeia a pasta requerida para o container que vão conter os scripts em comum
#nesse caso, não adicionei os scripts no container, pois há solucções legadas usando os mesmos.
#Se não for seu caso, use o comando ADD e COPY para ter um ambiente isolado e mais seguro
VOLUME /home/datacenter/Documentos/SCRIPTS/






