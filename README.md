```
turbo test

# start cache
$ docker run -it --rm -e TURBO_TOKEN=1234 -e NODE_ENV=production -e LOG_LEVEL=debug -e LOG_MODE=stdout -e STORAGE_PROVIDER=local -e STORAGE_PATH=/tmp/cache -e AUTH_MODE=static -e PORT=8089 -p 8089:8089 ducktors/turborepo-remote-cache

# use remote cache (uses .turbo/cache as local cache of the remote cache)
$ docker run -u node -it --rm -v $PWD:$PWD -w $PWD --entrypoint npm node:18.20.0 ci
$ docker run -e TURBO_API=http://192.168.111.250:8089 -e TURBO_TEAM=team_lf_sw -e TURBO_TOKEN=1234 -u node -it --rm -v $PWD:$PWD -w $PWD --entrypoint npx node:18.20.0 turbo  hello
```
