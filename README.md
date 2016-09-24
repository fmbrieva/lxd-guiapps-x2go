# lxd-guiapps-x2go
Running **GUI applications** inside a **LXD containe**r.

This is an easy way to run graphical apps from within LXD container via x2go.

## Installation

- Download LXD container image pokemon_YYYYMMDD.tar.gz
  (Ex: pokemon_20160924.tar.gz)
- Import LXD image in your Linux Container Hypervisor LXD
  (Ex: lxc image import pokemon_20160924.tar.gz --alias pokemon-20160924)
- Check your images list 
  (Ex. lxc image list
+-------------------+--------------+--------+---------------------------------------------+--------+----------+-------------------------------+

|       ALIAS       | FINGERPRINT  | PUBLIC |                DESCRIPCIÓN                 |  ARQ   | TAMAÑO  |          UPLOAD DATE          |

+-------------------+--------------+--------+---------------------------------------------+--------+----------+-------------------------------+

| pokemon-20160924  | c71daeb7f548 | no     | Ubuntu 16.04 LTS server (20160922)          | x86_64 | 593.93MB | Sep 24, 2016 at 1:05pm (UTC)  |

+-------------------+--------------+--------+---------------------------------------------+--------+----------+-------------------------------+

- Create a container
  lxc launch pokemon-20160924 pokemon
- List your containers
 lxc list
+-----------+---------+----------------------+------+------------+-----------+

|  NOMBRE   | ESTADO  |         IPV4         | IPV6 |    TIPO    | SNAPSHOTS |

+-----------+---------+----------------------+------+------------+-----------+

| pokemon   | RUNNING | 10.197.26.201 (eth0) |      | PERSISTENT | 0         |

+-----------+---------+----------------------+------+------------+-----------+

- Install x2goclient
In Ubuntu: apt install x2goclient



(More details about installation at [Extension:Grafana#installation](https://www.mediawiki.org/wiki/Extension:Grafana#Installation))
  
## Screenshot (Mediawiki + Grafana extension)
![](https://upload.wikimedia.org/wikipedia/mediawiki/7/7b/Grafana_Screenshot.png)

## Credits
- LXD http://www.ubuntu.com/cloud/lxd
- X2go http://wiki.x2go.org/doku.php/start

