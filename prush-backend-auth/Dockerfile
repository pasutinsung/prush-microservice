# Use the official Node.js 14 image as a base
FROM node:18.17.0

# Set the working directory inside the container
WORKDIR /app

# Copy package.json and package-lock.json to the working directory
COPY package*.json ./

# Install dependencies
RUN npm install

# Install daisyui
RUN npm install daisyui

# Copy the rest of the application code
COPY . .

RUN rm -rf node_modules

# Build the Next.js app for production
RUN npm run build

# Expose the port Next.js is running on
EXPOSE 8000

# Command to run the Next.js app
CMD ["npm", "start"]
