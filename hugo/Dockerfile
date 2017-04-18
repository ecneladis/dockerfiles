FROM alpine:latest

ENV HUGO_VERSION 0.20.2

RUN apk --no-cache add \
    ca-certificates \
    wget

WORKDIR "/tmp"
RUN wget "https://github.com/spf13/hugo/releases/download/v${HUGO_VERSION}/hugo_${HUGO_VERSION}_Linux-64bit.tar.gz" \
  && tar -xz --strip-components 1 -f hugo_${HUGO_VERSION}_Linux-64bit.tar.gz \
  && mv /tmp/hugo_${HUGO_VERSION}_linux_amd64 /usr/local/bin/hugo

VOLUME "/var/www/blog"
WORKDIR "/var/www/blog"

ENTRYPOINT ["hugo"]
