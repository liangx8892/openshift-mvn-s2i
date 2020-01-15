# mvn-jdk8-s2i
FROM mvn-jdk8:latest

# TODO: Put the maintainer name in the image metadata
LABEL maintainer="Liang Xiong <liangx8892@gmail.com>"

# TODO: Rename the builder environment variable to inform users about application you provide them
# ENV BUILDER_VERSION 1.0
ENV TZ Asia/Shanghai

# TODO: Set labels used in OpenShift to describe the builder image
LABEL io.k8s.description="Platform for serving SpringBoot applications" \
      io.k8s.display-name="jdk8 s2i image" \
      io.openshift.expose-services="8080:http" \
      io.openshift.tags="builder,java,springboot."

LABEL io.openshift.s2i.scripts-url="image:///usr/libexec/s2i"

# TODO: Copy the S2I scripts to /usr/libexec/s2i, since openshift/base-centos7 image
# sets io.openshift.s2i.scripts-url label that way, or update that label
COPY ./s2i/bin/ /usr/libexec/s2i/

# TODO: Drop the root user and make the content of /opt/app-root owned by user 1001
RUN chown -R 1001:1001 /opt/

# This default user is created in the openshift/base-centos7 image
USER 1001

# TODO: Set the default port for applications built using this image
EXPOSE 8080

# TODO: Set the default CMD for the image
CMD ["/usr/libexec/s2i/usage"]
