FROM alpine:3.7

MAINTAINER nanichowdary.ravilla@gmail.com

ARG proxy
ENV https_proxy=$proxy \
	LANG=en_US.UTF-8 \
	LC_ALL=en_US.UTF-8

RUN echo "ipv6" >> /etc/modules

RUN apk --update add build-base && \
	apk add alpine-sdk && \
	apk add libressl-dev && \
	apk add openssl && \
	apk add libffi && \
	apk add libffi-dev && \
	apk add --no-cache python3 && \
	apk add --no-cache python3-dev && \
	apk add --no-cache py-pip && \
	python3 -m ensurepip && \
	rm -r /usr/lib/python*/ensurepip && \
	pip3 install --upgrade pip setuptools && \
	pip install cryptography && \
	rm -r /root/.cache

RUN mkdir /app
WORKDIR /app

RUN python3 -V

CMD ["python3"]
