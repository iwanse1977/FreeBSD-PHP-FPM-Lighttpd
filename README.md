# FreeBSD PHP-FPM Lighttpd mod FastCGI
PHP-FPM is a FastCGI implementation for PHP that improves the performance and scalability of PHP web applications. In this article we will review in more depth what PHP-FPM is and how to install Lighttpd on a FreeBSD server with PHP support (via PHP-FPM).

PHP-FPM is an abbreviation for PHP FastCGI Process Manager, which is a process manager for running PHP applications via the FastCGI protocol. PHP-FPM can help improve the performance of PHP applications by running the PHP process as a separate daemon from the web server. In a standard configuration, PHP-FPM manages PHP processes separately from a web server such as Lighttpd or Nginx, allowing more flexibility in managing PHP processes and increasing application scalability.

PHP-FPM has several features, such as better process management, better process isolation, better resource management, the ability to limit the number of connections, and support for enabling PHP opcode caching. PHP-FPM also allows administrators to manage PHP applications more easily, including monitoring PHP processes and stopping problematic PHP processes.

## System specifications

OS: FreeBSD 13.2 Stable

Hostname: ns5

IP Address: 192.168.5.2

Domain: datainchi.com

Lighttpd version: lighttpd/1.4.67 (ssl) - a light and fast webserver
PHP version: PHP62
mod PHP

### Installation
The way to install PHP-FPM on FreeBSD is almost the same as other PHP mods. What's different is that PHP-FPM has a special configuration file located at "/usr/local/etc/php-fpm.d". Follow the guide below to install PHP-FPM.

Before we start the process of installing Lighttpd, you first install the Lighttpd dependencies, namely "Build dependencies" and "Library dependencies". Here's how to install these dependencies.
``` bash
root@ns5:~ # cd /usr/ports/lang/php82
root@ns5:/usr/ports/lang/php82 # make install clean
root@ns5:/usr/ports/lang/php82 # cd /usr/ports/www/mod_php82
root@ns5:/usr/ports/www/mod_php82 # make install clean
root@ns5:/usr/ports/www/mod_php82 # cd /usr/ports/databases/php82-mysqli
root@ns5:/usr/ports/databases/php82-mysqli # make install clean
```

## Support
https://www.unixwinbsd.site/2024/01/setup-lighttpd-with-php-fpm-mod-fastcgi.html
