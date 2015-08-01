###For fast work

##Enable tcp
```
sendfile on;
tcp_nopush on;
tcp_nodelay on; 
keepalive_timeout 2;
types_hash_max_size 2048;
server_tokens off;
```
#File Cache Settings
```
open_file_cache          max=5000  inactive=20s;
open_file_cache_valid    30s;
open_file_cache_min_uses 2;
open_file_cache_errors   on;
```
#Gzip Settings
```
gzip on;
gzip_static on;
gzip_disable "msie6";
gzip_http_version 1.1;
gzip_varcy on;
```
#It's important for level of gzip
```
gzip_comp_level 6;
gzip_proxied any;
gzip_types text/plain text/css application/json application/x-javascript text/xml application/xml application/xml+rss text/javascript application/javascript text/        x-js;`
gzip_buffers 16 8k; 
```
#for php-cache`
```
fastcgi_cache_path /var/cache/nginx levels=1:2 keys_zone=microcache:10m max_size=1000m inactive=60m;
```
#turn off logs
```
access_log off;
server_names_hash_bucket_size   64;
