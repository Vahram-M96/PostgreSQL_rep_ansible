FROM "{{ base_img_name }}"

ENV GOSU_VERSION 1.10

ADD ./gosu /usr/bin/
RUN chmod +x /usr/bin/gosu

RUN apt-get update

RUN apt-get install iputils-ping -y

RUN apt-get install htop

# COPY ./setup-slave.sh /docker-entrypoint-initdb.d
COPY ./docker-entrypoint.sh /docker-entrypoint.sh

RUN chmod +x /docker-entrypoint.sh

ENTRYPOINT ["/docker-entrypoint.sh"]

CMD ["gosu", "postgres", "postgres"]
