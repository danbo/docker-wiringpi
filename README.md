# wiringpi
updated image that works with new versions of hypriot os (> 1.7.1)

- original docker hub image: https://hub.docker.com/r/hypriot/wiringpi/
- original docker file source: http://blog.hypriot.com/post/docker-sensor-fu-on-a-raspberry-pi/
- issue with hypriot os > 1.7.1 (kernel > 4.4.50): https://www.raspberrypi.org/forums/viewtopic.php?p=1234126
- hypriot os downloads: http://blog.hypriot.com/downloads/

tested on rpi 1b

build: docker build -t danbo/wiringpi:latest .
run: docker run --device /dev/ttyAMA0:/dev/ttyAMA0 --device /dev/mem:/dev/mem --privileged -ti danbo/wiringpi /loldht 7 5
