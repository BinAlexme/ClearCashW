# ClearCashW

### Для автоматизации чистка от используемой памяти в роутере

1. Вести команду в роутере 
```
	cd /sbin && wget https://raw.githubusercontent.com/BinAlexme/ClearCashW/refs/heads/master/MemWCashes.sh
```
3. дылача прав на службу
```
	chmod +x /sbin/MemWCashes.sh
```
4. В панели управлени System/Scheduled Tasks вести значени минуты часы *** и действие. к примеру: reboot
```
 	40 18 * * * /sbin/MemWCashes.sh
```
5. Перезагрузить м запустить cron:
```
	service cron restart
 	service cron start
```

### Вручную для сброса кеша
```
	sync && echo 3 > /proc/sys/vm/drop_caches
```
