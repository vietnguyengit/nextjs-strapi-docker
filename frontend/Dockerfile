# build environment
FROM node:latest as build
WORKDIR /app
COPY ./package*.json ./
RUN npm install --production
COPY . .
RUN npm run build
# production environment
#FROM nginx:stable-alpine
#COPY --from=build /app/.next/ /usr/share/nginx/html
#COPY --from=build /app/nginx/nginx.conf /etc/nginx/conf.d/default.conf
ENTRYPOINT npm run start
