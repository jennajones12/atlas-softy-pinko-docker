# Use Ubuntu 22.04 as base image
FROM ubuntu:22.04

# Update pkg lists, upgrade existing pkgs, install dependencies
RUN apt-get update \
    && apt-get upgrade -y \
        python3 \
        python3-pip \
    && apt-get clean \
    && rm -rf /var/lib/apt/lists/*

# Set working directory
WORKDIR /app

# Copy app files into container
COPY api.py /app/api.py

# Install Flask and Flask-cors
RUN pip3 install flask flask-cors

# Expose port 5252
EXPOSE 5252

# Run Flask application
CMD ["python3", "/app/api.py"]
