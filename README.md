Satis Docker

```
docker run --rm --init -it \
  --user $(id -u):$(id -g) \
  --volume $(pwd):/build \
  --volume "${COMPOSER_HOME:-$HOME/.composer}:/composer" \
  composer/satis build satis.json docs
```


Test local

```
docker run -d -ti -p 8080:80 --name satis -v $PWD/docs:/usr/share/nginx/html nginx
```


