FROM python:3.9-alpine

# RUN useradd -ms /bin/bash colorME 
RUN addgroup -S colorgroup && adduser -S colorme -G colorgroup -h /home/colorme

#switch to non-root user
USER colorme
WORKDIR /home/colorme

# Copy application files and set correct ownership
COPY --chown=colorme:colorgroup . /home/colorme/

RUN pip install --user -r requirements.txt

EXPOSE 8080

ENV APP_COLOR=red
ENV VERSION=v1

ENTRYPOINT ["python", "app.py"]
