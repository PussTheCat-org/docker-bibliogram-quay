FROM node:lts-alpine
WORKDIR /app
RUN apk upgrade --no-cache \
    && apk --no-cache add git python3-dev make g++ graphicsmagick \
    && git clone --depth=1 https://git.sr.ht/~cadence/bibliogram . \
    && npm install
EXPOSE 10407
CMD ["npm", "start"]
