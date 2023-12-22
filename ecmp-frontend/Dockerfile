FROM node:20.10.0-alpine as node
WORKDIR /app
COPY package.json ./
COPY . .
RUN npm install
RUN npm run build

FROM nginx:latest
COPY nginx.conf /etc/nginx/conf.d/default.conf
COPY --from=node /app/dist/ecmp-frontend /usr/share/nginx/hml
