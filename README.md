ngx\_remote\_ip
===============

This module adds the possibility to respond to a certain URL simply with the remote IP address, e.g.:

    # curl http://ip.mydomain.tld/
    123.123.123.123

Installation
------------
To include this module in your nginx-installation either do:

    ./configure --add-module=/path/to/ngx_remote_ip/


or in Gentoo simple add this to your `/etc/make.profile`:

    NGINX_ADD_MODULES="/path/to/ngx_remote_ip/"

Configuration
-------------
Simply add a new server-declaration:

    server {
      listen 80;
      server_name ip.mydomain.tld;
      location / {
        remote_ip;
      }
    }


Credits
-------
Thanks to Evan Miller for his guide: http://www.evanmiller.org/nginx-modules-guide.html
This module is heavily based upon it.
