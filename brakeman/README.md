```
docker network create --driver bridge brakeman
docker run --rm \
  -v "$(pwd):/app:ro" \
  --security-opt="no-new-privileges" \
  --cap-drop=all \
  --read-only \
  --network=brakeman \
  ecneladis/brakeman -f html
```
