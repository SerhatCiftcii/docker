FROM python:3.12-slim
# NE İŞE YARAR PYTHONUNBUFFERED? 
# PYTHONUNBUFFERED=1, Python'un standart çıktı ve hata akışlarının tamponlanmamasını sağlar. Bu, uygulamanın çıktısının anında terminale yazılmasını sağlar, bu da özellikle Docker konteynerlerinde logların gerçek zamanlı olarak görüntülenmesi için faydalıdır. Normalde, Python çıktıyı tamponlar ve belirli bir miktar veri biriktiğinde veya program sona erdiğinde terminale yazar. Bu ortam değişkeni sayesinde, her çıktı hemen terminale yazılır, bu da hata ayıklama ve izleme süreçlerini kolaylaştırır.
ENV PYTHONUNBUFFERED=1


WORKDIR /django_app
COPY requirements.txt .
RUN pip install --no-cache-dir -r requirements.txt


