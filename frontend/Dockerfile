FROM node:20-alpine AS Builder
WORKDIR /app
COPY package*.json ./
RUN npm install
COPY . .
RUN npm run build 

FROM nginx:1.29.0-alpine
COPY --from=Builder /app/build /usr/share/nginx/html
COPY nginx.conf /etc/nginx/conf.d/default.conf

EXPOSE 80
CMD [ "nginx", "-g", "daemon off;" ]

