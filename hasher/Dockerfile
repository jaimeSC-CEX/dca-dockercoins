FROM ruby:3-alpine AS multilayers
RUN apk add --update build-base curl && gem install sinatra && gem install thin
COPY . .

FROM scratch
COPY --from=multilayers / /

CMD ["hasher.rb"] 
ENTRYPOINT [ "ruby" ]
ENV GEM_HOME /usr/local/bundle
ENV PATH $GEM_HOME/bin:$PATH
EXPOSE 8080
