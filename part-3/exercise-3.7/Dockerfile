FROM docker:latest

RUN apk add --no-cache git && \
    echo 'git clone $1 /app && \
          docker build -t $USERNAME/$2 /app && \
          docker login -u $USERNAME -p $PASSWORD && \
          docker push $USERNAME/$2 && \
          docker logout' >/script.sh

ENTRYPOINT ["sh", "/script.sh"]
