FROM node:18-alpine

WORKDIR /app

# 1. Copy package files first to leverage Docker layer caching
COPY package*.json ./

# 2. Install all necessary dependencies (including express)
RUN npm install --production

# 3. Copy the rest of your application code (like app.js)
COPY . .

EXPOSE 8080

CMD ["node", "app.js"]
