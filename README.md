# jenkins-docker
Contains Dockerfiles and description for running Jenkins master and Jenkins
agents as docker images in WSL2.

## jenkins-master
The default jenkins/jenkins:lts image does not contain docker cli, needed for
calling docker from Jenkins master. The jenkins-master directory contains a
Dockerfile which adds it.

## jenkins-agent-master
Add a base jenkins-agent image based on ubuntu 20.04 and with jre and opsnssh.
