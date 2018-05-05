# retroproxy :)
Retrocomputing web proxy eliminates TLS

I'm made changes in macproxy project to adapt for newer machines like iMac G3

# Requirements
- Python 2.7

# How to setup
- Run pip install -r requirements.txt OR sudo pip install -r requirements.txt
- Run python proxy.py 
- Set proxy on retro machine to IP:5000
- Be happy =)

# Systemd setup

- Create a file named /lib/systemd/system/proxymac.service
- Paste this:

\[Unit\]

Description=MAC Proxy

\[Service\]

Type=simple
ExecStart=/usr/bin/python [PATH TO PROXY]/proxy.py

\[Install\]

WantedBy=multi-user.target

- Run systemctl enable proxymac
- Run systemctl start proxymac


Based in https://github.com/tghw/macproxy
