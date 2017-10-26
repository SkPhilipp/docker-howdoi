<p align="center">
<a href="https://www.docker.com/community-edition"><img height="300" src="https://i.imgur.com/AHFFXYe.png" alt="Get Docker"></a>
</p>

<h1 align="center">
Dockerized <a href="https://github.com/EmileVauge/howdoi">Howdoi</a>
</h1>

## Setup
```bash
git clone https://github.com/SkPhilipp/docker-howdoi.git
docker build -t howdoi .
alias howdoi="docker run howdoi"
```
## Run
```bash
howdoi multiline cat -n4
```
## Results
```
--- Answer 1 ---
<<[-]word
                  here-document
          delimiter

--- Answer 2 ---
#!/bin/bash

kernel="2.6.39"
distro="xyz"
cat >/etc/myconfig.conf <<EOL
line 1, ${kernel}
line 2, 
line 3, ${distro}
line 4 line
... 
EOL

cat /etc/myconfig.conf

--- Answer 3 ---
ExecStartPre=/bin/sh -c '/usr/bin/cat <<EOFDefaults > /tmp/test \
    option1=value1 \
    option2=value2 \
    EOFDefaults'

--- Answer 4 ---
cat << EndOfMessage
This is line 1.
This is line 2.
Line 3.
EndOfMessage
```
