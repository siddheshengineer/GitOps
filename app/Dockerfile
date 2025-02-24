FROM python:3.9-alpine
WORKDIR /opt

COPY . /opt/
RUN pip install -r /opt/requirements.txt

EXPOSE 8080

ENV APP_COLOR=red
ENV VERSION=v1

ENTRYPOINT ["python", "app.py"]
