FROM almalinux:9

RUN dnf install nginx -y

RUN rm -rf /usr/share/nginx/html/index.html

ADD https://raw.githubusercontent.com/manojmantha/Dockerfile-Instrutions/refs/heads/main/1-FROM/Dockerfile /usr/share/nginx/html/index.html

CMD ["nginx", "-g", "daemon off;"]