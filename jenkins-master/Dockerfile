FROM jenkins/jenkins:lts

USER root

# Install the latest Docker CE binaries and add user `jenkins` to the docker group
RUN apt-get update && \
    apt-get install -y --no-install-recommends software-properties-common && \
    curl -fsSL https://download.docker.com/linux/$(. /etc/os-release; echo "$ID")/gpg > /tmp/dkey; apt-key add /tmp/dkey && \
    add-apt-repository \
      "deb [arch=amd64] https://download.docker.com/linux/$(. /etc/os-release; echo "$ID") \
      $(lsb_release -cs) \
      stable" && \
   apt-get update && \
   apt-get -y --no-install-recommends install docker-ce && \
   rm -rf /var/lib/apt/lists/* && \
   usermod -aG docker jenkins

# drop back to the regular jenkins user - good practice
USER jenkins