BRANCH := $(shell git rev-parse --abbrev-ref HEAD)
COMMIT := $(shell git rev-parse HEAD)
REPOSITORY=krol
PROJECT=hasher
PORT=8080

build:
	echo "Image: ${REPOSITORY}/${PROJECT}:$(BRANCH)"
	docker build -t ${REPOSITORY}/${PROJECT}:$(BRANCH) .

push:
	docker push ${REPOSITORY}/${PROJECT}:$(BRANCH)

run:
	docker run -it -p ${PORT}:${PORT} ${REPOSITORY}/${PROJECT}:$(BRANCH)