
## hooks/build


``` bash
#!/usr/bin/env sh

echo "------ HOOK START - BUILD -------"
printenv

docker build --build-arg BUILD_DATE=`date -u +"%Y-%m-%dT%H:%M:%SZ"` --build-arg VCS_REF=$SOURCE_COMMIT --build-arg GIT_SHA1=$GIT_SHA1 -t $IMAGE_NAME  .
```


