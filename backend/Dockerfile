FROM node:20
EXPOSE 8080
RUN adduser expense
RUN mkdir /opt/service
RUN chown expense:expense -R /opt/service
WORKDIR /opt/service
COPY package.json .
COPY *.js .
RUN npm install
USER expense
CMD [ "node","index.js" ]

