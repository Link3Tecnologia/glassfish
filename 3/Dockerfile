# link3tecnologia/glassfish:3
FROM link3tecnologia/oraclejava:7
ENV GLASSFISH_VERSION=3.1.2.2
ENV GLASSFISH_FILE=glassfish-$GLASSFISH_VERSION.zip
RUN yum -y install unzip
WORKDIR /opt
RUN wget http://download.oracle.com/glassfish/$GLASSFISH_VERSION/release/$GLASSFISH_FILE
RUN unzip -o $GLASSFISH_FILE
RUN mv glassfish3/ glassfish-$GLASSFISH_VERSION/
EXPOSE 4848 8080 8181
RUN ln -s /opt/glassfish-$GLASSFISH_VERSION /opt/glassfish
CMD ["/opt/glassfish/bin/asadmin", "start-domain", "-v"]
