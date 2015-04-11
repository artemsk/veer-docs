Installation
=========

Clone git repository or use Composer:
<pre><code>$ git clone https://github.com/artemsk/veer.git ./  
<span class="com">// or</span>  
$ composer create-project artemsk/veer ./  
</code></pre>

If you don't have Composer install it with `$ php -r "readfile('https://getcomposer.org/installer');" | php`

Install all dependencies: 
```
$ composer update
```

Copy and rename main configuration file — *.env.example* to *.env*. Set database parameters in it (others are optional):
<pre><code><span class="kwd">DB_HOST=</span><span class="str">localhost or url</span> 
<span class="kwd">DB_DATABASE=</span><span class="str">database name</span> 
<span class="kwd">DB_USERNAME=</span><span class="str">database username</span> 
<span class="kwd">DB_PASSWORD=</span><span class="str">database password</span> 
</code></pre>

Set permissions for these folders: **storage**, **vendor**.

Cache configuration & routes:  
```
$ php artisan config:cache  
$ php artisan route:cache  
```

Set your initial url and migrate database. *You will be asked to set administrator login and password.*
<pre><code>$ php artisan veer:install <span class="str">&lt;url&gt;</span> --migrate
</code></pre>