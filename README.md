# openshift-mvn-s2i  
## Usage:  
### git clone https://github.com/liangx8892/openshift-mvn-s2i  
### cd openshift-mvn-s2i  
### cd mvn-jdk8-docker  
### var/cache/yum/  
### docker build . -t mvn-jdk8:latest  
### cd ../mvn-jdk8-s2i/  
### docker build . -t mvn-jdk8-s2i:latest  
### cd ..  
### cd ..  
### wget https://github.com/openshift/source-to-image/releases/download/v1.2.0/source-to-image-v1.2.0-2a579ecd-linux-amd64.tar.gz  
### tar -xf source-to-image-v1.2.0-2a579ecd-linux-amd64.tar.gz  
### mv s2i /usr/local/bin/  
### mv sti /usr/local/bin/  
### s2i build https://github.com/liangx8892/fsd-registry mvn-jdk8-s2i fsd-registry  
### docker run -d --name fsd-registry -p 8080:8080 fsd-registry  
