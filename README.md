# Socks5-SSH
Very simple and quick Socks5 proxy via SSH tunnel 

# Instruction 
Dynamic port forwarding allows you to create a socket on the local (ssh client) machine, which acts as a SOCKS proxy server. When a client connects to this port, the connection is forwarded to the remote (ssh server) machine, which is then forwarded to a dynamic port on the destination machine.

This way, all the applications using the SOCKS proxy will connect to the SSH server, and the server will forward all the traffic to its actual destination. To make your localhost device a Socks5 proxy server which forward all network traffic to a remote server simply run:

```
ssh -D localport user@remote_ip
```

In addition you can use `-N` and `-f` switches for no-shell and background execution with `ssh` command.
