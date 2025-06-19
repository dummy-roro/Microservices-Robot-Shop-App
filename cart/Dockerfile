FROM node:14
# Use Node.js version 14 as base image

ENV INSTANA_AUTO_PROFILE true
# Set environment variable to enable Instana profiling

EXPOSE 8080
# Expose port 8080 for the container

WORKDIR /opt/server
# Set working directory inside the container

COPY package.json /opt/server/
# Copy package.json to the working directory

RUN npm install
# Install dependencies listed in package.json

COPY server.js /opt/server/
# Copy server.js application file to working directory

# Run the server.js file using node when container starts
CMD ["node", "server.js"]
