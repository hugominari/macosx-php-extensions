# Installing extension for PHP on macOSX

First u need to install Autoconf using Homebrew or other way.

```bash
brew install autoconf
```

Now, you have to build the extension from the PHP source code, and can be downloaded at:

``` bash
[http://php.net/get/php-7.4.2.tar.bz2/from/a/mirror](http://php.net/get/php-7.4.2.tar.bz2/from/a/mirror)

Note: Change the 7.4.2 to your PHP version.
To check the PHP version u can run:

which php
```

Unpack file downloaded and follow this steps: (Im using MAMP, then...)
``` bash
$ cd php-7.4.2/ext/name-of-extension-u-need
$ /Applications/MAMP/bin/php/php7.4.2/bin/phpize
$ ./configure --with-php-config=/Applications/MAMP/bin/php/php7.4.2/bin/php-config
$ make && make install
```

Add the extension builded into your `php.ini` in `/Applications/MAMP/bin/php/php7.4.2/conf` and restart MAMP.

```bash
extension=name-of-extension-u-need.so
```

Done...

Run this command `php -m` and locate the extension installed or just check for the extension `php -m | grep -i name-of-extension-u-need`.