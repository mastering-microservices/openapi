# OpenAPI

https://openapi-generator.tech/docs/installation

```bash
docker pull --platform linux/arm64 openapitools/openapi-generator-cli
```

```bash
docker run --rm   -v ${PWD}:/local openapitools/openapi-generator-cli help
```

```bash
curl https://raw.githubusercontent.com/openapitools/openapi-generator/master/modules/openapi-generator/src/test/resources/3_0/petstore.yaml
```

Generate server
```bash
docker run --rm   -v ${PWD}:/local openapitools/openapi-generator-cli generate   -i /local/petstore.yaml -g python-flask -o /local/out/python-flask
cloc out/python-flask
tree out/python-flask
cat  out/python-flask/README.md
```

Generate clients
```bash
docker run --rm   -v ${PWD}:/local openapitools/openapi-generator-cli generate   -i /local/petstore.yaml -g bash -o /local/out/bash
docker run --rm   -v ${PWD}:/local openapitools/openapi-generator-cli generate   -i /local/petstore.yaml -g typescript-angular -o /local/out/typescript-angular
```

Generate database schema
```bash
docker run --rm   -v ${PWD}:/local openapitools/openapi-generator-cli generate   -i /local/petstore.yaml -g postgresql-schema -o /local/out/postgresql-schema
```

Generate documentation
```bash
docker run --rm   -v ${PWD}:/local openapitools/openapi-generator-cli generate   -i /local/petstore.yaml -g html -o /local/out/html
docker run --rm   -v ${PWD}:/local openapitools/openapi-generator-cli generate   -i /local/petstore.yaml -g dynamic-html -o /local/out/dynamic-html
```

