FROM node:18

#Set args
ARG VITE_API_URL

#Set env vars
ENV DATABASE_URL=$VITE_API_URL

WORKDIR /app

#Copy the currentdirectory into /app
COPY . .

#Install needed package
RUN npm install

EXPOSE 5173

CMD ["npm", "run", "dev", "--", "--host", "0.0.0.0"]