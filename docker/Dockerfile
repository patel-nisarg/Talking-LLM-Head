# Use an official NVIDIA PyTorch image as a parent image
FROM pytorch/pytorch:latest

# Set the working directory in the container
WORKDIR /workspace

# Install any needed packages specified in requirements.txt
COPY requirements.txt /workspace/
RUN pip install --no-cache-dir -r requirements.txt

# Copy the current directory contents into the container at /workspace
COPY . /workspace

# Make port 80 available to the world outside this container
EXPOSE 80

# Define environment variable
ENV NAME World

# Run app.py when the container launches
CMD ["python", "main.py"]
