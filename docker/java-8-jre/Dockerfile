#
# OpenJDK Java 8 JRE Dockerfile
#
# https://github.com/michaelmarquis/raspberry-zero/java-8-jre
#

# Pull base image.
FROM resin/rpi-raspbian:latest

# Install Java.
RUN \
  apt-get update && \
  apt-get install -y openjdk-8-jre-headless && \
  rm -rf /var/lib/apt/lists/* && \
  java -version

# Define working directory.
WORKDIR /data

# Define commonly used JAVA_HOME variable
ENV JAVA_HOME /usr/lib/jvm/java-8-openjdk-armhf/

# Define the JAVA_OPTIONS variable
CMD java -XX:+PrintFlagsFinal -XX:+PrintGCDetails $JAVA_OPTIONS -jar java-container.jar

# Define default command.
CMD ["bash"]
