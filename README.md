```
turbo test

$ docker run -u node -it --rm -v $PWD:$PWD -w $PWD --entrypoint npm node:18.20.0 ci
$ docker run -u node -it --rm -v $PWD:$PWD -w $PWD --entrypoint npx node:18.20.0 turbo  hello
```
