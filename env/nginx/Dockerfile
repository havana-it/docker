FROM nginx:latest

LABEL author="Yann Blacher for Havana IT & APPS" \
      description="Nginx image with logs and vim installed" \
      license="MIT"

RUN apt-get update && apt-get install -y vim \
   && apt-get autoremove && apt-get autoclean \
   && rm -rf /var/lib/apt/lists/*

RUN sed -i 's#^error_log.*$#error_log /proc/self/fd/2 warn;#' /etc/nginx/nginx.conf
