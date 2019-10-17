FROM ubuntu
RUN apt-get update
RUN apt-get install -y python
RUN echo 1.0 >> /etc/version && apt-get install -y git \
	&& apt-get install -y iputils-ping
RUN mkdir /datos

##WORKDIR##
#Cambia a un directorio y podemos trabajar sobre el
#WORKDIR /datos
#RUN touch f1.txt
#RUN mkdir /datos1
#WORKDIR /datos1
#RUN touch f2.txt

##COPY##
#Copia archivos
#COPY index.html .
#COPY app.log /datos

##ADD##
#Tiene como diferencia del COPY,que permite copiar archivos .tar
#ADD docs docs
#ADD f* /datos/
#ADD f.tar .

##ENV##
#Genera variables
#ENV dir=/data dit1=/data1
#RUN mkdir $dir

##ARG##
#Genera argumentos para pasarlos al momento del build [--build-arg <var>=<value>] tantas veces como variables tengas
#ARG dir2
#RUN mkdir $dir2

##El siguiente codigo deberia generar un usuario y el nombre toma del ARG que le pasamos
#ARG user
#ENV user_docker $user
#ADD add_user.sh /datos1
#RUN /datos1/add_user.sh

##EXPOSE##
#Permite exponer puertos
RUN apt-get install -y apache2
EXPOSE 80
#ADD entrypoint.sh /datos1
#CMD /datos1/entrypoint.sh

##VOLUME##
ADD paginas /var/www/html
VOLUME ["/var/www/html"]

##ENTRYPOINT##
#Es como el CMD pero obliga a que el comando se ejecute, con el CMD podemos pisar la ejecucion si ponemos un CMD luego (se ejecuta el ultimo del archivo)
#ENTRYPOINT ["/bin/bash"]

