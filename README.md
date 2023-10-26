# backup
# ЗАДАНИЕ 1
Команда:
```YAML
rsync -ac --delete --exclude=".*/" . /tmp/backup
```

# ЗАДАНИЕ 2
Скрипт ( --delete для полностью зеркальной копии )
```YAML
rsync -a --delete /root /tmp/backup

if [ "$?" -eq 0 ]; then
        logger "Backup successfully"
else    logger "Backup failed"
fi
```
Далее вызвал crontab -e и указал планирование на ежедневный вызов скрипта копирования
