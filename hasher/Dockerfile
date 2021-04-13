FROM ruby:3-alpine AS multilayers
RUN apk add --update build-base curl && gem install sinatra && gem install thin
COPY . .
CMD ["ruby", "hasher.rb"]
EXPOSE 8080

FROM scratch
COPY --from=multilayers / /
