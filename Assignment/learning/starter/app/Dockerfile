FROM python:3.11-slim

WORKDIR /app

# Copy dependencies file and install
COPY app/requirements.txt .
RUN pip install --no-cache-dir -r requirements.txt

# Install curl so Compose healthchecks can use it
RUN apt-get update && apt-get install -y curl && rm -rf /var/lib/apt/lists/*

# Copy the app code
COPY app/app.py .

# App defaults
ENV PORT=5000
EXPOSE 5000

CMD ["python", "app.py"]
