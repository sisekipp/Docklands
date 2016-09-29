FROM sisekipp/centos_java
MAINTAINER Sebastian Kipping, kipping.sebastian@gmail.com
ENV ARCHIVE apache-tomcat-8.0.37
ENV INSTALL_DIR /opt
ENV SERVER_HOME ${INSTALL_DIR}/${ARCHIVE}
RUN curl -o ${SERVER_HOME}.zip -L http://apache.mirror.iphh.net/tomcat/tomcat-8/v8.0.37/bin/apache-tomcat-8.0.37.zip
RUN unzip ${SERVER_HOME}.zip -d /opt
RUN chmod a+x ${SERVER_HOME}/bin/catalina.sh
ENV DEPLOYMENT_DIR ${SERVER_HOME}/webapps/
ENTRYPOINT ${SERVER_HOME}/bin/catalina.sh run
EXPOSE 8080
