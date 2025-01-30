FROM node:18

#Set args
ARG DATABASE_URL
ARG JWT_SECRET
ARG BCRYPT_SALT_ROUNDS

#Set env vars
ENV DATABASE_URL=$DATABASE_URL
ENV JWT_SECRET=$JWT_SECRET
ENV BCRYPT_SALT_ROUNDS=$BCRYPT_SALT_ROUNDS

WORKDIR /app

#Copy the currentdirectory into /app
COPY . .

#Install needed package
RUN npm install

EXPOSE 3000

CMD ["npm", "start"]