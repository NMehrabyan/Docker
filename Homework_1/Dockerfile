FROM ubuntu

RUN apt-get update && \
     apt-get install -y nginx \
                      net-tools \
                      iputils-ping \
                      telnet \
                      procps \
                      vim
CMD ["nginx", "-g", "daemon off;"]
EXPOSE 80