FROM anarh/centos6.6
COPY jre-8u45-linux-x64.rpm /tmp/
RUN rpm -ivh /tmp/jre-8u45-linux-x64.rpm
RUN useradd -d "/home/tom" -m -s "/bin/bash" tom
COPY apache-tomcat-6.0.44/ /home/tom/
EXPOSE 8080
ENV CATALINA_HOME /home/tom
ENV JAVA_HOME /usr
RUN chown -R tom:tom /home/tom && chmod -R 755 /home/tom
USER tom
CMD /home/tom/bin/catalina.sh run

