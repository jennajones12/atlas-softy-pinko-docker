# Use Ubuntu 22.04 as base image
FROM ubuntu:22.04

# Update package lists and install dependencies
RUN apt-get update
RUN apt-get install -y python3 python3-pip
RUN apt-get clean

# Create and set working directory
WORKDIR /app

# Copy application files into the container
COPY api.py /app/api.py

# Install Flask and Flask-cors
RUN pip3 install flask 
RUN pip3 install flask-cors

# Expose port 5252 to outside world
EXPOSE 5252

# Run Flask application
CMD ["python3", "/app/api.py"]
