# multistage-docker-examples

Examples of how to use multistage docker builds to construct small production images

These examples are from the blog post [All the small things]().

### Python

Here we have a minimal Flask application.

#### Building

Thicc:
```
$ cd python-example
$ docker build -t python-thicc -f Dockerfile_thicc .
```

Slim:
```
$ cd python-example
$ docker build -t python-slim -f Dockerfile_slim .
```

#### Running

Thicc:
```
$ docker run --rm -p 4000:4000 python-thicc
```

Slim:
```
$ docker run --rm -p 4000:4000 python-slim
```

### Java

A Spring Boot HTTP JSON API generated from the Petstore Swagger example and modified to use Java 11.

#### Building

Thicc:
```
$ cd java-example
$ docker build -t java-thicc -f Dockerfile_thicc .
```

Slim:
```
$ cd java-example
$ docker build -t java-slim -f Dockerfile_slim .
```

#### Running

Thicc:
```
$ docker run --rm -p 8080:8080 java-thicc
```

Slim:
```
$ docker run --rm -p 8080:8080 java-slim
```

### Go

A HTTP JSON API generated from the Petstore Swagger example.

#### Building

Thicc:
```
$ cd go-example
$ docker build -t go-thicc -f Dockerfile_thicc .
```

Slim:
```
$ cd go-example
$ docker build -t go-slim -f Dockerfile_slim .
```

#### Running

Thicc:
```
$ docker run --rm -p 5000:5000 go-slim
```

Slim:
```
$ docker run --rm -p 5000:5000 go-slim
```

### Javascript

A React-based, single-page web application.

#### Building

Thicc:
```
$ cd js-example
$ docker build -t js-thicc -f Dockerfile_thicc .
```

Slim:
```
$ cd js-example
$ docker build -t js-slim -f Dockerfile_slim .
```

#### Running

Thicc:
```
$ docker run --rm -p 5000:5000 js-thicc
```

Slim:
```
$ docker run --rm -p 5000:80 js-slim
```
