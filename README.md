# Configure SSH for GitHub behind a proxy

Open the SSH configuration file located at ~.ssh/config. Add the following lines, replacing IP-PROXY and PORT with the proxy host address and port number:

```
Host github.com
    Hostname ssh.github.com
    ProxyCommand nc -X connect -x <IP-PROXY>:<PORT> %h %p
    Port 443
    ServerAliveInterval 20
    User git

```

