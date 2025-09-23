# Log server temperature

Log Temperatures to a file using a simple script and cron job.

Create a script at `/home/josep/scripts/log_temp.sh` (for instance):

```bash
#!/bin/bash

DATE=$(date)
TEMP=$(/usr/bin/sensors | /usr/bin/grep 'Package id 0:' | /usr/bin/awk '{print $4}')
echo "$DATE, $TEMP" >> /home/josep/scripts/cpu_temp.log
```

Make sure the file is executable:

```bash
chmod +x /home/josep/scripts/log_temp.sh
```

Add the cron job. The example bellow runs once every hour, at minute 0:

```bash
crontab -e
```

```
0 * * * * /home/josep/scripts/log_temp.sh
```
