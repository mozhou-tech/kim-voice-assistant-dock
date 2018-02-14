FROM resin/armhf-alpine:3.6

LABEL io.resin.device-type="raspberry-pi"
LABEL author="tenstone"

RUN echo -e "http://mirrors.aliyun.com/alpine/v3.7/main\nhttp://mirrors.aliyun.com/alpine/v3.7/community" > /etc/apk/repositories \
    && apk add --update  --no-cache \
		less \
		net-tools \
		python3 \
		ifupdown \
		usbutils \
		gnupg \
		raspberrypi \
		raspberrypi-libs \
		raspberrypi-dev \
#	&& pip install python-pyaudio pyaudio python3-pyaudio sox RPi.GPIO RPIO
