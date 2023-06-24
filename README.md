# php-install
Useful scripts for setting up a PHP environment.

- [Install any version of PHP](#install-any-version-of-php)
- [Switch between PHP versions](#switch-between-php-versions)
- [Install composer](#install-composer)

## Initialization

In order to use some scripts, some tools and PPA need to be installed first.

Run:
```bash
bash phpprepare
```

This will also make `phpinstall` and `phpversion` globally available on your computer.

```console
$> bash phpprepare
STEP Updating system and installing needed programs
[...]
OK
STEP Adding PHP Personal Package Archive
[...]
OK
STEP Updating apt after adding PPA
[...]
OK
STEP Placing phpinstall in /usr/local/bin/
OK
STEP Placing phpversion in /usr/local/bin/
OK

DONE Your system is ready for PHP !
Available versions :
7.4
5.6
7.0
7.1
7.2
7.3
8.0
8.1
8.2

To install any PHP version, run phpinstall
$>
```

## Install any version of PHP

Run:
```bash
phpinstall
```
The script will ask you which version you want to install.
**Note: you can install as many PHP versions as you want.**

```console
$> phpinstall
STEP Updating system
[...]
OK

Installable PHP versions :
7.4
5.6
7.0
7.1
7.2
7.3
8.0
8.1
8.2

Which one do you want ? 7.4 <= user input
STEP Installing PHP7.4
[...]
OK

SUCCESS PHP 7.4 has been installed
Run phpversion to switch your active PHP version
$>
```

## Switch between PHP versions

Run:
```bash
phpversion
```
The script will ask you which version you want to switch to.

```console
$> phpversion
Current PHP version : 8.2.7

Available versions :
7.4
8.1
8.2

Target version : 8.1 <= user input

Current PHP version : 8.1.20
$>
```

Alternatively, you can tell which version you want to use:
```bash
phpversion 8.2
```

```console
$> phpversion 8.1
Current PHP version : 8.2.7
Target version : 8.1
Current PHP version : 8.1.20
$>
```

## Install composer

Run:
```bash
bash composerinstall
```

```console
$> bash composerinstall
Downloading composer.phar
Installer verified
Install completed
$>
```

To make sure composer is correctly installed, run:
```bash
composer --version
```
