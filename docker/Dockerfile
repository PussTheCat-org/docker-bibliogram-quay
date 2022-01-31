FROM node:14.4.0-buster
WORKDIR /app
RUN apt update && apt upgrade \
    && apt install -y git python3 make g++ graphicsmagick \
    && git clone --depth=1 https://git.sr.ht/~cadence/bibliogram . \
    && npm install
EXPOSE 10407
CMD ["npm", "start"]
