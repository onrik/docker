build:
	docker buildx build --build-arg GO_VERSION=1.25-alpine --platform linux/amd64,linux/arm64 -t onrik/golangci-lint:v1.64-go1.25-alpine .
	docker buildx build --build-arg GO_VERSION=1.26-alpine --platform linux/amd64,linux/arm64 -t onrik/golangci-lint:v1.64-go1.26-alpine .

push:
	docker push onrik/golangci-lint:v1.64-go1.25-alpine
	docker push onrik/golangci-lint:v1.64-go1.26-alpine
