# python-runtime

A Docker file to create an image with python runtime

If the image is built inside a private network, you can mention gateway to proxy through

docker build --build-arg proxy=<hostname:port> -t <image-tag> .
