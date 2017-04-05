FROM ruby:2.4-alpine

WORKDIR /app

RUN adduser -u 9000 -D app && \
    chown -R app:app /app
    USER app
    
RUN gem install --no-ri --no-rdoc bundler-audit

RUN bundle-audit update

ENTRYPOINT ["bundle-audit"]
