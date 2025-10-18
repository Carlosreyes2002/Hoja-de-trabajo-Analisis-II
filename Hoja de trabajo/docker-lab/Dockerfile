# Base image
FROM python:3.11-slim

# Set working directory
WORKDIR /app

# Install system dependencies for psycopg2
RUN apt-get update && apt-get install -y \
    gcc \
    postgresql-client \
    libpq-dev \
    && rm -rf /var/lib/apt/lists/*

# Copy files
COPY . .

# Install dependencies
RUN pip install -r requirements.txt

# Expose Flask default port
EXPOSE 5000

# Run the app
CMD ["python", "app.py"]
