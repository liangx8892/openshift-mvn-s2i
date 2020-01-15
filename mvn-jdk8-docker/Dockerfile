FROM openshift/base-centos7:latest

ENV MAVEN_VERSION 3.6.3
ENV MAVEN_HOME /usr/lib/mvn
ENV PATH $MAVEN_HOME/bin:$PATH

RUN yum install -y \
       java-1.8.0-openjdk \
       java-1.8.0-openjdk-devel

RUN wget http://mirror.bit.edu.cn/apache/maven/maven-3/$MAVEN_VERSION/binaries/apache-maven-$MAVEN_VERSION-bin.tar.gz && \
    tar -zxvf apache-maven-$MAVEN_VERSION-bin.tar.gz && \
    rm apache-maven-$MAVEN_VERSION-bin.tar.gz && \
    mv apache-maven-$MAVEN_VERSION /usr/lib/mvn 

ENV JAVA_HOME /usr/lib/jvm/java-1.8.0-openjdk-1.8.0.232.b09-0.el7_7.x86_64

# Only apply when use China network
#RUN rm -f /usr/lib/mvn/conf/settings.xml \
#    mkdir /usr/lib/mvn/repo
# Only apply when use China network
# COPY settings.xml /usr/lib/mvn/conf/
# Only apply when use China network
# ADD repo.tar /usr/lib/mvn/ 
