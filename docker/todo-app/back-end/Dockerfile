FROM node:14.19.2-alpine3.15 AS todobackend
WORKDIR /todo-app/back-end
ADD node_modules.tar.gz .
COPY . .
EXPOSE 3001
CMD [ "npm", "start" ]



