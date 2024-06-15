
FROM python:3.13


WORKDIR /usr/src/app


COPY requirements.txt ./


RUN pip install --no-cache-dir -r requirements.txt


COPY . .


RUN python manage.py migrate && python manage.py collectstatic --noinput


EXPOSE 9000


CMD ["gunicorn", "myproject.wsgi:application", "--bind", "0.0.0.0:8000"]
