# Nginx Cors Plus [![GitHub license](https://img.shields.io/badge/license-Apache%20License%202.0-blue.svg?style=flat)](http://www.apache.org/licenses/LICENSE-2.0)

A simple nginx proxy that you can put in front of any domain to enable CORS.
Handles the preflight requests that can occur when trying to use `application/json` as the request content-type.

## Build it yourself

```bash
docker build nginx-cors-plus/ -t bellotapps/nginx-cors-plus
```

## Docker Run

```bash
docker run -p 8080:80 -e TARGET=example.com bellotapps/nginx-cors-plus
```

## Docker Compose

```yaml
version: '2'
services:
  nginx:
    image: bellotapps/nginx-cors-plus
    ports:
      - 8090:80
    environment:
      - TARGET=https://example.com
```

## License

Copyright 2019 BellotApps

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

   <http://www.apache.org/licenses/LICENSE-2.0>

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.

## Acknowledge

Forked from [https://github.com/shakyShane/nginx-cors-plus](https://github.com/shakyShane/nginx-cors-plus)

## Author

* [Juan Marcos Bellini](https://github.com/juanmbellini)
