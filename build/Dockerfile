FROM ubuntu:20.04
ENV TZ=Europe/Dublin
RUN ln -snf /usr/share/zoneinfo/$TZ /etc/localtime && echo $TZ > /etc/timezone
RUN apt-get -qq update && \
    apt-get install -y apache2 && \
    apt-get clean
COPY public-html/index.html /var/www/html/
EXPOSE 80
CMD apachectl -D FOREGROUND
