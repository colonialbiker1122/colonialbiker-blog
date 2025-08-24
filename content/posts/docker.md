+++
date = '2025-08-09T09:03:43+05:30'
draft = false
title = 'Introduction to Docker'
categories = ['DevOps']
+++
## Container characteristics
- Container engine virtualises OS
- Container is light-weight, fast, isolated, portable and secure
- Binaries, libraries within container enable apps to run
- Platform independent: cloud/ on-premises etc
- OS independent: Windows/ Linux
- Language independent

## Container vendors
- Docker: Robust
- Podman: More-secure
- LXC: data-intensive
- Vagrant: High isolation-level

## Docker
- Build: create container image from dockerfile
- Images:
- Run: Creates container from an image
- Push: Store images in configured registry
- Pull: Retrieve

- Dockerfile: FROM base_img RUN command
- Docker image: Read-only template with instructions to create a container hostname/ repository
  - hotsname/repository:tag
  - docker.io/ubuntu:18.04

- Commands: 
  - docker images (list images)
  - docker pull hello-world
  - docker run hello-world
  - docker ps -a (list containers)
  - docker build . -t myimage:v1 (build image and tag image ID)
  - docker run -dp 8080:8080 myimage:vl

