# Step 1: Use the official Python 3.12-slim image
FROM python:3.12-slim

# Step 2: Set the working directory inside the container
WORKDIR /app

# Step 3: Copy the requirements file and install dependencies
COPY requirements.txt .
RUN pip install --no-cache-dir -r requirements.txt

# Step 4: Copy the application file
COPY app.py .

# Step 5: Set an environment variable for the CSV file
ENV METRICS_LOG_FILE=docker_system_inference_metrics.csv

# Step 6: Expose port 5000
EXPOSE 5000

# Step 7: Run the application
CMD ["python", "app.py"]
