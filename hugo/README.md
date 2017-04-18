```
docker network create --driver bridge hugo
docker run -it --rm \
  --user `id -u` \
  --security-opt="no-new-privileges" \
  --cap-drop=all \
  -v `pwd`:/var/www/blog \
  --network=hugo \
  --name hugo \
  ecneladis/hugo
```
