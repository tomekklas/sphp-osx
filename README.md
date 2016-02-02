# PHP version switcher for OSX
##### forked from https://github.com/conradkleinespel/sphp-osx and ported to Nginx

If you're on OSX with PHP installed via Brew, you may be looking for an easy way to switch between PHP versions (5.3, 5.4, 5.5, 5.6, etc). Well, this package is it.

Installation:
```
git clone git@github.com:tomekklas/sphp-osx.git
```

Add `/usr/local/bin` to your `$PATH`. If you use the Bash shell, you can do this by running this command:
```
echo 'export PATH="/usr/local/bin:$PATH"' >> $HOME/.bashrc
```
then run
```
source .bashrc
```

Usage:
```
sphp 54
sphp 55
sphp 56
sphp 70
```

## Troubleshooting

### PHP doesn't work anymore when I switch versions in Bash

Bash has an executable path cache. It saves the paths of executables it has previously run. If Brew changes the path to the `php` executable, you may encounter
this error. You have 2 options:
- Add `set +h` in your `~/.bashrc` or `~/.profile` file. This will disable the executable path cache in Bash. However, this might slow down your Bash.
- After you use `sphp`, enter the command `hash -r` in your shell. This will clear the executable path cache only once.

## Contributors

* [@alefi87](https://github.com/alefi87)
* [@conradkleinespel](https://github.com/conradkleinespel)
* [@michaelburtonray](https://github.com/michaelburtonray)
* [@sebastienbarre](https://github.com/sebastienbarre)
* [@uzyn](https://github.com/uzyn)
* [@w00fz](https://github.com/w00fz)
