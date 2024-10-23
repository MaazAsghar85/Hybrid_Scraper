# Use a base image with Playwright
FROM mcr.microsoft.com/playwright:v1.48.1-focal

# Set the working directory
WORKDIR /app

# Copy the Playwright test files to the container
COPY . .

# Install dependencies
RUN apt-get update && apt-get install -y \
    libgbm-dev \
    libglib2.0-0 \
    libnss3 \
    libatk1.0-0 \
    libatk-bridge2.0-0 \
    libdrm2 \
    libxkbcommon-x11-0 \
    libxcomposite1 \
    libxrandr2 \
    libasound2 \
    libpangocairo-1.0-0 \
    libgtk-3-0 \
    libxshmfence1 \
    libegl1-mesa \
    libgbm1 \
    libxcursor1 \
    libxi6 \
    libxdamage1 \
    libxtst6 \
    libxinerama1

# Install Chromium
RUN apt-get install -y chromium-browser

# Install dependencies
RUN npm install

# Expose port (if needed for the app)
EXPOSE 8080

# Start the application (modify this if necessary)
CMD ["npx", "ts-node", "server/tests/example.spec.ts"]
