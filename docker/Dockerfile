FROM python:3-slim

RUN apt-get update && apt-get install -y \
    make \
 && rm -rf /var/lib/apt/lists/*

WORKDIR /docs

COPY ./docker/requirements.txt ./requirements.txt
RUN pip install -r requirements.txt

COPY ./ ./
CMD make help
