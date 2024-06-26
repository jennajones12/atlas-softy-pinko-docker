# Use Ubuntu 22.04 as base image
FROM ubuntu:22.04

# Set working directory in container
WORKDIR /app

# Cp local api.py file into container at /app
COPY api.py /app/api.py

WORKDIR /app
COPY . /app
RUN apt-get update 
RUN apt-get install -y software-properties-common
RUN add-apt-repository universe

ENV PYTHONUNBUFFERED=1
RUN apt install -y python3
RUN apt-get -y install python3-pip
RUN pip install --no-cache --upgrade pip setuptools

# Expose port 5252 to outside world
EXPOSE 5252

# Run Flask application
CMD ["python3", "api.py"]
