## DanielMueller1309pihole

### Beschreibung

### Funktioniert auf
- [x] Ubuntu (>=20.04)
### Variablen + Defaults
```yml
user_pihole: "pihole"
group_pihole: "pihole"
web_password: "{{ lookup('keepass', 'pihole_password_hash', 'password') }}"
ipv4_address_pihole: 192.168.178.15
fspath_web_interface: "/var/www/admin"
fspath_web_directory: "/var/www/pihole"
fspath_pihole: "/opt/pihole"
fspath_pihole_src: "/etc/.pihole"
fspath_pihole_config: "/etc/pihole"


extra_hosts:
  - hostname: "fritz"
    domain: "box"
    ip: "192.168.178.1"

network_interface: eth0
dns_servers:
  - "8.8.8.8"
  - "8.8.4.4"
dns_domain: home
dhcp_activ: true
dhcp_start: '192.168.178.20'
dhcp_end: '192.168.178.200'
dhcp_router: '192.168.178.1'
dhcp_leasetime: 24
dhcp_ipv6: false
```
