### Installation

### Kali Linux / Ubuntu / Parrot OS

```bash
apt upadte -y
apt upgrade -y
apt install git -y
git clone https://github.com/memes-bachha/seeker.git
cd seeker
apt install python3 python3-pip php
pip3 install requests
```

### BlackArch Linux

```bash
pacman -S seeker
```

### Termux

```bash
pkg update -y
pkg upgrade -y
pkg install git curl php python -y
git clone https://github.com/memes-bachha/seeker.git
cd seeker
pip3 install requests
python3 seeker.py -t manual
```
### Docker

```bash
docker pull memes-bachha/seeker
```

## Usage

```bash
python3 seeker.py -h

usage: seeker.py [-h] [-s SUBDOMAIN]

optional arguments:
  -h, --help            show this help message and exit
  -k KML, --kml         Provide KML Filename ( Optional )
  -p PORT, --port       Port for Web Server [ Default : 8080 ]
  -t TUNNEL, --tunnel   Specify Tunnel Mode [ Available : manual ]

##################
# Usage Examples #
##################

# Step 1 : In first terminal
$ python3 seeker.py -t manual

# Step 2 : In second terminal start a tunnel service such as ngrok
$ ./ngrok http 8080

###########
# Options #
###########

# Ouput KML File for Google Earth
$ python3 seeker.py -t manual -k <filename>

# Use Custom Port
$ python3 seeker.py -t manual -p 1337
$ ./ngrok http 1337

################
# Docker Usage #
################

# Step 1
$ docker network create ngroknet

# Step 2
$ docker run --rm -it --net ngroknet --name seeker memes-bachha/seeker

# Step 3
$ docker run --rm -it --net ngroknet --name ngrok wernight/ngrok ngrok http seeker:8080
```
