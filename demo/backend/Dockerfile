FROM node:12-alpine
RUN mkdir -p /backend/node_modules && chown -R node:node /backend
WORKDIR /backend
COPY package*.json ./
USER node
RUN npm install --no-progress --ignore-optional
COPY --chown=node:node . .
EXPOSE 3000
CMD ["npm","run", "start:dev"]
