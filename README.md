# backup
# ЗАДАНИЕ 1
Команда:
```YAML
rsync -ac --delete --exclude=".*/" . /tmp/backup
```
![alt text](https://github.com/StepanovSA/backup/blob/main/26.10%20rsync1.PNG)
# ЗАДАНИЕ 2
Скрипт ( --delete для полностью зеркальной копии )
```YAML
#!/bin/bash
rsync -a --delete /root /tmp/backup

if [ "$?" -eq 0 ]; then
        logger "Backup successfully"
else    logger "Backup failed"
fi
```
Далее вызвал crontab -e и указал планирование на ежедневный вызов скрипта копирования
![alt text](https://github.com/StepanovSA/backup/blob/main/26.10%20rsync2%20crontab.PNG)
![alt text](https://github.com/StepanovSA/backup/blob/main/26.10%20rsync2%20script.PNG)
