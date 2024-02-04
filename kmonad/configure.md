download kmonad from here
https://github.com/kmonad/kmonad/releases

sudo chmod +x kmonad

mv kmonad /usr/bin/kmonad

add file below to systemd service

anyname.service
```
[Unit]
Description=kmonad keyboard config

[Service]
Restart=always
RestartSec=3
ExecStart=/usr/bin/kmonad/kmonad  /home/dracu/.config/kmonad/ansi_keyboard.kbd
Nice=-20

[Install]
WantedBy=default.target
```




