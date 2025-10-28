>> How to run (organizer)
---
## 1) Build (if you received source + Dockerfile):
```
sudo docker build -t iranctf/ssti1:1.0 .
```
## 2) Run (mount a per-team flag file from the host into the container):
```
sudo docker run -d --rm --name ssti1_team1 -p 5001:5000 -v /srv/ctf/team1/flag:/home/ctfuser/flag:ro iranctf/ssti1:1.0
```
## 3) Remove container (stop + remove):
```
sudo docker rm -f ssti1_team1 2>/dev/null || true
```
