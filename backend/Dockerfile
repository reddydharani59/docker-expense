FROM nodejs:20
EXPOSE 8080
RUN useradd expense
RUN mkdir /opt/server
RUN chown expense:expense -R /opt/server
FROM node:20
EXPOSE 8080
WORKDIR /opt/server
COPY package.json .
COPY *.js .
RUN npm install
CMD [ "node","index.js" ]