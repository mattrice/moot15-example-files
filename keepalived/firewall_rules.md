### example of allowing keepalived to communicate on Ubuntu's UFW (Uncomplicated FireWall)

#### on both haproxy nodes
ufw default deny
ufw allow ssh
ufw allow http
ufw allow https
ufw enable

#### on haproxy_a
```
ufw allow in from 198.51.100.21 to 224.0.0.18
```

#### on haproxy_b
```
ufw allow in from 198.51.100.20 to 224.0.0.18
```