# Use the official Python image from the Docker Hub as the base image
FROM python:3.9.19-slim

# Set the working directory in the container
WORKDIR /app

# Copy the requirements.txt file into the container
COPY requirements.txt .

# Install the dependencies specified in requirements.txt
RUN pip install --no-cache-dir -r requirements.txt

# Copy the rest of the application code into the container
COPY . .

# Expose the port the application will run on
EXPOSE 5000

# Specify the command to run the application
CMD ["python", "app.py"]
