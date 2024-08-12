FROM node:20
EXPOSE 8080
ENV DB_HOST \
    DB_USER \
    DB_PWD \
    DB_DATABASE 
RUN useradd expense
RUN mkdir /opt/server
RUN chown expense:expense -R /opt/server
WORKDIR /opt/server
COPY package.json .
COPY *.js .
RUN npm install
USER expense
CMD [ "node", "index.js" ]
