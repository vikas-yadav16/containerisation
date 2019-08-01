FROM ubuntu

RUN apt-get update \
    && apt-get install -y nginx && apt-get clean \
    && rm -rf /var/lib/apt/lists/*  && echo "daemon off;" >> /etc/nginx/nginx.conf
     
   
ADD default /etc/nginx/sites-available
	
EXPOSE 80
CMD echo $HOSTNAME > /usr/share/nginx/html/index.html && nginx



