FROM node:lts-alpine as build
WORKDIR /app
RUN apk upgrade --no-cache \
    && apk --no-cache add git python3-dev make g++ \
    && git clone --depth=1 https://git.sr.ht/~cadence/bibliogram . \
    && npm install --no-optional

FROM node:lts-alpine as app
WORKDIR /app
COPY --from=build /app /app
RUN apk add --no-cache graphicsmagick git
EXPOSE 10407
CMD ["npm", "start"]
