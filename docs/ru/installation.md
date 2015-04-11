Установка
=========

Клонировать git репозиторий или использовать Composer:
<pre><code>$ git clone https://github.com/artemsk/veer.git ./  
<span class="com">// или</span>  
$ composer create-project artemsk/veer ./  
</code></pre>

Если Composer нет, установить его так `$ php -r "readfile('https://getcomposer.org/installer');" | php`

Поставить все зависимости и дополнительные пакеты: 
```
$ composer update
```

Копировать и переименовать конфигурационный файл — *.env.example* или *.env*. В нем настроить параметры базы данных (остальные параметры по желанию):  
<pre><code><span class="kwd">DB_HOST=</span><span class="str">localhost or url</span> 
<span class="kwd">DB_DATABASE=</span><span class="str">название бд</span> 
<span class="kwd">DB_USERNAME=</span><span class="str">имя пользователя бд</span> 
<span class="kwd">DB_PASSWORD=</span><span class="str">пароль бд</span> 
</code></pre>

Настроить разрешения на запись для следующих папок: **storage**, **vendor**.

Закэшировать конфигурацию и маршруты:
```
$ php artisan config:cache  
$ php artisan route:cache  
```

Настроить основной url и запустить миграцию базы данных. *В ходе настройки необходимо будет создать логин и пароль администратора.*
<pre><code>$ php artisan veer:install <span class="str">&lt;url&gt;</span> --migrate
</code></pre>