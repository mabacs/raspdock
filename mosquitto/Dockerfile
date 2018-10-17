FROM resin/rpi-raspbian:jessie
# FROM debian:jessie

ARG MQTT_USERNAME
ARG MQTT_PASSWORD

RUN apt-get -y update && apt-get -y upgrade \
    && apt-get -y install wget \
    && wget http://repo.mosquitto.org/debian/mosquitto-repo.gpg.key \
    && apt-key add mosquitto-repo.gpg.key \
    && cd /etc/apt/sources.list.d/ \
    && wget http://repo.mosquitto.org/debian/mosquitto-jessie.list \
    && apt-get -y install apt-transport-https \
    && apt-get -y update \
    && apt-get -y install mosquitto

RUN touch /etc/mosquitto/pwfile

RUN mosquitto_passwd -b /etc/mosquitto/pwfile $MQTT_USERNAME $MQTT_PASSWORD

CMD ["mosquitto", "-c", "/mosquitto/mosquitto.conf"]
