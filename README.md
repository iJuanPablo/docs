# docs
Be able to access the different documentation you use just form within your computer.

## Requirements

You just need [docker!](www.docker.io)

## Summary

|Package|Location|
|-------|--------|
|docker|[localhost:4000](localhost:4000)|
|kubernetes|[localhost:8080](localhost:8080)|
|angular|[localhost:7070](localhost:7070)|

|React|`software/reacjs.org`|Location<br>`yarn dev`|
|Go tour|`go/src/golang.org/x/tour`|`go/bin`<br>`gotour`|
|Go Docs|`software/go`<br>`go/src/github.com/golang/go`|`godoc -http=:8080 -goroot /home/ijuanpablo/software/go` <br>`godoc -http=:8080 -goroot /home/ijuanpablo/go/src/github.com/golang/go`|
|Angular Material|`software/material.angular.io`|Location<br>`ng serve`|
|Angular|`software/angular/aio`|Location<br>`yarn start`|

## Docker

With docker install just run

`docker run  -it -p 4000:4000 docs/docker.github.io:latest`

## Kubernetes

Go to kubernetes folder

`cd kubernetes`

Build the container

`docker image build -t kubernetes:v0.10 .`

Run it

`docker run -d -p 8080:80 kubernetes:v0.10`

Now you can access it in [localhost:8080](localhost:8080).
If you want to poke around inside the container run

`docker run -ti kubernetes:v0.10 bash`

## Angular

Go to kubernetes folder

`cd angular.io`

Build the container

`docker image build -t angular.io:v0.5 .`

Run it

`docker run -d -p 7070:80 angular.io:v0.5`

Now you can access it in [localhost:7070](localhost:7070).
If you want to poke around inside the container run

`docker run -ti angular.io:v0.5 bash`

## Readings

https://medium.com/@DenysVuika/your-angular-apps-as-docker-containers-471f570a7f2