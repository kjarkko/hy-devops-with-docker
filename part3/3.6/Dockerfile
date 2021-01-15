FROM node:10 AS builder
COPY . .
RUN npm install && npm run build

FROM nginx
COPY --from=builder /dist /usr/share/nginx/html
