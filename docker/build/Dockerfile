FROM alpine
RUN apk add maven
ARG USER
ARG PWD
ARG PORT
ARG IP
ARG DB_NAME
WORKDIR  /opt/maven
ARG env_file=WebContent/Config.properties
COPY  . /opt/maven
RUN echo app42.paas.db.username = ${USER} > ${env_file} \
&& echo app42.paas.db.port = ${PWD} >> ${env_file} \
&& echo app42.paas.db.password = ${PORT} >> ${env_file} \
&& echo app42.paas.db.ip = ${IP} >> ${env_file} \
&& echo app42.paas.db.name = ${DB_NAME} >> ${env_file}
RUN mvn package
RUN mkdir data && cp target/*.war data/ && cp WebContent/Config.properties data/Config.properties
CMD tail -f /dev/null
