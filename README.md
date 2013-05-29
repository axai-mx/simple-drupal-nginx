This is a simple (one file) configuration file for nginx with drupal.
It works with ubuntu 12.04 and 13.04.

It is based on http://wiki.nginx.org/Drupal

## Pre-requisites

* php5-fpm installed and all drupal dependencies (php5-mysql or php5-postgres, php5-gd, etc)
* nginx installed

## Usage

You clone the repo, then just create a new config file for you new site.

file: /etc/nginx/sites-available/sample-site.conf

    server {
      listen       80;
      server_name  dev.axai.org;
      root         /path/to/your/drupal/folder;
      include      /path/to/your/drupal.conf;
    }

Then just enable the site by doing a symlink to /etc/nginx/sites-enabled and
restarting nginx.

    ln -s /etc/nginx/sites-available/sample-site.conf /etc/nginx/sites-enabled/sample-site.conf

