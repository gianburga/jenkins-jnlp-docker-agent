# Jenkins JNLP Docker Agent

Jenkins JNLP Agent with DnD

### Base Docker Image
[jenkins/jnlp-agent](https://hub.docker.com/r/jenkins/jnlp-agent)


### Image

[francoburga/jenkins-jnlp-docker-agent](https://hub.docker.com/r/francoburga/jenkins-jnlp-docker-agent)

### Pull Image

`docker pull francoburga/jenkins-jnlp-docker-agent:latest`

### Run Command
```
docker run \
    -v /var/run/docker.sock:/var/run/docker.sock \
    -v /var/jenkins-agent/:/home/jenkins/agent \
    francoburga/jenkins-jnlp-docker-agent:latest \
        -url http://jenkins-host \
        -workDir=/home/jenkins/agent <secret> <agent-name>
```

### Run Command With Root User
```
docker run \
    -u root \
    -v /var/run/docker.sock:/var/run/docker.sock \
    -v /var/jenkins-agent/:/home/jenkins/agent \
    francoburga/jenkins-jnlp-docker-agent:latest \
        -url http://jenkins-host \
        -workDir=/home/jenkins/agent <secret> <agent-name>
```