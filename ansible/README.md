Jenkins swarm slave with Ansible development environment
========================================================

Start a [Jenkins swarm](https://wiki.jenkins-ci.org/display/JENKINS/Swarm+Plugin) slave with Ansible installed in Docker.

### Start a slave

```
docker run \
  --detach \
  heliostech/jenkins-slave-ansible \
  -master http://jenkins-server/ \
  -username JENKINS_USER \
  -password JENKINS_USER_KEY \
  -executors 2 \
  -labels "linux ansible"
```


### Available Options

Display the available options with the following command:

```
docker run -it --rm heliostech/jenkins-slave-ansible -help
```

## Credits

   This container is part of [DevStack](https://www.devstack.com/), a project to facilitate DevOps work with continuous integration and deployment environment ready to use.
