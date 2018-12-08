# API First experiments

This is a toy repo to experiment with [connexion](https://github.com/zalando/connexion). Rather than write code and generate OpenAPI definitions from the code, with Connexion the OpenAPI definition can be written first, before any code.

Notes
- this python app is a rip-off from the Docker Get-Started app. 
- modifications include the additional use of connexion
- the Dockerfile is modified to use an alpine image, and the pip requirements are fetched before the app is copied to the image, so as to enjoy some caching goodness

Build in docker:
```
docker build -t connexion-api .
```
Run in docker:
```
docker run -p 8080:8080 --name=apitest --rm connextion-api
```

Then in your browser
```
http://<docker-machine ip>:8080
http://<docker-machine ip>:8080/api/greeting
http://<docker-machine ip>:8080/api/ui
```



