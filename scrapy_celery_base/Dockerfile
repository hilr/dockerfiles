FROM python:3.10-alpine3.15
RUN apk add --no-cache --virtual .build-dependencies build-base libffi-dev curl-dev && \
    PYCURL_SSL_LIBRARY=openssl pip install celery==5.2.3 scrapy==2.5.1 pycurl urllib3 xlrd==1.2.0 scrapy_spiders && \
    apk del --purge .build-dependencies && \
    apk add libcurl && \
    pip cache purge
