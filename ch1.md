# Глава 1 - git config
Привет! 
Это небольшой, но полезный для начинающих практический туториал по использованию git команд и github. 
Постарайтесь выполнять все задания, чтобы познакомиться с полезным инструментом по контролю версий. 
    
Т.к. этот туториал рассчитан на начинающих, то команды будут рассмотрены поверхностно. Вам понадобится 
терминал (или командную строчку для Windows), IDE и немного кода. В данном туториале я буду приводить примеры на python + PyCharm 
(или любой другой продукт Idea). 

Откройте терминал. Первым делом посмотрите где вы сейчас находитесь. Например, для Windows это может быть так:

```C:\user\your_name> ```

Первым делом, давайте узнаем, как зовут пользователя и его e-mail для работы с git. 
```
git config --global --list
```
И найдите две строчки `user.name` и `user.email`. Эта информация необходима для работы с git, чтобы сохранить 
и сказать кто сделал новые правки в код. Если вы ещё не забыли, то мы работаем с системой контроля версий.

Чтобы установить имя и e-mail пользователя, нужно написать:
```
git config --global user.name "имя_пользователя"
git config --global user.name "e-mail"
```
И да-да, обязательно в кавычках. 

После установки вызовите команду, которая получает все настройки и посмотрите, применились изменения или нет:
```
git config --global --list
```

Самые внимательные могли заметить хитрый ключ `--global`. Этот ключ указывает git, что мы хотим сделать глобальные 
настройки, т.е. "для всех". Но что делать, если у нас несколько репозиториев и в каждом из них нужно отправлять 
данные под разными именами или e-mail? Можно использовать локальные настройки! 

Для того чтобы вызвать локальные настройки, нужно просто убрать ключ `--global`. Но есть важный момент: необходимо
вызывать команды для установки или проверки строго в корневой папке будущего/текущего репозитория, т.е. 
туда куда собираетесь клонировать или уже клонировали git репозиторий. 
