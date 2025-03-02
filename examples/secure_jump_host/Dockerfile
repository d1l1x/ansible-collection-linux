FROM alpine:latest AS source

WORKDIR /app

COPY requirements.yml .

RUN apk add --no-cache python3 git \
    && python3 -m venv venv \
    && source venv/bin/activate \
    && pip install --upgrade pip \
    && pip install ansible

RUN source venv/bin/activate \
    && ansible-galaxy install -r requirements.yml

ENV PATH="/app/venv/bin:$PATH"
ENTRYPOINT [ "ansible-playbook" ]
