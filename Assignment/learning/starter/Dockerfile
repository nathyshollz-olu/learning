FROM python:3.11-slim
WORKDIR /app

# Copy dependencies file and install
COPY app/requirements.txt .
RUN pip install --no-cache-dir -r requirements.txt

# Copy the app code
COPY app/app.py .

ENV PORT=5000
EXPOSE 5000

CMD ["python", "app.py"]