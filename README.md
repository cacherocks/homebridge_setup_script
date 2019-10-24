# Homebridge setup script

Итак, что же делает этот скрипт?

* Ставит `libavahi-compat-libdnssd-dev`
* Через npm ставит `homebridge`
* Создает папку `.homebridge` в домашнем каталоге текущего пользователя
* Кладет туда файл конфигурации с данными для запуска веб-интерфейса
* Ставит сам плагин веб-морды - `homebridge-config-ui-x`
* Создает `homebridge.service` и запускает его
* Создает отдельный `homebridge-config-ui-x.service` и запускает его

Если вам необходимо установить Homebridge без установки/замены/обновления NodeJS, то этот скрипт вам отлично подойдет.

# Как ставить

`sudo apt install git`

`git clone https://github.com/cacherocks/homebridge_setup_script`

`cd homebridge_setup_script`

`bash install.sh`

Теперь даже при перезагрузке homebridge с кривым конфигом, Вы сможете восстановить его работоспособность используя веб-интерфейс.

Процесс установки займет минут 10 на 3й малине и меньше 2 минут на 4й малине с быстрой флешкой, в итоге Вы получите работоспособный homebridge и его веб-морду на порту `8080`.
