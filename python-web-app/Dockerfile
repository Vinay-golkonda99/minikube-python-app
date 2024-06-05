FROM ubuntu:20.04

# Set the working directory inside the container
WORKDIR /app

# Copy the requirements file into the container
COPY requirements.txt .

# Copy the entire application directory into the container
COPY devops .

# Install Python and pip
RUN apt-get update && \
    apt-get install -y python3 python3-pip

# Install the required Python packages
RUN pip3 install -r requirements.txt

# Set the entry point and default command
ENTRYPOINT ["python3"]
CMD ["manage.py", "runserver", "0.0.0.0:8000"]
