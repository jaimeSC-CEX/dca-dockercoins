FROM node:4-slim
RUN npm install express && npm install redis
COPY . .
CMD ["node", "webui.js"]
EXPOSE 8080
