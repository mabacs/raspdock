FROM kafebob/rpi-alpine-base:3.6

RUN addgroup -g 1000 node && \
    adduser -u 1000 -G node -s /bin/sh -h /home/node -D node && \
    apk add --update --no-cache nodejs-npm && \
    rm -rf /tmp/* /var/cache/apk/*