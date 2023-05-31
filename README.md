# Highload Software Architecture 8 Lesson 25 Homework

AWS: EC2 and Load Balancer
---

## Project setup

The project consists of two almost identical nginx-based Docker images that serve static content: [`service-one`](service-one) and [`service-two`](service-two).

These docker images are built with GitHub Actions [workflow](.github/workflows/docker.yaml) and pushed to the same Docker Hub repository, but with different tags, for simplicity: [ssamoilenko/hsa-25-ec2](https://hub.docker.com/repository/docker/ssamoilenko/hsa-25-ec2).

These docker images are then used on two t2.micro EC2 instances: [service-one](http://ec2-3-124-209-226.eu-central-1.compute.amazonaws.com/) and [service-two](http://ec2-18-159-35-23.eu-central-1.compute.amazonaws.com/).

These services are then load-balanced with AWS Application [Load Balancer](http://hsa25-86038341.eu-central-1.elb.amazonaws.com).

## Presentation

No Terraform/CloudFormation this time, but I prepared a short demo record with Loom: https://www.loom.com/share/a404d0ae6bab432898344288032d9f2c
