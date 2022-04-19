FROM python:latest

COPY config requirements.txt ./

RUN pip install -r requirements.txt

CMD [ "python", "-m", "radicale", "--config", "config" ]
