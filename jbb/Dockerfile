FROM python:3.9

RUN git clone https://github.com/JoseFilipeFerreira/jbb.py

WORKDIR /jbb.py

RUN pip install -r requirements.txt

COPY config.yaml client_secret.json credentials_calendar.json ./

CMD [ "python", "bot.py" ]
