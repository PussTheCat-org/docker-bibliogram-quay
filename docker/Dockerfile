FROM node:14.4.0-buster
WORKDIR /app
RUN apt update -y && apt upgrade -y \
    && apt install -y git graphicsmagick \
    && git clone --depth=1 https://git.sr.ht/~cadence/bibliogram . \
    && npm install
EXPOSE 10407
CMD ["npm", "start"]
