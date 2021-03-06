# gcm
**NOTE: I am not the original author**

fork of Gnome-Connection-Manager

based on version 1.1

Get the original version here:
http://kuthulu.com/gcm

## New
 - changed to use pyaes
 - added menu items for scp strings (from https://github.com/yma-het/GnomeConnectionManager)
 - empty passwords are not saved to config
 - can specify config directory through the command line (-c option)

# REQUIREMENTS:
 * python 2.6 or later
 * python-gtk2 
 * expect
 * python-vte
 * libglade2
 * python-glade2
 * pyaes
 * python-gettext

# INSTALLATION:
## Linux/Unix:

copy the gcm files wherever you want, then execute `gnome_connection_manager.py`

example:
```
/home/someuser/gcm/gnome_connection_manager.py
```

## FreeBSD:
Edit the file gnome_connection_manager.py and use the full path of the "ssh" and "telnet" binaries in the lines:
```
SSH_BIN = 'ssh'
TEL_BIN = 'telnet'
```
Edit the file ssh.expect and replace the first line with the full path of the "expect" command:
```
#!/usr/bin/expect
```

# LANGUAGE:
to force a language start the application with this command:
```
LANGUAGE=en /home/someuser/gcm/gnome_connection_manager.py
```

if that doesn't work, try with:
```
env LANGUAGE=en python /home/someuser/gcm/gnome_connection_manager.py
```

