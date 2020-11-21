FROM ubuntu:16.04
RUN apt-get update 
RUN apt-get -y install openjdk-8-jre
RUN apt-get -y install openjdk-8-jdk
RUN rm -rf /var/lib/apt/lists/*

ENV JAVA_HOME /usr/lib/jvm/java-15-openjdk-amd64
ENV PATH $JAVA_HOME/bin:$PATH

COPY Hello.java .
RUN javac Hello.java
RUN java Hello
WORKDIR .
CMD java Hello 