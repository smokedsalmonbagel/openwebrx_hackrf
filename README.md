# openwebrx_hackrf
A docker build for openwebrx and the hackrf

-plug in hackrf
-enable in config_webrx.py (you can use the copy fromt his repo)
-run docker container  below:
docker run -it --rm -p 8073:8073 --device=/dev/bus/usb:/dev/bus/usb -v /path/to/config_webrx.py:/opt/openwebrx/config_webrx.py --name sdr --entrypoint "/bin/bash" tycon/openwebrx

or 

docker run -d --rm -p 8073:8073 --device=/dev/bus/usb:/dev/bus/usb -v /path/to/config_webrx.py:/opt/openwebrx/config_webrx.py --name sdr tycon/openwebrx

or 

build container from Dockerfile in this repo
