FROM node:latest
WORKDIR .
COPY . .
RUN npm i
RUN npm i -g serve
RUN npm run build
CMD ["serve", "-s", "build"]
