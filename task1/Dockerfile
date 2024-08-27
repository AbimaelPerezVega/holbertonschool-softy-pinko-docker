# Use the latest Ubuntu as the base image
FROM ubuntu:latest

# Update the package repository and upgrade existing packages
RUN apt-get update && apt-get upgrade -y

# Install Python3 and pip3
RUN apt-get install -y python3 python3-pip

# Remove EXTERNALLY-MANAGED error file if present
RUN rm -f /usr/lib/python*/EXTERNALLY-MANAGED

# Install Flask using pip3
RUN pip3 install flask

# Set the working directory to /app
WORKDIR /app

# Copy the Flask app file into the Docker image
COPY ./api.py /app/api.py

# Run the Flask app
CMD ["python3", "api.py"]
