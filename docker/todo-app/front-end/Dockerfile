FROM node:14.19.2-alpine3.15 AS todofrontend
WORKDIR /todo-app/front-end
ADD node_modules.tar.gz .
COPY . .
EXPOSE 3000
CMD [ "npm", "start" ]
