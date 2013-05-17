This is a simple (one file) configuration file for nginx with drupal.
It works with ubuntu 12.04 and 13.04.

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
