FROM nginx:latest

RUN apt-get update && \
    apt-get install -y libnginx-mod-http-modsecurity && \
    apt-get clean && \
    rm -rf /var/lib/apt/lists/*

COPY modsecurity/modsecurity.conf /etc/nginx/modsecurity/modsecurity.conf
COPY nginx.conf /etc/nginx/nginx.conf

CMD ["nginx", "-g", "daemon off;"]
