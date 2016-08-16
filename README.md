# certbot_renew
Basic script to automate certificate update from certbot.

Use a cron job to run this once a month
```
# m h  dom mon dow   command                                                                                        
00 3 1 * * /root/bin/certbot_renew > /tmp/certbot_renew.log 2>&1 
```

If using systemd timers:

Copy the service and timer files into the `/etc/systemd/system` directory and enable the service.
```
# cp systemd/* /etc/systemd/system

# systemctl enable letsencrypt.timer
# systemctl start letsencrypt.timer

```
