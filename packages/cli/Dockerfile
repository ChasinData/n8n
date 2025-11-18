FROM node:20

WORKDIR /app

COPY . .

RUN npm install -g pnpm@8.15.4 lerna@6.6.2 && \
    pnpm install --no-frozen-lockfile && \
    pnpm build

VOLUME /home/node/.n8n

WORKDIR /home/node

ENV N8N_USER_FOLDER=/home/node/.n8n

CMD ["pnpm", "start"]

