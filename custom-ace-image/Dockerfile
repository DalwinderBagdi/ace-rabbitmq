FROM cp.icr.io/cp/appc/ace-server-prod@sha256:eed0750a788047982b3f7ddcf6f6762d46e6c54aca3098dff8ddd25197bcebbc

COPY ace/drivers/mysql-connector-odbc-8.0.26-1.el8.x86_64.rpm /home/aceuser/drivers/mysql-connector-odbc-8.0.26-1.el8.x86_64.rpm

USER root

#install the mysqlconnector
RUN microdnf install yum
RUN yum -y localinstall  /home/aceuser/drivers/mysql-connector-odbc-8.0.26-1.el8.x86_64.rpm

RUN mkdir /home/aceuser/rabbitmqjars
COPY /ace/rabbitmqjars/ /home/aceuser/rabbitmqjars

USER aceuser