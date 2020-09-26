BRANCH := $(shell git rev-parse --abbrev-ref HEAD)
COMMIT := $(shell git rev-parse HEAD)
REPOSITORY=krol
PROJECT=nginx
PORT=8080
CONTAINER_PORT=80

build:
	echo "Image: ${REPOSITORY}/${PROJECT}:$(BRANCH)"
	docker build -t ${REPOSITORY}/${PROJECT}:$(BRANCH) .

push:
	docker push ${REPOSITORY}/${PROJECT}:$(BRANCH)

run:
	docker run -it -p ${PORT}:${CONTAINER_PORT} ${REPOSITORY}/${PROJECT}:$(BRANCH)

test:
	curl http://localhost:8080/

validate-nginx:
	docker run --rm -t ${REPOSITORY}/${PROJECT}:$(BRANCH) nginx -c /etc/nginx/nginx.conf -t