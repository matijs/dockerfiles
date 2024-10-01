# pnpm

## Suggested usage

```shell
$ docker run --rm --tty --interactive \
  --volume "$(pwd):/app" \
  --volume pnpm-store:/root/.local/share/pnpm/store/ \
  --workdir /app \
  local/pnpm:latest /bin/ash
```
