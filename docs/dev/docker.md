## Docker
[公式ページ](https://docs.docker.com/install/linux/docker-ce/ubuntu/)

### uninstall old version

```
$ sudo apt remove docker docker-engine docker.io containerd runc
```

### install Docker Engine
#### set up the repository

```
$ sudo apt update
$ sudo apt install apt-transport-https ca-certificates curl gnupg-agent software-properties-common

$ curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -
$ sudo apt-key fingerprint 0EBFCD88
$ sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable"
```

#### install docker engine - community

```
$ sudo apt update
$ sudo apt install docker-ce docker-ce-cli containerd.io
```

### uninstall docker engine - community

```
$ sudo apt purge docker-ce
$ sudo rm -rf /var/lib/docker
```

## docker-compose
[公式ページ](https://docs.docker.com/compose/install/)
```
$ pip3 install docker-compose
```

## GPU Docker
  - [NVIDIA Docker って今どうなってるの？ (19.11版)](https://qiita.com/ksasaki/items/b20a785e1a0f610efa08)