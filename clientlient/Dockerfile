FROM node:18-alpine

# Install build dependencies
RUN apk add --no-cache \
      python3 \
      make \
      g++ \
      cairo-dev \
      pango-dev \
      giflib-dev

# Create a symlink for python3 as python
RUN ln -sf /usr/bin/python3 /usr/bin/python

# Set environment variable for Python
ENV PYTHON=/usr/bin/python3

# Set the working directory
WORKDIR /usr/src/app

# Copy package.json and package-lock.json
COPY package*.json ./

# Install dependencies
RUN npm install --only=production

# Copy the rest of the application code
COPY . .

# Expose the port the app runs on
EXPOSE 3000

# Start the application
CMD ["node", "app.js"]

