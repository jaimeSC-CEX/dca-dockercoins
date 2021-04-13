FROM ruby:3-alpine
RUN apk add --update build-base curl && gem install sinatra && gem install thin
COPY hasher.rb /
CMD ["ruby", "hasher.rb"]
EXPOSE 8080
