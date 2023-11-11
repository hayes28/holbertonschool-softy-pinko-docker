# Use an official Python runtime as a parent image
FROM ubuntu:latest

# Set the working directory in the container
WORKDIR /app

# Install python3 and pip3
RUN apt-get update && \
    apt-get install -y python3 python3-pip

# Install Flask
RUN pip3 install flask

# Copy the current directory contents into the container at /app
COPY api.py /app/api.py

# Make port 5252 available to the world outside this container
EXPOSE 5252

# Define environment variable
ENV NAME World

# Run api.py when the container launches
CMD ["python3", "api.py"]
