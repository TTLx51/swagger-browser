# Explore swagger API REST with swagger-ui and docker

## REQUIREMENTS
 - docker-compose
 - docker engine

## run swager-ui
```bash
docker-compose -f docker-compose.dev.yml up
```

Add in your hosts, the domains
```bash
sudo sh -c "echo '127.0.0.1 browser.swagger.loc swaggerui.swagger.loc' >> /etc/hosts"
```

With your browser go to http://swaggerui.swagger.loc:81

## generate .JSON file from .yaml file
```bash
docker run -it -w /app -v $PWD:/app --rm swaggerapi/swagger-codegen-cli generate -i public/tiptv/swagger.yaml -l swagger
```
