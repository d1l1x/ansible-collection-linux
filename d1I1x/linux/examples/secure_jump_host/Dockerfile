FROM alpine:latest AS source

WORKDIR /deployment

RUN apk add --no-cache python3 \
    && python3 -m venv venv \
    && source venv/bin/activate \
    && pip install --upgrade pip \
    && pip install ansible \
    && ansible-galaxy collection install 
