# Get from docker repo
FROM python:3.9

# Working directory for the source files of the projetct
WORKDIR /usr/src/app

# Get the libraries python libraries for the project to run (to the working directory)
COPY requirements.txt ./

# Install the libraries
RUN pip install --no-cache-dir -r requirements.txt

# Copy all the content of the project directory to the container
COPY . .

# Run the app
CMD ["uvicorn", "main:app", "--host", "0.0.0.0", "--port", "80"]

