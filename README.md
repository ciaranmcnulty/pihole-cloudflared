# Pihole DNS-over-HTTPS config

This uses 2 existing docker images to run pihole and cloudflared, configured to proxy all DNS over HTTPS

This does *not* use pihole's DHCP functionality; you need to give the device a static IP address and make sure devices on your network are using it as their DNS server.

## Usage

Copy `.env.dist` to `.env` and populate with an admin password for pihole and a hostname for it

To start: `docker-compose up -d`

To stop: `docker-compose down`

## Notes

Pihole grabs a lot of ports; this may conflict with other containers

Blocking port 53 outbound at your router firewall is now possible if you want to ensure all DNS is over HTTPS
