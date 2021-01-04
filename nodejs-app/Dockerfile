# Define an image dependency present in host machine or in dockerhub
FROM node

# Root folder where the commands must be executed (will be created in container if not exist)
WORKDIR /app

# Copy source files/folders to destination in the container
# optimize by copying package.json to store dependencies in cache before copying folder files
COPY package.json /app

# Run commands on images > Executed when the image is created
RUN npm install

# Copy source files/folders to destination in the container
COPY . /app

# Expose on the host (local machine) the port needed by the container
EXPOSE 8081

# Run when the container is started base on the image
CMD ["node","server.js"]  