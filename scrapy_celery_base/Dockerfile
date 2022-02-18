FROM python:3.10-alpine3.15
RUN apk add --no-cache --virtual .build-dependencies build-base libffi-dev curl-dev && \
    pip install celery==5.2.3 scrapy==2.5.1 pycurl urllib3 && \
    apk del --purge .build-dependencies && \
    pip cache purge
