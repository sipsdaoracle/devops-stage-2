# Stage 1: Build React application
FROM node:16-alpine AS build
# Set working directory
WORKDIR /app
# Copy package.json and package-lock.json
COPY package*.json ./
# Install dependencies
RUN npm install
# Copy the rest of the application
COPY . .
EXPOSE 5173
# Run the development server on container start
CMD ["npm", "run", "dev", "--", "--host"]

# # Stage 2: Serve React application with nginx
# FROM nginx:alpine 
# COPY --from=build /app/dist /usr/share/nginx/html  
# COPY nginx.conf /etc/nginx/conf.d/default.conf

# EXPOSE 80
# CMD ["nginx", "-g", "daemon off;"]
