>> README.md — What this CTF is & how to run (give this to the organizer)
---
### What is this CTF?

+ SSTI1 is a small teaching-style challenge that demonstrates a Server-Side Template Injection (SSTI)
vulnerability in a toy searchbox application using Jinja. Players can submit template expressions 
in the search box; the server intentionally evaluates them (VULN mode) so players can practice 
SSTI exploitation techniques to execute commands and read files.

### Short hint for players (show on the challenge page)

+ The blob you retrieve is encoded and requires multiple transforms (a sequence of decodes) to
reveal the final CTF_flag{...} string.

--- 
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
