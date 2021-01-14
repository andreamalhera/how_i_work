# First day steps
* Set disk password 
* Set user OS password
* Get internet connection (if you haven't)
* Install chrome
* Get access to documentation and books
* Get access to email
    * Import colleague's calenders
    * Enter workdays
* Install tools
* Get access to internal servers per ssh:
    `ssh <username>@<machine>.<domain.com>`
    * Set ssh keys, so you don't have to enter the psw every time:
         * create new ssh-key: `ssh-keygen`
         * save ssh-key to server: `ssh-copy-id -i ~/.ssh/id_rsa.pub <username>@<machine>.<domain.com>`
* Connect to Visualizers:
    * `ssh -L 8082:localhost:8082 <username>@<machine>.<domain.com>`
    * open `http://localhost:8082`
