# TestRepo
13
FROM ubuntu:focal-20210217
LABEL mainteiner Avasti ovc@770760.ru
RUN apt-get update \ 
   && apt-get install -y nginx=1.18.0-0ubuntu1 \
   && rm -rf /var/lib/apt/lists/* 

EXPOSE 80 443

CMD ["nginx", "-g", "daemon off;"]
