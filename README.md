# Docker Files
Some docker files for various purposes


## Launching with x11 forwarding:
Start the docker image. (Puts you in a container)

```
docker run -p 5900 -it arch /bin/bash
```

Set the display variable
```
export DISPLAY=:1
```

Configure Xvfb to display to this display
```
Xvfb :1 -screen 0 1024x768x16 &
```

Launch a graphical application
```
firefox &
```

Start the vnc server
```
x11vnc -display :1 -forever -usepw
```

## Launching with X forwarding:
Run on the host:
```
Xephyr :1
```

Start docker image.
```
docker run -e DISPLAY=:1 -v /tmp:/tmp --ipc=host --pid=host -it arch /bin/bash
```


