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
