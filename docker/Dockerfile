FROM python:3.13-slim

# Install system dependencies required to build Python packages with C extensions
RUN apt-get update && \
    apt-get install -y --no-install-recommends \
    build-essential \
    gcc \
    g++ \
    make \
    python3-dev \
    libffi-dev \
    libssl-dev && \
    rm -rf /var/lib/apt/lists/*

# Set working directory
WORKDIR /app

RUN python -m pip install --upgrade pip

# Copy requirements and install dependencies
COPY ./chapters/requirements.txt /app/requirements.txt
RUN pip install --no-cache-dir -r /app/requirements.txt

# Copy project code
#COPY . /app
#
#CMD ["python", "your_script.py"]
