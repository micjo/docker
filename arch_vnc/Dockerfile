FROM base/archlinux
#RUN pacman -Syu --debug
#RUN pacman -S xorg-xeyes

RUN pacman -Syyu --noconfirm
RUN pacman-db-upgrade
RUN pacman -S xorg-server --noconfirm
RUN pacman -S xorg-xeyes --noconfirm


# for setup with x11vnc
RUN pacman -S x11vnc --noconfirm
RUN pacman -S xorg-server-xvfb --noconfirm
RUN mkdir /root/.vnc/
RUN x11vnc -storepasswd 1234 /root/.vnc/passwd

#Installing lxde
RUN pacman -S lxde-common openbox lxsession --noconfirm

#Firefox for testing stuff
RUN pacman -S firefox --noconfirm
