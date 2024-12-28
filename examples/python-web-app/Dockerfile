FROM ubuntu

WORKDIR /app

COPY requirements.txt /app
COPY devops /app

RUN apt-get update && \
    apt install -y python3.12.1 && \
    apt-get install -y python3.12.1-pip && \
    pip install -r requirements.txt && \
    cd devops

ENTRYPOINT ["python3.12.1"]
CMD ["manage.py", "runserver", "0.0.0.0:8000"]




