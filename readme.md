# How to create a Docker image which provides Nginx server by using Packer.

# Purpose

This repository's sole purpose is to demonstrate how to built a Docker image using Packer which provides Nginx webserver.

# Technologies in use :

- Packer
- Vagrant
- VirtualBox
- Nginx
- Docker

# How to install the pre-requisites:

- [How to install Vagrant](https://www.vagrantup.com/docs/installation/)
- [How to install VirtualBox](https://www.virtualbox.org/manual/ch02.html)

# How to use

- Clone this git repository using `git clone https://github.com/martinhristov90/packerDockerNginx `
- Switch into the directory of the project using : `cd packerDockerNginx`
- Now you should have a copy of the project, run `vagrant up` to build the VM in which Packer and Docker are going to run.
- When the VM is running, ssh to it with `vagrant ssh`
- Change into the building directory with `cd ~/buildDir`
- Run `packer build template.json`, which is going to output Docker image with Nginx installed, also it is going to be imported to Docker automatically. To verify that the image is imported run `docker images`, the output should look like this : 

```

REPOSITORY          TAG                 IMAGE ID            CREATED             SIZE
martin              0.1                 b87d812ae4d5        14 hours ago        200MB
ubuntu              xenial              a3551444fc85        2 weeks ago         119MB

```


