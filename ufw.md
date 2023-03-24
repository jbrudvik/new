# New [UFW](https://launchpad.net/ufw) firewall

## Create new UFW firewall allowing SSH, HTTP, and HTTPS

```sh
$ sudo ufw default deny incoming
$ sudo ufw default allow outgoing
$ sudo ufw allow ssh
$ sudo ufw allow http
$ sudo ufw allow https
$ sudo ufw enable

$ sudo ufw status verbose
```

## ...and make changes

- Allow connections to a particular port: `$ sudo ufw allow 8080`
  - Stop allowing connections to the port: `$ sudo ufw delete allow 8080`
- Block all HTTP traffic: `$ sudo ufw deny http`
  - Re-allow HTTP traffic: `$ sudo ufw allow http`
- Allow connections to PostgreSQL: `$ sudo ufw allow postgres`
  - Stop allowing connections to PostgreSQL: `$ sudo ufw delete allow postgres`

## ...and disable the firewall (opening up to all traffic!)

```sh
$ sudo ufw disable
```
