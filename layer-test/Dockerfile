#FROM node:20
#IC 1
FROM node:20.18.3-alpine3.21
#on top od ic 1 instruction 2 is executed , and save this layer 2 image. ic 1 is removed
#create ic 2, on top of ic 2 instruction-3 id executed and save this as layer image. ic 2 is removed
RUN addgroup -S expense && adduser -S expense -G expense && \
    mkdir /opt/backend && \
    chown -R expense:expense /opt/backend
WORKDIR /opt/backend
COPY package.json .
COPY *.js ./
RUN npm install
#ENV DB_HOST="mysql"
#ENV DB_HOST="localhost"
USER expense
CMD ["node", "index.js"]
