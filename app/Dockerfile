FROM python:3.9-alpine

# RUN useradd -ms /bin/bash colorME 
RUN adduser -D -h /home/colorme colorme
USER colorme
WORKDIR /home/colorme

COPY . .
RUN pip install --user -r requirements.txt

EXPOSE 8080

ENV APP_COLOR=red
ENV VERSION=v1

ENTRYPOINT ["python", "app.py"]
