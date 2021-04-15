# copy a file to remote server

1. scp


# set up a webserver

[https://ubuntu.com/tutorials/install-and-configure-nginx#5-activating-virtual-host-and-testing-results]


# create password protected website

[https://docs.nginx.com/nginx/admin-guide/security-controls/configuring-http-basic-authentication/]

# create user

```
adduser --gecos "" --disabled-password fullsnaxdev
chpasswd <<<"fullsnaxdev:unsecure1"
```