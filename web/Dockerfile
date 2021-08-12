FROM python:3.7

LABEL version="1.0" description="django+uwsgi+nginx+postgresql"

COPY ./mysite /var/www/html/mysite

WORKDIR /var/www/html/mysite

RUN pip install -r requirements.txt

RUN useradd -D user

USER user

ENTRYPOINT [ "/bin/bash", "start.sh" ]