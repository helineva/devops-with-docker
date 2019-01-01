FROM alpine:3.8

RUN apk add --no-cache bc bash git && \
    git clone https://github.com/helineva/bc-average.git /app && \
    apk del git && \
    chmod a+x /app/average.sh && \
    adduser -D app

USER app

ENTRYPOINT ["/app/average.sh"]
