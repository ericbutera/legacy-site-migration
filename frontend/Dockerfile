# Dockerfile (development mode)
FROM node:18

# Set working directory
WORKDIR /app

# Install deps separately for caching
COPY package*.json ./
RUN npm install

# Copy the rest of the app
COPY . .

# Expose port
EXPOSE 3000

# Run dev server
CMD ["npm", "run", "dev"]
