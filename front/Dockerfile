FROM node:18 as build

#Set args
ARG VITE_API_URL

#Set env vars
ENV DATABASE_URL=$VITE_API_URL

WORKDIR /app

#Copy the currentdirectory into /app
COPY . .

#Install needed package
RUN npm install
RUN npm run build

FROM nginx:alpine

COPY --from=build /app/dist /usr/share/nginx/html

EXPOSE 80

CMD ["nginx", "-g", "daemon off;"]