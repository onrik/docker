PROJECT = assetto-server
VERSION = 0.0.50
build:
	docker build --build-arg VERSION=$(VERSION) -t $(PROJECT):$(VERSION) --progress=plain .

push:
	docker tag $(PROJECT):$(VERSION) onrik/$(PROJECT):$(VERSION)
	docker tag $(PROJECT):$(VERSION) onrik/$(PROJECT):latest
	docker push onrik/$(PROJECT):$(VERSION)
	docker push onrik/$(PROJECT):latest
