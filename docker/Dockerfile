FROM node:14-bullseye
WORKDIR /app
RUN apt update -y && apt upgrade -y \
    && apt install -y --no-install-recommends git python3 make g++ graphicsmagick \
    && apt autoclean -y \
    && apt autoremove -y \
    && rm -rf /var/lib/apt/lists/* \
    && git clone --depth=1 https://git.sr.ht/~cadence/bibliogram . \
    && npm install
EXPOSE 10407
CMD ["npm", "start"]
