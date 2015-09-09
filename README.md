This is the Docker image for my blog's nginx server.

## How to deploy

```
$ docker build -t blog-nginx .
$ docker run -d -p 80:80 \
    --restart=always \
    -v /var/www/blog-static/output:/var/www:ro \
    --name blog blog-nginx
```
