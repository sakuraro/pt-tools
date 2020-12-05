FROM archlinux
RUN cd /etc/pacman.d && \
    cp mirrorlist mirrorlist.backup && \
    echo "Server = https://mirrors.tuna.tsinghua.edu.cn/archlinux/\$repo/os/\$arch" > mirrorlist && \
    pacman -Syyu --noconfirm
RUN pacman -S nano vi qbittorrent-nox rclone --noconfirm
VOLUME [ "/home/qbt/.config/qBittorrent", "/home/qbt/.local/share/data/qBittorrent", "/home/qbt/Downloads", "/home/qbt/.config/rclone/rclone.conf" ]
EXPOSE 8080
CMD [ "qbittorrent-nox" ]