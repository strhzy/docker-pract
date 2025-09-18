FROM python:3.13-slim

WORKDIR /app

COPY requirements.txt .

RUN pip install -r requirements.txt

COPY . .

RUN pip install gunicorn

ENTRYPOINT ["sh", "-c"]

EXPOSE 8000
CMD ["python manage.py migrate --noinput && gunicorn --bind 0.0.0.0:8000 eshop.wsgi:application"]