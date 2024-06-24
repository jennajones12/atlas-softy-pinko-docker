# Use Ubuntu 22.04 as base image
FROM ubuntu:22.04

# Update package lists and install software
RUN apt-get update

RUN apt-get upgrade -y

RUN apt-get install -y python3 python3-pip

# Install Flask
RUN pip3 install Flask

# Install Flask-cors
RUN pip3 install Flask-cors

# Set working directory in container
WORKDIR /app

# Cp local api.py file into container at /app
COPY api.py /app/api.py

# Expose port 5252 to outside world
EXPOSE 5252

# Run Flask application
CMD ["python3", "api.py"]
