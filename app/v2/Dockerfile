FROM python:3.9-slim

# Set working directory
WORKDIR /app

# Copy the application code
COPY app.py .

# Install dependencies
RUN pip install flask

# Expose port
EXPOSE 80

# Run the application
CMD ["python", "app.py"]
