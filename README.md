# CSE 135 HW 1

## Names
Cass Adefuin, Xavier Chua

## Apache Login
Droplet IP: 165.232.143.95
username: grader
password: YOUareAWESOME:)

## [Link to Website](https://timmyfanclub.site/)

## Auto Deploy Setup


## Site Login
username: grader
password: OscarPrince21@5

## Compression Changes
We found minor changes in our HTML files. For example, some lines in cassadefuin.html had additional quotation marks, and different line breaks than what was originally written.

## Removing Server Header
We followed the instructions on [tecmint.com](https://www.tecmint.com/change-apache-server-name-to-anything-in-server-headers/) to rename the server header.

First, we installed Apache mod_security module.
```
$ sudo apt install libapache2-mod-security2
$ sudo a2enmod security2
```

Then we added the following lines to `/etc/apache2/apache2.conf`
```
ServerTokens Full
SecServerSignature “Tecmint_Web”
```

Finally, we restarted the web server using `$ sudo systemctl restart apache2`