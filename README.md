# Code-server compose project

Certbot must be ran standalone beforehand,
otherwise nginx will fail to start.

Alternatively, see [here](https://github.com/wmnnd/nginx-certbot) for
a way to load dummy certificates, in order for nginx to start and serve
the acme challenge.

Example command for running certbot standalone:

```
docker run --rm -it \
        -v "$(pwd)/certbot/conf:/etc/letsencrypt" \
        -v "$(pwd)/certbot/www:/var/www/certbot" \
        -p "80:80"
        certbot/certbot certonly
```

Following the instructions presented.
