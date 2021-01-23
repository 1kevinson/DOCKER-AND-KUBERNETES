FROM node

# Create app directory
WORKDIR /app

# Install dependencies
COPY package.json /app

RUN npm install

# Create a anonymous volume to exclude modules to be overwrite by bind mount 
VOLUME ["/app/node_modules"]

# Bundle app sources
COPY . /app

EXPOSE 80

# environment variables for db credentials
ENV MONGODB_USERNAME=root
ENV MONGODB_PASSWORD=secret

# Launch the app
CMD ["npm","start"]  