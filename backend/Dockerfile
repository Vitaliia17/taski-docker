FROM python:3.12

WORKDIR /app

RUN pip install --upgrade pip && pip install setuptools gunicorn==23.0.0

COPY requirements.txt .

RUN pip install -r requirements.txt --no-cache-dir

COPY . .

CMD ["gunicorn", "--bind", "0.0.0.0:8000", "backend.wsgi"]