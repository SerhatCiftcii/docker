FROM python:3.12-slim

# Python tamponlamayı kapat
ENV PYTHONUNBUFFERED=1

# Çalışma dizini
WORKDIR /django_app

# Sistem bağımlılıklarını yükle (psycopg2 için gerekli)
RUN apt-get update && apt-get install -y \
    gcc \
    libpq-dev \
    python3-dev \
    build-essential \
    && rm -rf /var/lib/apt/lists/*

# requirements dosyasını kopyala
COPY requirements.txt .

# pip güncelle ve bağımlılıkları kur
RUN pip install --upgrade pip \
    && pip install --no-cache-dir -r requirements.txt

# Django projesini container'a kopyala
COPY . .