FROM node:10-alpine
RUN mkdir -p /frontend/node_modules && chown -R node:node /frontend
WORKDIR /frontend
COPY package*.json ./
USER node
RUN npm install --no-progress --ignore-optional
COPY --chown=node:node . .
CMD ["npm", "start"]
