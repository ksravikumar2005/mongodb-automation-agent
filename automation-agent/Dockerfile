FROM ubuntu:16.04
ENV AGENT_PACKAGE mongodb-mms-automation-agent-manager_latest_amd64.ubuntu1604.deb
ENV AGENT_SOURCE https://cloud.mongodb.com/download/agent/automation
#https://cloud.mongodb.com/download/agent/automation/mongodb-mms-automation-agent-manager_latest_amd64.ubuntu1604.deb
RUN apt-get -qqy update && \
    apt-get install -qqy \
    ca-certificates \
    libsasl2-2 \
    wget \
    curl \
    libcurl3
RUN wget  ${AGENT_SOURCE}/${AGENT_PACKAGE}
RUN dpkg -i ${AGENT_PACKAGE}
RUN mkdir /data
RUN chown mongodb:mongodb /data

VOLUME /etc/mongodb-mms/
VOLUME /data

EXPOSE 27000
EXPOSE 27017
ENTRYPOINT ["/opt/mongodb-mms-automation/bin/mongodb-mms-automation-agent"]
