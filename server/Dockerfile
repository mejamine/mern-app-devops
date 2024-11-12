#node js version
FROM node:20

# working directory
WORKDIR /app

# handeling dependecy source (package.json)
COPY package.json ./

# install dependencies 
RUN npm install

# copy the rest of the code
COPY . ./

# port
EXPOSE 9000

#run 
CMD ["npm","start"]
