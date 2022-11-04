# build environment
FROM node:latest
WORKDIR /app
RUN npm install --global pm2
COPY ./package*.json ./
RUN npm install --production
COPY . .
RUN npm run build
CMD ["pm2-runtime", "npm", "--", "start"]
