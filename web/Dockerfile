# Stage 1: Build the Vite app
FROM node:20-alpine AS builder

# Upgrade npm
RUN npm install -g npm@latest

WORKDIR /app
COPY . .
RUN npm install
RUN npm run build


# Stage 2: Serve with a minimal static server
FROM node:20-alpine

# Install serve to serve the dist directory
RUN npm install -g serve

WORKDIR /app

# Copy built app from builder stage
COPY --from=builder /app/dist ./dist

# Serve the static files on port 3000
EXPOSE 3000
CMD ["serve", "-s", "dist", "-l", "3000"]
