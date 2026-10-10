FROM python:3.13-slim

RUN groupadd -r Linux && useradd -r -g Linux Linux

WORKDIR /app

COPY requirements.txt .

RUN pip install --no-cache-dir -r requirements.txt

COPY ./app/app.py .

RUN chown -R Linux:Linux /app

EXPOSE 5000

CMD ["python", "app.py"]