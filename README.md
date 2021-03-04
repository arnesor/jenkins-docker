# jenkins-docker
Contains Dockerfiles and description for running Jenkins master and Jenkins
agents as docker images in WSL2.

## jenkins-master
The default jenkins/jenkins:lts image does not contain docker cli, needed for
calling docker from Jenkins master. The jenkins-master directory contains a
Dockerfile which adds it.
