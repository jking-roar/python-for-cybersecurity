# Use an official Python runtime as a parent image
FROM python:3.13-slim

# Set the working directory in the container
WORKDIR /app

# Copy the requirements.txt from the /downloads folder into the container
COPY ./downloads/requirements.txt /app/requirements.txt

# Install the necessary dependencies from requirements.txt
RUN pip install --no-cache-dir -r /app/requirements.txt

# Copy the rest of the project files into the container
COPY . /app

# Command to run the application
CMD ["python", "your_script.py"]
