# Use the official Python image
FROM python:3.8-slim

# Set the working directory in the container
WORKDIR /app

# Copy the current directory contents into the container at /app
COPY . /app

# Install Flask
RUN pip install Flask

# Expose the port Flask runs on
EXPOSE 5000

# Run the application
CMD ["python", "app.py"]

