# Use the official Python image as the base image
FROM python:latest

# Set the working directory in the container
WORKDIR /app

# Install Django
RUN pip install Django

# Create a new Django project
RUN django-admin startproject myproject .

# Copy the local requirements file to the container
COPY requirements.txt .

# Install Python dependencies
RUN pip install -r requirements.txt

# Expose the port that Django will run on
EXPOSE 8000

# Command to run the Django development server
CMD ["python", "manage.py", "runserver", "0.0.0.0:8000"]
