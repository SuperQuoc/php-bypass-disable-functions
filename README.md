# php-bypass-disable-functions
Demo project how to bypass the disable_functions security control of PHP on Linux, where processes can inspect and even write their own memory via the special /proc/self/map file via standard file operations (open/seek/read/write).

Tested on PHP 7.3.5, x86_64 Linux

See also: https://seclists.org/bugtraq/2019/May/52

## how to use

```
regularuser@7981d86dd9aa:/$ ./php-7.3.5-vanilla/sapi/cli/php -d 'disable_functions=system' disfunpoc.php

Warning: system() has been disabled for security reasons in /repo-shared/disabled_functions/disfunpoc.php on line 2
uid=1000(regularuser) gid=1000(regularuser) groups=1000(regularuser)

```
