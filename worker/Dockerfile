# Use a special node version for worker..
FROM node:14.14.0-alpine

WORKDIR '/app'

# Get our dependencies in a separate cached image
COPY ./package.json .
RUN npm install

# Now grab everything else
COPY . .

# Start everything up in dev monitor mode (nodemon)
CMD ["npm", "run", "start"]
