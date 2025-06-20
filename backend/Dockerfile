FROM node:20

# Set working directory
WORKDIR /app

# Copy package.json dan install dependencies
COPY package*.json ./
RUN npm install

# Copy seluruh source code
COPY . .

# Jalankan aplikasi
EXPOSE 3000
CMD ["npm", "install"]
CMD ["npx", "prisma", "generate"]
CMD ["node", "src/main.js"]
