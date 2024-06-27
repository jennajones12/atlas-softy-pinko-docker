# Use Ubuntu 22.04 as base image
FROM ubuntu:22.04

# Set working directory in container
WORKDIR /app

# Cp local api.py file into container at /app
COPY api.py /app/api.py

# Update package lists and install packages
RUN apt-get update && apt-get install -y \
    python3 \
    python3-pip \
    && apt-get clean

# Install Flask
RUN pip3 install flask flask-cors

# Expose port 5252 to outside world
EXPOSE 5252

# Run Flask application
CMD ["python3", "/app/api.py"]
