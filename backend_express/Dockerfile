FROM node:17
# Create app directory
WORKDIR /usr/src/app
# Copy all files
COPY . .
# install dependencies
RUN npm install
# Open port
EXPOSE 3000
# Run app in debug mode
CMD [ "npm", "start" ]