FROM alpine:3.15.0
RUN apk update \
  && apk add --no-cache wget unzip \
  && wget https://releases.hashicorp.com/terraform/0.12.20/terraform_0.12.20_linux_amd64.zip --output-file terraform.zip \
  && unzip ./terraform_0.12.20_linux_amd64.zip -d /usr/local/bin/ \
  && rm -f terraform.zip 
CMD ["terraform", "--version"]