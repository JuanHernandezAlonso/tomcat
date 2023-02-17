FROM tomcat:latest
RUN useradd -p admin admin
RUN useradd -p robot robot
RUN useradd -p tomcat tomcat
RUN useradd -p both both
ENV CATALINA_BASE=/usr/local/tomcat
ENV CATALINA_HOME=/usr/local/tomcat
RUN mkdir -p /usr/local/tomcat
RUN mv webapps webapps2
RUN mv webapps.dist/ webapps
RUN chmod 755 $CATALINA_HOME/bin/catalina.sh
COPY host-manager/context.xml $CATALINA_HOME/webapps/host-manager/META-INF/context.xml
COPY manager/context.xml $CATALINA_HOME/webapps/manager/META-INF/context.xml
COPY tomcat-users.xml $CATALINA_HOME/conf/tomcat-users.xml
#Se levanta en el siguiente puerto
EXPOSE 8080/tcp
#Ejecutamos el script catalina.sh
CMD ["/usr/local/tomcat/bin/catalina.sh","run"]