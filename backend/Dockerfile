FROM node:18-alpine

WORKDIR /app

COPY package*.json ./
RUN npm install

COPY . .

RUN npx prisma generate

EXPOSE 3000

# Wait for database and then run migrations
CMD ["sh", "-c", "sleep 30 && npx prisma migrate deploy && node src/main.js"]