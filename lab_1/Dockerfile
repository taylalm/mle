# last updated Mar 25 2025, 11:00am
FROM python:3.12-slim

# Set the working directory
WORKDIR /app

# Copy the requirements file into the container
COPY requirements.txt ./

# Install dependencies
RUN pip install --no-cache-dir -r requirements.txt

# Expose the default JupyterLab port
EXPOSE 8888

# Create a volume mount point for notebooks
VOLUME /app

# Set environment variable to enable JupyterLab
ENV JUPYTER_ENABLE_LAB=yes

# Set up the command to run JupyterLab
CMD ["jupyter", "lab", "--ip=0.0.0.0", "--port=8888", "--no-browser", "--allow-root", "--notebook-dir=/app"]
