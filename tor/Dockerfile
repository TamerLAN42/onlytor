FROM alpine
RUN apk add --no-cache tor proxychains-ng nano curl obfs4proxy
COPY proxychains.conf /etc/proxychains/proxychains.conf
RUN adduser -D -h /home/toruser -s /bin/sh toruser
USER toruser
WORKDIR /home/toruser
CMD ["tor"]
