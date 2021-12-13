FROM alpine
RUN apk add maven
WORKDIR  /opt/maven
COPY  . /opt/maven
RUN mvn package
RUN mkdir data && cp target/*.war data/ && cp Config.properties data/Config.properties
