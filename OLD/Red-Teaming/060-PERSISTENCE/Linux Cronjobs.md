You can use Cronjobs for autoruns, though, they may not always work.

```bash
# Manually add crontab
# Open Crontab Editor
crontab -e

# Paste this in to run scoring.sh every min
* * * * * /dev/shm/scoring.sh

# All in one line, add to end of crontab, root user
(sudo crontab -l; echo "* * * * * /path/to/script.sh") | sudo crontab -u root -
```