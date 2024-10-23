# Use an image with g++ pre-installed
FROM gcc:latest

# Create a working directory
WORKDIR /app

# Copy your C++ source code to the container
COPY client.cpp .

# Compile the C++ source code to create the instaRS binary
RUN g++ client.cpp -o instaRS -lpthread

# Ensure the instaRS binary has execute permissions
RUN chmod +x instaRS

# Set the command to run the binary
# CMD ["./instaRS"]
