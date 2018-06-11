# eks-tools-alpine
Alpine image with Kubectl, Helm, Heptio, and AWS CLI pre-installed.

This is in the early stages adn should change a lot. 

## Getting started

Pretty easy, pull the image and you have an almost complete working environment for accessing EKS. Just load your credentials, which with using Heptio are fairly generic, and you can rock and roll.

```
docker pull phillipsj/eks-tools-base:0.1-beta
docker run eks-tools-base
```
