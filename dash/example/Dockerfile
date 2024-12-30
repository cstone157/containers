# Use a slim base image to reduce image size
FROM python:3.9-slim-buster

# Set the working directory inside the container
WORKDIR /dash

# Copy the requirements file first, so we can install dependencies before copying the app
COPY ./work/requirements.txt .
COPY ./work/app.py .

# Install Python dependencies
RUN pip install --no-cache-dir -r requirements.txt

# Copy the application code
COPY ./work/app/* ./app/

# Update the work directory
WORKDIR /dash/app

# Expose the port that the Dash app will use (8050)
EXPOSE 8050

# Define the command to run the app
CMD ["gunicorn", "--bind", "0.0.0.0:8050", "app:server"]