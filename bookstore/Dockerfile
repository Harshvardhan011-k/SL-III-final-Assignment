# Use an official Python runtime as the base image
FROM python:3.9-slim

# Set the working directory in the container
WORKDIR /app

# Copy the current directory contents into the container
COPY . /app

# Install the dependencies from the requirements.txt file
RUN pip install --no-cache-dir -r requirements.txt

# Expose the Django app on port 8000
EXPOSE 8000

# Run Django migrations and start the app when the container is run
CMD ["sh", "-c", "python manage.py migrate && python manage.py runserver 0.0.0.0:8000"]
