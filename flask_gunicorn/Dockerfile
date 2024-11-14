# Use the official Python base image
FROM python:3.9

# Set the working directory in the container
WORKDIR /app

# Copy the requirements file to the container
COPY requirements.txt .

# Install the Python dependencies
RUN pip install --no-cache-dir -r requirements.txt

# Copy the Flask application code to the container
COPY . .

# Expose port 5000 for the Flask application
EXPOSE 5000

# Start Gunicorn to run the Flask application with 4 workers
CMD ["gunicorn", "--bind", "0.0.0.0:5000", "--workers", "4", "app:app"]

