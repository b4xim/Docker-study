FROM node:18-alpine
WORKDIR /app

RUN apk add --no-cache git && \
    git clone https://github.com/b4xim/simple_nodejs-app.git . && \
    apk del git && \
    npm install
EXPOSE 3000
CMD ["npm","start"]