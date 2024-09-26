# Kali Linux in Docker accessible via web browser

1. Install Docker

2. Open terminal and run the following command
```
docker run -d --name=kali-linux --security-opt seccomp=unconfined -e PGID=1000 -e TZ=Etc/GMT -e SUBFOLDER=/ -e TITLE="Kali Linux " -p 3011:3000 -p 3009:3001 --shm-size="1gb" --restart unless-stopped linuxserver/kalilinux:latest
```
3. Open your web browser and visit
```
localhost:3011
```

   If deployed successfully you should see the GUI for Kali running inside your browser.
