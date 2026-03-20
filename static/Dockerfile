# Use an official Python runtime as a parent image
FROM python:3.9

# Set the working directory for subsequent instructions

WORKDIR /opt/todo/app

COPY requirements.txt ./

RUN pip install --no-cache-dir -r requirements.txt

RUN groupadd -r appgroup && useradd -r -g appgroup -s /bin/bash todouser 

RUN chown -R todouser:appgroup /opt/todo/app

USER todouser

CMD ["python", "app.py"]


