FROM node:18

# Create app directory
WORKDIR /app

# Install dependencies
COPY . .

RUN npm install -g pnpm lerna && \
    pnpm install && \
    pnpm build

# Set volume for persistent data
VOLUME /home/node/.n8n

# Set working directory
WORKDIR /home/node

# Set environment path (use your own if needed)
ENV N8N_USER_FOLDER=/home/node/.n8n

# Run n8n
CMD ["pnpm", "start"]
