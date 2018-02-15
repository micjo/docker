# Launching with x11 access

## On the host:
Build the docker image
```
docker build . -t ubu_x11
```

Start the Xephyr nested x server
```
Xephyr :1
```

Run the image and connect to the Xephyr virtual x window
```
docker run -e DISPLAY=:1 -v /tmp:/tmp --ipc=host --pid=host -it ubu_x11 /bin/bash
```

## In the container:
Run a graphical application:
```
startlxde &
```

# TODO
* Fix the ``No session for pid ...`` Error when running ``startlxde &``.
* Shouldnt run ``startlxde &`` as root
* Get ``startlxde &`` running on arch
