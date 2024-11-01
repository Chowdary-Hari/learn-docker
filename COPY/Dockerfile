FROM almalinux:9
RUN dnf install nginx -y
RUN rm -rf /user/shared/nginx/html/idex.html
COPY ./index.html  /user/shared/nginx/html/idex.html
EXPOSE 80
CMD ["nginx", "-g", "daemon off;"]

# copy :: copy files from your local machine to the docker image