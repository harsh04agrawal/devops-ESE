# Use official Python image
FROM python:3.12-slim

# Set working directory
WORKDIR /app

# Copy dependency file first (better caching)
COPY requirements.txt .

# Install dependencies
RUN pip install --no-cache-dir -r requirements.txt

# Copy rest of app code
COPY . .

# Default command (runs pytest when container starts)
CMD ["pytest", "-v"]
