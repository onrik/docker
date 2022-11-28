VERSION = 3.7.0
build:
	docker build --build-arg VERSION=$(VERSION) . -t goose:$(VERSION)

push:
	docker tag goose:$(VERSION) onrik/goose:$(VERSION)
	docker tag goose:$(VERSION) onrik/goose:latest
	docker push onrik/goose:$(VERSION)
	docker push onrik/goose:latest