# Installation from release webpage for ubuntu
* look for binary
* `wget http://<webpage-path-to-package>.tar.gz`
* `tar -xzvf <>.tar.gz`

# How to connect to internal pages through a proxy
* ssh to a internal machine that supports proxy connection with `ssh -D <port> <username>@<machine>.<domain.com>` e.g port 10000
* Go to the settings of your browser
* Open for "proxy" settings
     * Enable socks-proxy
         * SOCKS Proxy Server is "localhost"
         * Port is <port> from above
* Visit internal pages on your browser
NOTE: Do not forget to exit the proxy when you are done. Also deactivating the socks-proxy on the browser.
