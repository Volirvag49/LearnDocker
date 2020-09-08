FROM python:3.8

RUN groupadd -r uwsgi && useradd -r -g uwsgi uwsgi
WORKDIR /app
COPY app /app
COPY cmd.sh /
COPY requirements.txt requirements.txt
RUN pip install -r requirements.txt

EXPOSE 9090 9191
USER uwsgi

CMD ["/cmd.sh"]
