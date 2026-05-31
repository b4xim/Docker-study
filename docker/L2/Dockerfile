FROM node:18-alpine AS builder
WORKDIR /app

RUN apk add --no-cache git && \
    git clone https://github.com/b4xim/simple_nodejs-app.git . && \
    npm install

FROM node:18-alpine
WORKDIR /app
COPY --from=builder /app .
HEALTHCHECK --interval=30s --timeout=10s --retries=3 CMD wget -qO- http://localhost:3000/ || exit 1
CMD ["npm", "start"]
EXPOSE 3000
