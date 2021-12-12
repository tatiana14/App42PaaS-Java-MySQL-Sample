FROM tomcat:alpine
WORKDIR  /usr/local/tomcat/
RUN mkdir ROOT
EXPOSE 8080
CMD   cp  /data/*.war webapps/  &&  cp /data/*.properties  ROOT/  && cp /data/*.properties  webapps/ROOT/ && catalina.sh run
