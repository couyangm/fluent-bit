### Windows
Build command:
```
docker build --no-cache `
  --build-arg WINDOWS_VERSION=ltsc2019 `
  --build-arg MSVS_VERSION=16 `
  -t fluent/fluent-bit:master-windows -f ./dockerfiles/Dockerfile.windows .

docker create --name tmp fluent/fluent-bit:master-windows
docker cp tmp:C:\fluent-bit\bin\fluent-bit.exe .\build\
docker rm tmp
```
