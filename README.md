# Zapret (обход блокировки Discord'а и Youtube'а) - REPACK OF [THIS REPOSITORY](https://github.com/Flowseal/zapret-discord-youtube) ALL CREDITS TO [Flowseal](https://github.com/Flowseal)

## Guide

Запустите **от имени администратора** то, что вам нужно:

- **`discord.bat`** - запустить обход дискорда
- **`discord_youtube.bat`** - запустить обход дискорда и ютуба
- **`discord_youtube_secondary.bat`** - запустить обход дискорда и ютуба (если не работает первый, лучше работает на МГТС)
##
- **`service_discord.bat`** - запустить обход дискорда и поставить на автозапуск (в сервисах)
- **`service_discord_secondary.bat`** - запустить обход дискорда и поставить на автозапуск (в сервисах | если не работает первый, лучше работает на МГТС)
- **`service_discord_youtube.bat`** - запустить обход дискорда и ютуба и поставить на автозапуск (в сервисах)
- **`service_discord_youtube_secondary.bat`** - запустить обход дискорда и ютуба и поставить на автозапуск (в сервисах | если не работает первый, лучше работает на МГТС)
##
- **`service_goodbye_discord.bat`** - запустить, если вы используете **СЕРВИС goodbyedpi**, и хотите, чтобы zapret обходил **только discord**. ВНИМАНИЕ: Запускать ПОСЛЕ создания сервиса goodbyedpi. Первый раз goodbyedpi может вылететь - просто перезапустите устройство! (Работает плохо
##
- **`service_remove.bat`** - остановить и удалить сервисы выше

## Не работает?
- Проверьте, запускаете ли вы файлы от имени администратора
- Не работает сервис? Проверьте, чтобы в пути до файла **не было пробелов** и русских символов. Также отключите программы, которые могут мешать созданию сервиса *(Антивирусы, клинеры с доп. защитой)*
- Не работает вместе с VPN? Отключите функцию **TUN** (Tunneling) в настройках VPN
- Не работает `service_goodbye_discord`? Удостовертесь, что сервис goodbyedpi запущен и имеет название GoodbyeDPI. После снова запустите `service_goodbye_discord.bat` и перезапустите устройство
- Не прогружается видео на ютубе? Попробуйте поставить **`Kyber`** и **`QUIC`** в default (`chrome://flags/`). Также в файле, который открываете, в строчке с `--filter-tcp=443`: попробуйте поменять `--dpi-desync-fooling=md5sig` на `--dpi-desync-fooling=badseq` (https://github.com/Flowseal/zapret-discord-youtube/issues/46)
- Попробуйте обновить бинарники с оригинального репозитория (https://github.com/Flowseal/zapret-discord-youtube)
##
- Не работает **YouTube**? Попробуйте найти ответ здесь - https://github.com/Flowseal/zapret-discord-youtube/issues/90
- Не работает **Discord**? Попробуйте найти ответ здесь - https://github.com/Flowseal/zapret-discord-youtube/issues/92

### Хочу удалить, но остался файл WinDivert?
Для удаления оставшегося драйвера WinDivert, откройте cmd от имени администратора и пропишите следующее:
```
sc stop WinDivert
sc delete WinDivert
```

Возможно, драйвер у вас будет записан по-другому. Для уточнения названия пропишите `driverquery | find "Divert"` в cmd.

### Дополнительные адреса заблокированных сайтов можно добавить в список list-general.txt (для `*discord_youtube`) и в список list-discord (для файлов без `youtube` в названии). После добавления сервис нужно перезапустить

### Оригинальный репозиторий
Credits to https://github.com/bol-van/zapret/tree/master/binaries/win64/zapret-winws and https://github.com/Flowseal/zapret-discord-youtube
