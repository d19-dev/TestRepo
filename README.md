# TestRepo
FROM ubuntu:focal-20210217
LABEL mainteiner Avastik 112@770760.ru
RUN apt-get update \ 
   && apt-get install -y nginx \
   && rm -rf /var/lib/apt/lists/* 

EXPOSE 80 443

CMD ["nginx", "-g", "daemon off;"]

