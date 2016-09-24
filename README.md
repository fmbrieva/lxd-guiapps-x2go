# lxd-guiapps-x2go
Running *GUI applications* inside a ***LXD container***.

This is an easy way to run graphical apps ***GUI*** from within LXD container via ***x2go***.

## Installation

- Download tar file with [LXD container image](http://www.delegacionprovincial.com/mediawiki/upload_files/lxd_images/pokemon_20160924.tar.gz):

>Actual tar file: ***pokemon_20160924.tar.gz***

- Import *LXD image* in your *Linux Container Hypervisor LXD* 

>***lxc image import pokemon_20160924.tar.gz --alias pokemon-20160924***

- Check your images list 
 
>***lxc image list***

```
+-------------------+--------------+--------+---------------------------------------------+--------+----------+-------------------------------+
|       ALIAS       | FINGERPRINT  | PUBLIC |                DESCRIPCIÓN                 |  ARQ   | TAMAÑO  |          UPLOAD DATE          |
+-------------------+--------------+--------+---------------------------------------------+--------+----------+-------------------------------+
| pokemon-20160924  | c71daeb7f548 | no     | Ubuntu 16.04 LTS server (20160922)          | x86_64 | 593.93MB | Sep 24, 2016 at 1:05pm (UTC)  |
+-------------------+--------------+--------+---------------------------------------------+--------+----------+-------------------------------+
```

- Create a container

> ***lxc launch pokemon-20160924 pokemon***

- List your containers

> ***lxc list***
```
+-----------+---------+----------------------+------+------------+-----------+
|  NOMBRE   | ESTADO  |         IPV4         | IPV6 |    TIPO    | SNAPSHOTS |
+-----------+---------+----------------------+------+------------+-----------+
| pokemon   | RUNNING | 192.168.1.201 (eth0) |      | PERSISTENT | 0         |
+-----------+---------+----------------------+------+------------+-----------+
```

> ***Pokemon*** container has ip address *192.168.1.201*

- Install x2goclient in remote computer

>*In Ubuntu*: ***apt install x2goclient***

## Notes

LXD Container: ***pokemon***

User/Password: ***pikachu***/***pikachu***

## Usage

- Start ***x2goclient*** in remote computer and add a new session
- Enter user (***pikachu***) and password (***pikachu***)
- You have a GUI session in LXD container

>***x2goclient***
## Credits
- LXD http://www.ubuntu.com/cloud/lxd
- X2go http://wiki.x2go.org/doku.php/start

