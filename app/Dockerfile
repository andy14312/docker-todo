# syntax=docker/dockerfile:1
FROM node:19-alpine3.15
RUN apk add --no-cache python2 g++ make
WORKDIR /app
COPY package.json yarn.lock ./
RUN yarn install --production
COPY . .
CMD ["node", "src/index.js"]
EXPOSE 3000