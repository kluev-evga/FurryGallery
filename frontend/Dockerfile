FROM node:18-alpine
WORKDIR /app
COPY package*.json .
RUN npm ci
COPY . .
RUN npm run build
CMD ["npx", "-y", "http-server", "-p", "8000", "/app/build"]