FROM node:4-slim AS multilayer
COPY . .
RUN npm install express && npm install redis


FROM scratch
COPY --from=multilayer / /

CMD ["webui.js"]
ENTRYPOINT ["node"]
EXPOSE 8080
