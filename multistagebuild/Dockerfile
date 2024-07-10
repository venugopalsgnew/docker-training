# Stage 1: Build Stage
FROM python:3.9 as builder

# Set the working directory inside the container
WORKDIR /app

# Copy requirements.txt and install dependencies
COPY requirements.txt .
RUN pip install --upgrade pip \
    && pip install --no-cache-dir -r requirements.txt

# Copy the application code
COPY . .

# Perform any build steps here, if necessary
# For example, you could run tests, linting, etc.



# Stage 2: Production Stage
FROM python:3.9-slim

# Set the working directory inside the container
WORKDIR /app

# Copy only necessary files from the builder stage
COPY --from=builder /app /app

# Set environment variables, if needed
# ENV MY_ENV_VARIABLE=value

# Start the application
CMD ["python", "app/app.py"]

