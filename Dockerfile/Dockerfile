FROM jenkins/jenkins:lts

USER root

# Change Debian repository mirror to a more stable one
RUN echo "deb http://ftp.debian.org/debian bookworm main" > /etc/apt/sources.list

# Update package lists and install dependencies
RUN apt-get update && \
    apt-get upgrade -y && \
    apt-get install -y make g++ --fix-missing && \
    apt-get clean && \
    rm -rf /var/lib/apt/lists/*

# Switch back to Jenkins user
USER jenkins
