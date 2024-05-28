## Радио на Raspberry Pi:

- Установи mpg123 на Raspberry Pi:
```bash
sudo apt-get update
sudo apt-get install mpg123
```
- Создай скрипт для проигрывания радио. Например, создадим файл play_radio.sh:

```bash
nano play_radio.sh
```
- Вставь следующий код в файл play_radio.sh:

```bash
#!/bin/bash
#mpg123 http://prmstrm.1.fm:8000/ajazz &
mpg123 http://prmstrm.1.fm:8000/x &

```

- Сделай скрипт исполняемым:

```bash
chmod +x play_radio.sh
```

- Теперь можешь запускать скрипт:

```bash
./play_radio.sh
```

Этот скрипт будет использовать mpg123 для подключения и проигрывания потока интернет-радио с указанного URL.

Если хочешь, чтобы радио автоматически начинало проигрываться при запуске Raspberry Pi, можно добавить запуск этого скрипта в файл автозагрузки:

- Открой файл rc.local для редактирования:

```bash
sudo nano /etc/rc.local
```

- Добавь строку перед exit 0:

```bash
/home/pi/play_radio.sh &
```
- Сохрани изменения и выйди из редактора.

### Список радиостанций
```
https://espradio.ru/stream_list/
```