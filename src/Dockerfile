FROM python:3.6-alpine

# Install AWS CLI
RUN pip install awscli --upgrade

# Install CURL
RUN apk add --no-cache bash curl openssl ca-certificates

# Install Kubectl
RUN set -ex \
        && curl -LO https://storage.googleapis.com/kubernetes-release/release/$(curl -s https://storage.googleapis.com/kubernetes-release/release/stable.txt)/bin/linux/amd64/kubectl \
        && chmod +x ./kubectl \
        && mv ./kubectl /usr/local/bin/kubectl \
        \
        # Install Heptio 
        && curl -o heptio-authenticator-aws https://amazon-eks.s3-us-west-2.amazonaws.com/1.10.3/2018-06-05/bin/darwin/amd64/heptio-authenticator-aws \
        && chmod +x ./heptio-authenticator-aws \
        && mv ./heptio-authenticator-aws /usr/local/bin/heptio-authenticator-aws \
        \
        # Install Helm
        && curl https://raw.githubusercontent.com/kubernetes/helm/master/scripts/get > get_helm.sh \
        && chmod +x ./get_helm.sh \
        && ./get_helm.sh
