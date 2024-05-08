# Use Node.js LTS image as base
FROM node:14

# Set the maximum heap size
# ENV NODE_OPTIONS="--max_old_space_size=2048" 

# Frontend env
ENV REACT_APP_AUTH0_DOMAIN="dev-gz0neue2qdskafes.us.auth0.com"
ENV REACT_APP_AUTH0_CLIENT_ID="L5xBB9uNUwkRIuJNpNUUrfCCm4fvjfzg"
ENV REACT_APP_AUTH0_CALLBACK_URL="https://skketsy.xyz"
ENV REACT_APP_API_BASE_URL="https://api.skketsy.xyz"
ENV REACT_APP_AUTH0_AUDIENCE="airbnb-clone-app-api"
ENV REACT_APP_GOOGLE_MAP_KEY="AIzaSyBT-ZipeKuIjY4ICzT8aZIqLDthwLQC_dQ"
ENV REACT_APP_MAP_ID="2e32cbf919ca80a5"
ENV REACT_APP_API_BASE_URL="https://api.skketsy.xyz"

# Set the working directory in the container for frontend
WORKDIR /app

# Copy frontend package.json and package-lock.json
COPY ./frontend/package*.json ./

# Install frontend dependencies
RUN npm install

# Copy the rest of the frontend application code
COPY ./frontend/ ./

# Expose port 3000
EXPOSE 3000

# Start Nginx server
CMD ["npm", "start"]
