# HLS Reverse Proxy
## Setup

1. Install Nginx using [manual](https://nginx.org/en/linux_packages.html)
1. Replace *<HLS root name>* in `./conf.d/hls-proxy.conf` with your HLS root server hostname
1. Set *server_name*  in `./conf.d/hls-proxy.conf`
1. `rm /etc/nginx/conf.d/default.conf`
1. `ln -s $(pwd)/conf.d/hls-proxy.conf /etc/nginx/conf.d/`
1. `systemctl restart nginx`
1. Install *certbot* `apt install -y certbot python3-certbot-nginx`
1. Run `certbot --nginx` to get SSL certificate 

