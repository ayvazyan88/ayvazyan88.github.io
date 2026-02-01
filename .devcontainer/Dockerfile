FROM ruby:3.2
ENV LANG=C.UTF-8 \
    LC_ALL=C.UTF-8 \
    JEKYLL_ENV=development
RUN apt-get update -y && \
    apt-get install -y \
      nodejs \
      npm \
      git \
      locales \
    && rm -rf /var/lib/apt/lists/*
RUN gem install bundler jekyll
WORKDIR /workspace
