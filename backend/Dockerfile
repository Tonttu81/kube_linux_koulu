FROM python:3.11-slim

WORKDIR /app

COPY backend/requirements.txt /app/requirements.txt
RUN pip install --no-cache-dir -r requirements.txt

COPY backend/ /app/

EXPOSE 7000

CMD ["gunicorn", "--workers", "3", "--bind", "0.0.0.0:7000", "app:app"]