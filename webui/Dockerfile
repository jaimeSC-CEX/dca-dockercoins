FROM node:4-slim AS multilayer
RUN npm install express && npm install redis
COPY . .
CMD ["node", "webui.js"]
EXPOSE 8080

FROM scratch
COPY --from=multilayer / /
