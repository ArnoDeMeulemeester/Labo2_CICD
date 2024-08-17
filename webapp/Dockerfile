#Start from a Docker image for Node.js version 18.x.x (LTS)
FROM node:18

#The application should be reachable on port 3000
EXPOSE 3000

#Copy the application code in the /app folder in the container
WORKDIR /app
COPY . /app
COPY package.json yarn.lock /app/

#Install the application dependencies with the yarn install --frozen-lockfile command
RUN yarn install --frozen-lockfile

#The application should be started using the yarn start command (when the container is started)
CMD ["yarn", "start"]
