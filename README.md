Virtualhost Manage Script
===========

Bash Script to allow create or delete apache/nginx virtual hosts on Ubuntu on a quick way using by new version rimauwaf panel.

## Installation ##

1. Download the script
2. Apply permission to execute:

```
$ chmod +x /path/to/rimauwaf-cli.sh
```

3. Optional: if you want to use the script globally, then you need to copy the file to your /usr/local/bin directory, is better
if you copy it without the .sh extension:

```bash
$ sudo cp /path/to/rimauwaf-cli.sh /usr/local/bin/rimauwaf-cli
```

### For Global Shortcut ###

```bash
$ cd /usr/local/bin
$ wget -O rimauwaf-cli https://raw.githubusercontent.com/asklinux/virtualhost/master/rimauwaf-cli.sh
$ chmod +x rimauwaf-cli
$ wget -O rimauwaf-cli https://raw.githubusercontent.com/RoverWire/virtualhost/master/rimauwaf-cli-nginx.sh
$ chmod +x rimauwaf-cli
```

## Usage ##

Basic command line syntax:

```bash
$ sudo sh /path/to/rimauwaf-cli.sh [create | delete] [domain] [optional host_dir] [on | off]
```

With script installed on /usr/local/bin

```bash
$ sudo rimauwaf-cli [create | delete] [domain] [optional host_dir] [on | off]
```

### Examples ###

to create a new virtual host:

```bash
$ sudo rimauwaf-cli create mysite.dev
```
to create a new virtual host with custom directory name:

```bash
$ sudo rimauwaf-cli create anothersite.dev my_dir on
```
to delete a virtual host

```bash
$ sudo rimauwaf-cli delete mysite.dev
```

to delete a virtual host with custom directory name:

```
$ sudo rimauwaf-cli delete anothersite.dev my_dir
```
### Localization

For Apache:

```bash
$ sudo cp /path/to/locale/<language>/virtualhost.mo /usr/share/locale/<language>/LC_MESSAGES/
```

For NGINX:

```bash
$ sudo cp /path/to/locale/<language>/virtualhost-nginx.mo /usr/share/locale/<language>/LC_MESSAGES/
```
