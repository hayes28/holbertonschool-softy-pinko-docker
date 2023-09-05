# Use the latest version of Ubuntu as the base image
FROM ubuntu:latest

# Update APT package list and upgrade installed packages
RUN apt-get update && apt-get upgrade -y

# Install Python3 and pip3
RUN apt-get install -y python3 python3-pip

# Install Flask using pip3
RUN pip3 install Flask

# Set the working directory to /app
WORKDIR /app

# Copy the api.py file into the /app directory in the container
COPY ./api.py /app/api.py

# Command to run the Flask app
CMD ["python3", "api.py"]
