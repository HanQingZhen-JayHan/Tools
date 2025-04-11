```
## GIT

Q: fatal: unable to access 'https://github.com/xxxx.git': Failed to connect to github.com port 443 after 2222 ms: Timed out
A: git config --global http.proxy http://acdount:pwd@proxy.xxx.com:8080
   git config --global https.proxy http://account:pwd@proxy.xxx.com:8080
   Tip: @ = %40

Q: Error: Received HTTP code 504 from proxy after CONNECT
   (sometimes previous proxy settings makes this kind of problem)
A: git config --global --unset http.proxy
   git config --global --unset https.proxy
   
   git config --global http.proxy ''
   git config --global https.proxy ''

Q: Error: SSL certificate problem: unable to get local issuer certificate
A: git config --global http.sslbackend schannel

## Proxy
Q: windwos system
A: set http_proxy=http://account:pwd@proxy.xxx.com:8080
   set https_proxy=http://account:pwd@proxy.xxx.com:8080

Q: PIP
A: pip install --proxy=http://account:pwd@proxy.xxx.com:8080 psycopg2

## Ubantu

Q: 'Username' is not in the sudoers file. This incident will be reported
A: 1. open file
   su root
   nano /etc/sudoers
   2. add the user below admin user like below syntax
   user_name ALL=(ALL) ALL
```
