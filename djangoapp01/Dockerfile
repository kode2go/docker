FROM python:3.9-alpine

WORKDIR /app

COPY requirements.txt .

RUN pip install -r requirements.txt && \
    django-admin startproject myproject .

EXPOSE 8000

CMD ["python", "manage.py", "runserver", "0.0.0.0:8000"]
