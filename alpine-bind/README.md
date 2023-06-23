bind based on alpine

Small alpine container with bind package installed.

Usage

docker run -d \
  --name=bind \
  -p 172.16.77.254:53:53/udp \
  -v /srv/bind/named.conf:/etc/bind/named.conf:ro \
  -v /srv/bind/lab:/etc/bind/lab:ro \
  -v /srv/bind/lab-rev:/etc/bind/lab-rev:ro \
  --restart unless-stopped \
  pkoperwas/alpine-bind
