# Launching with vnc server:

## On the host:
Build the docker image:
```
docker build . -t arch_vnc
```

Start the docker image.
```
docker run -p 5900:5900 -it arch_vnc /bin/bash
```
## In the container:
Set the display variable
```
export DISPLAY=:1
```

Launch Xvfb
```
Xvfb :1 -screen 0 1024x768x16 &
```

Launch a graphical application
```
firefox &
```

Start the vnc server
```
x11vnc -display :1 -forever -usepw &
```

## On the host:
Connect with your favorite VNC viewer to localhost:5900 with password 1234.
