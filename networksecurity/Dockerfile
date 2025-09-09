FROM python:3.10-slim-buster

WORKDIR /app

# Copy everything into container
COPY . /app

# Install dependencies
RUN apt-get update && apt-get install -y awscli \
    && pip install --no-cache-dir -r requirements.txt

# Run FastAPI with Uvicorn instead of raw python
CMD ["uvicorn", "app:app", "--host", "0.0.0.0", "--port", "8000"]
