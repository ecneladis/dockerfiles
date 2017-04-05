FROM ruby:2.4-alpine

LABEL maintainer "Michal Marek <ecneladis@gmail.com>"

WORKDIR /app

RUN adduser -u 9000 -D app && \
    chown -R app:app /app
    
USER app

RUN gem install --no-ri --no-rdoc brakeman

ENTRYPOINT ["brakeman"]
