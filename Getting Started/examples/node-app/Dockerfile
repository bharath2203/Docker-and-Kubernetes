# Use pre built docker image
FROM node

# Sets working directory as /app
WORKDIR /app

# COPY and RUN words relative to the working directory(which is root at start)
COPY . /app

RUN npm install

# Expose the app to port 80
EXPOSE 80

# CMD is when you want to run the container
CMD ["node", "server.js"]
