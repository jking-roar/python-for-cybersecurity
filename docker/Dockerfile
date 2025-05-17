# Use an official Python runtime as a parent image
FROM python:3.13-slim

# Set the working directory in the container
WORKDIR /app

# Copy the requirements.txt from the /downloads folder into the container
COPY ./chapters/requirements.txt /app/requirements.txt

# upgrade pip to the latest version
RUN python -m pip install --upgrade pip
# Install the necessary dependencies from requirements.txt
RUN pip install --no-cache-dir -r /app/requirements.txt

# copy the chapters folders into the container
