FROM node:18-alpine AS builder
WORKDIR /app

RUN apk add --no-cache git && \
    git clone https://github.com/b4xim/simple_nodejs-app.git . && \
    npm ci

FROM node:18-alpine
WORKDIR /app
RUN apk add --no-cache curl
COPY --from=builder /app .
HEALTHCHECK --interval=30s --timeout=10s --retries=3 \
  CMD curl -f http://localhost:3000/ || exit 1
EXPOSE 3000
CMD ["npm", "start"]
