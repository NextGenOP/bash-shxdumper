# sh.x dumper for bash, version 1.0

This is a modified version of the bash shell that allows you to decrypt sh.x (shc compiled) scripts. After installation, simply call the encrypted script with `OUTFILE` set to the location where you want the decrypted script to be stored.

## The automatic and easy way

### Usage

#### Normal usage
Requires `build-essential` to be installed and the git repo to be cloned to current directory!

`sudo python3 ./run.py dump ./encrypted.sh.x ./decrypted.sh`

#### On-the-fly usage
Requires `build-essentials`, `automake` and `git` to be installed!

`sudo true && wget -q -O- https://github.com/NextGenOP/bash-shxdumper/raw/master/run.py | sudo python3 /dev/stdin dump ./encrypted.sh.x ./decrypted.sh`

## The manual but harder way

### Usage

### Compilation
`./configure`

`make -j$(nproc) || make`

### Installation
`sudo mv /bin/bash /bin/bash.bak && sudo cp ./bash /bin/bash`

### Run

`OUTFILE=./decrypted.sh ./encrypted.sh.x`

### Uninstallation
`sudo rm /bin/bash`

`sudo mv /bin/bash.bak /bin/bash`

`sudo chmod a+x /bin/bash`

## Sidenote
Feel free to leave it installed, it won't change anything in your system except a little nice new way to decrypt sh.x scripts!
(and a little outdated master branch bash version lol)
