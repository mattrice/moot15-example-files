# moot15-example-files
US Moodle Moot 2015

# Getting HAProxy logs out of the system log

By default, HAProxy logs to rsyslog. If you are interested in isolating the logs from HAProxy, you can do the following:

1. make a subdirectory to where HAProxy will log
```
mkdir -p /var/log/haproxy                   # Create the directory
chown -R syslog:adm /var/log/haproxy/       # Set up permissions
chmod -R g+s /var/log/haproxy/              # Ensure permissions propagate to sub-directories
```

2. modify rsyslog's configuration to isolate out the HAProxy log files
```
# Create/edit /etc/rsyslog.d/49-haproxy.conf
```

3. Restart the rsyslog service
```
service rsyslog restart
```