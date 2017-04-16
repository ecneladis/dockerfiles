```
docker network create --driver bridge bundler-audit
docker run --rm \
  -v "$(pwd):/app:ro" \
  --security-opt="no-new-privileges" \
  --cap-drop=all \
  --read-only \
  --network=bundler-audit \
  ecneladis/bundler-audit
```
