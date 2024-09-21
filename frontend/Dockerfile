FROM node:20-alpine AS build
# Set the working directory inside the container
WORKDIR /app

# Copy package.json and package-lock.json to install dependencies
COPY package*.json .

# Install dependencies
RUN npm install

# Copy the rest of the application code
COPY . .

# Build the production bundle
RUN npm run build

# Expose the port your app will run on
EXPOSE 3000

# Start the application
CMD ["npm", "run", "dev"]