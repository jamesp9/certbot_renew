# certbot_renew
Basic script to automate certificate update from certbot.

Use a cron job to run this once a month
```
# m h  dom mon dow   command                                                                                        
00 3 1 * * /root/bin/certbot_renew > /tmp/certbot_renew.log 2>&1 
```
