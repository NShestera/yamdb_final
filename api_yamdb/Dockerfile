FROM python:3.7-slim

# arm64
ARG BUILD_DEPS="build-essential libpq-dev"
RUN set -ex && \
    apt-get update && \
    apt-get install -y --no-install-recommends $BUILD_DEPS && \
    rm -rf /var/lib/apt/lists/*
WORKDIR /app
COPY requirements.txt .
RUN pip3 install -r ./requirements.txt --no-cache-dir
COPY . . 
CMD ["gunicorn", "api_yamdb.wsgi:application", "--bind", "0.0.0.0:8000"]
