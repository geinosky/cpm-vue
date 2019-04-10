# cpm-vue

### Local development

To spin up a docker container, first build the image:

```bash
docker build -t vuejs-cookbook/dockerize-vuejs-app .
```

Then build the container with:

```
docker run -it -p 8080:8080 --rm --name dockerize-vuejs-app-1 vuejs-cookbook/dockerize-vuejs-app
```