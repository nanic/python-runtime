FROM alpine:3.7

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
	rm -r /root/.cache

RUN mkdir /app
WORKDIR /app

RUN python3 -V

CMD ["python3"]
