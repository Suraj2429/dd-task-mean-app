# Stage 1: Build Angular App
FROM node:18 AS build

WORKDIR /app

COPY package*.json ./

RUN npm install

COPY . .

# Build Angular 
RUN npm run build


# Stage 2: Serve with Nginx
FROM nginx:alpine

# Remove default nginx static files
RUN rm -rf /usr/share/nginx/html/*

# Copy built Angular app to nginx folder
COPY --from=build /app/dist/angular-15-crud /usr/share/nginx/html

# Expose port 80
EXPOSE 80

CMD ["nginx", "-g", "daemon off;"]