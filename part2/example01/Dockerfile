FROM httpd:alpine
MAINTAINER @mimaraslan (mimar.aslan@gmail.com)

RUN apk add htop gzip iputils curl apache2 tree openjdk17-jre
RUN apk update && apk upgrade

WORKDIR /usr/src/myapp
COPY /myapp .
RUN echo "<html><body><h1>Docker hello.</h1></body></html>" > /usr/local/apache2/htdocs/index.html