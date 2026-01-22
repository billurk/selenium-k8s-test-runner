FROM python:3.11-slim

# Chrome
RUN apt-get update && apt-get install -y \
    curl \
    && rm -rf /var/lib/apt/lists/*

WORKDIR /tests

COPY docker/requirements.txt .
RUN pip install --no-cache-dir -r requirements.txt

COPY tests/ ./tests

CMD ["pytest", "-v", "tests"]
