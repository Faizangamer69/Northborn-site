# 1️⃣ Build stage
FROM node:20-alpine AS builder

# Set working directory
WORKDIR /app

# Install dependencies
COPY package*.json ./
RUN npm install

# Copy all project files
COPY . .

# Build the Next.js app
RUN npm run build

# 2️⃣ Production stage
FROM node:20-alpine AS runner

WORKDIR /app
ENV NODE_ENV=production

# Copy only the necessary files from build stage
COPY --from=builder /app/.next ./.next
COPY --from=builder /app/public ./public
COPY --from=builder /app/package*.json ./
COPY --from=builder /app/next.config.ts ./

# Install only production dependencies
RUN npm install --omit=dev

# Expose port 3000
EXPOSE 3000

# Start the app
CMD ["npm", "run", "start"]
