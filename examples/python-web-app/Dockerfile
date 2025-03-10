FROM alpine

WORKDIR /app

COPY requirements.txt /app/
COPY devops /app/

RUN apk add --no-cache \
    gcc \
    musl-dev \
    libffi-dev \
    python3-dev \
    libxml2-dev \
    libxslt-dev \
    && python3 -m ensurepip --upgrade
#    && pip install --no-cache --upgrade pip setuptools wheel
#RUN apt-get update && apt-get install -y python3 python3-pip python3-venv

SHELL ["/bin/bash", "-c"]

RUN python3 -m venv venv1 && \
source venv1/bin/activate && \
pip install --no-cache --upgrade pip setuptools wheel && \
pip install --no-cache-dir -r requirements.txt

EXPOSE 8000

CMD source venv1/bin/activate && python3 manage.py runserver 0.0.0.0:8000




