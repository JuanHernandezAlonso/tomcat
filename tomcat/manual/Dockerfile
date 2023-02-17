FROM openjdk:11.0.16-jdk-slim-buster
ENV CATALINA_BASE=/usr/local/tomcat
ENV CATALINA_HOME=/usr/local/tomcat
RUN mkdir -p $CATALINA_HOME
COPY apache-tomcat-10.0.27.tar.gz $CATALINA_HOME/
RUN tar xvzf $CATALINA_HOME/apache-tomcat-10.0.27.tar.gz --strip-components=1 -C $CATALINA_HOME && chmod 755 $CATALINA_HOME/bin/catalina.sh
COPY host-manager/context.xml $CATALINA_HOME/webapps/host-manager/META-INF/context.xml
COPY manager/context.xml $CATALINA_HOME/webapps/manager/META-INF/context.xml
COPY tomcat-users.xml $CATALINA_HOME/conf/tomcat-users.xml
RUN useradd -p admin admin
RUN useradd -p robot robot
RUN chmod 755 $CATALINA_HOME/bin/catalina.sh
COPY sample.war $CATALINA_HOME/webapps
EXPOSE 8080/tcp
CMD ["/usr/local/tomcat/bin/catalina.sh","run"]