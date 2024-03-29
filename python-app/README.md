# Python Flask Application Setup:

## Step 1: Set Up Flask Application
#### 1. Install Flask: If you haven't already installed Flask, you can do so using pip:

    pip install Flask

#### 2. Create app.py: Copy your provided app.py and save it in your project directory.

## Step 2: Test the Flask Application
#### Ensure that the Flask application runs correctly by executing app.py:

    python app.py

#### Your Flask application should start, and you should be able to access it in your web browser at http://localhost:5000.

## Step 3: Create a Dockerfile
#### Now, let's create a Dockerfile to containerize the Flask application.

#### 1. Create a file named Dockerfile in your project directory.

#### 2. Write the Dockerfile:

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

## Step 4: Build Docker Image
#### Navigate to your project directory in the terminal and run the following command to build your Docker image:

    docker build -t flask-app .

## Step 5: Run Docker Container
#### After the build is successful, you can run the Docker container:

    docker run -p 5000:5000 flask-app
