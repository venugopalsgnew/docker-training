FROM ubuntu
RUN apt-get update && apt-get install -y \
    wget \
    unzip \
    default-jdk
WORKDIR /opt
RUN mkdir maven
ADD https://dlcdn.apache.org/maven/maven-3/3.9.9/binaries/apache-maven-3.9.9-bin.zip /opt/maven
RUN unzip /opt/maven/apache-maven-3.9.9-bin.zip -d /opt/maven
RUN rm /opt/maven/apache-maven-3.9.9-bin.zip
ENV MAVEN_HOME=/opt/maven/apache-maven-3.9.9
ENV PATH=${MAVEN_HOME}/bin:${PATH}
# Verify Maven installation
RUN mvn -version
# Set the default command to bash
CMD ["bash"]
