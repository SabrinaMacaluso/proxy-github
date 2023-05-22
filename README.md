# proxy-github

nano .ssh/config and add:

```
Host github.com
    Hostname ssh.github.com
    ProxyCommand nc -X connect -x <IP-PROXY>:<PORT> %h %p
    Port 443
    ServerAliveInterval 20
    User git

```
