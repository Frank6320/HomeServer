# HomeServer

This is the first commit of my HomeServer. Core part is FHEM.

**Change all the passwords for mySQL, FHEM, NodeRed, ...**

## Contains

- FHEM
- homebridge
- mariadb
- NodeRed

## Requirements

- Docker
- Docker-Compose

## Install

```
blabla
```

## Defaults / Ports

- FHEM: http://[ip]:8083/fhem
- Node-Red: http://[ip]:1880/

## Passwords

- fhem-User: admin
- fhem-Password: 1LOg2810AGBLmT2fn
- telnet: ggOCu3IAKbN0x54zN

- mySQL-User: fhemuser
- mySQL-Password: (see mysql/init.sql and fhem/core/contrib/configDB/configDB.conf)

## Additional Information

- FHEM
    - HTTPS is not configured right now
