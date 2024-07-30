FROM node:16

# Set the working directory
WORKDIR /app

EXPOSE 5000

ENV REACT_APP_BACKEND_URL=http://localhost:8080

# Copy the package.json and yarn.lock files to the working directory
COPY package.json ./

# Install dependencies
RUN npm install

RUN npm install -g serve

# Copy the rest of the application code to the working directory
COPY . .

# Build the application
RUN npm run build

CMD ["serve", "-s", "build", "-l", "5000"]


