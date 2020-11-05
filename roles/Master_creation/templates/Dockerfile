FROM "{{ base_img_name }}"

RUN apt update

RUN apt install htop

COPY ./setup-master.sh /docker-entrypoint-initdb.d/setup-master.sh

RUN chmod 0666 /docker-entrypoint-initdb.d/setup-master.sh
