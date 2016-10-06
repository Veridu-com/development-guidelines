# Installing PHPBrew:
- Install [PHPBrew requirements](https://github.com/phpbrew/phpbrew/wiki/Requirement) for your OS
- Install PHPBrew
```
curl -L -O https://github.com/phpbrew/phpbrew/raw/master/phpbrew
chmod +x phpbrew
§``
- Move phpbrew to somewhere can be found by your $PATH
```
sudo mv phpbrew /usr/bin/phpbrew
```

# Compiling PHP 7 with XDebug
## General
```
phpbrew install --name 7.0.11 7.0.11 +default +pdo +pgsql +mbstring +openssl +gmp +opcache
phpbrew install --name 7.0.11-zts 7.0.11 +default +pdo +pgsql +mbstring +openssl +gmp +opcache +zts
```

## Fedora (the correct OS)
```
phpbrew install --name 7.0.11 7.0.11 +default +pdo +pgsql +mbstring +openssl +gmp +opcache \-- --with-libdir=/lib64
phpbrew install --name 7.0.11-zts 7.0.11 +default +pdo +pgsql +mbstring +openssl +gmp +opcache +zts \-- --with-libdir=/lib64
```

## Mac OS (the not-so-correct-but-fine OS)
```
phpbrew install --name 7.0.11 7.0.11 +default +pdo +pgsql +mbstring +openssl=/usr/local/Cellar/openssl/1.0.2j/ +gmp +opcache
phpbrew install --name 7.0.11-zts 7.0.11 +default +pdo +pgsql +mbstring +openssl=/usr/local/Cellar/openssl/1.0.2j/ +gmp +opcache +zts
```

# Installing PHP 7 Extensions
```
phpbrew use 7.0.11
phpbrew extension install iconv
phpbrew extension install mongodb
phpbrew extension install github:wcgallego/pecl-gearman gearman-2.0.1
phpbrew extension install xdebug

phpbrew use 7.0.11-zts
phpbrew extension install iconv
phpbrew extension install mongodb
phpbrew extension install github:wcgallego/pecl-gearman gearman-2.0.1
phpbrew extension install xdebug
phpbrew extension install pthreads
```

# Compiling PHP 5 with XDebug
## General
```
phpbrew install --name 5.6.26 5.6.26 +default +pdo +pgsql +mbstring +openssl +gmp +opcache
phpbrew install --name 5.6.26-zts 5.6.26 +default +pdo +pgsql +mbstring +openssl +gmp +opcache +zts
```

## Fedora (the correct OS)
```
phpbrew install --name 5.6.26 5.6.26 +default +pdo +pgsql +mbstring +openssl +gmp +opcache \-- --with-libdir=/lib64
phpbrew install --name 5.6.26-zts 5.6.26 +default +pdo +pgsql +mbstring +openssl +gmp +opcache +zts \-- --with-libdir=/lib64
```

## Mac OS (the not-so-correct-but-fine OS)
```
phpbrew install --name 5.6.26 5.6.26 +default +pdo +pgsql +mbstring +openssl=/usr/local/Cellar/openssl/1.0.2j/ +gmp +opcache
phpbrew install --name 5.6.26-zts 5.6.26 +default +pdo +pgsql +mbstring +openssl=/usr/local/Cellar/openssl/1.0.2j/ +gmp +opcache +zts
```

# Installing PHP 5 Extensions
```
phpbrew use 5.6.26
phpbrew extension install iconv
phpbrew extension install mongodb
phpbrew extension install gearman
phpbrew extension install xdebug

phpbrew use 5.6.26-zts
phpbrew extension install iconv
phpbrew extension install mongodb
phpbrew extension install gearman
phpbrew extension install xdebug
phpbrew extension install pthreads
```

# Configuring XDebug for Remote Debugging
- Edit your xdebug.ini (usually located in ~/.phpbrew/php/<php-version>/var/db/xdebug.ini) and add:
```
xdebug.remote_enable=1
xdebug.remote_port=9000
xdebug.remote_host="localhost"
xdebug.remote_autostart=1
xdebug.profiler_enable=1
xdebug.profiler_output_dir="\tmp"
xdebug.remote_mode=req
xdebug.remote_connect_back=1
xdebug.max_nesting_level=200
xdebug.var_display_max_depth=1000
xdebug.var_display_max_children=256
xdebug.var_display_max_data=4096
request_terminate_timeout=600s

; Uncomment this line if you are using PHPStorm
; xdebug.idekey="PHPSTORM"
```
