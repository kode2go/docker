# Docker

# Setup - Win 10 - WSL - Ubuntu

Reference:

https://docs.docker.com/engine/install/ubuntu/

1. Install Ubuntu in MS Store

2. Make WSL 2 is Running

```
wsl.exe --list --verbose
wsl.exe --set-version Ubuntu-22.04 2
```

# Ubuntu (WSL)

```
# Add Docker's official GPG key:
sudo apt-get update
sudo apt-get install ca-certificates curl
sudo install -m 0755 -d /etc/apt/keyrings
sudo curl -fsSL https://download.docker.com/linux/ubuntu/gpg -o /etc/apt/keyrings/docker.asc
sudo chmod a+r /etc/apt/keyrings/docker.asc

# Add the repository to Apt sources:
echo \
  "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.asc] https://download.docker.com/linux/ubuntu \
  $(. /etc/os-release && echo "$VERSION_CODENAME") stable" | \
  sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
sudo apt-get update
```

```
sudo apt-get install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin
```

```
sudo docker run hello-world
```

## Debug

I had an issue with `sudo curl...` I thought it was broken, but it wasnt - said "not a link". Should have just completed the installation as it all worked.

# Key Commands

```
sudo service docker start
```

```
sudo docker run hello-world
```

```
sudo docker images
```

```
sudo docker ps
```

Remove: 

```
sudo docker rim <IMAGE ID>
```
