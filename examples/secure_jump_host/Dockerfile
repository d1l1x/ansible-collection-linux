FROM alpine:latest AS source

WORKDIR /deployment

COPY requirements.yml .

RUN apk add --no-cache python3 git \
    && python3 -m venv venv \
    && source venv/bin/activate \
    && pip install --upgrade pip \
    && pip install ansible \
    && ansible-galaxy install -r requirements.yml
