FROM python:3.9

RUN git clone https://github.com/JoseFilipeFerreira/merossd

WORKDIR /merossd

RUN pip install -r requirements.txt

COPY config.yaml ./

CMD [ "python", "server.py" ]
