.PHONY: build
build:
	docker build --tag my-scratch .

# Have to authenticate to dockerhub and create repo first:
# https://docs.docker.com/engine/reference/commandline/login/
.PHONY: push-dockerhub
push-dockerhub:
	docker tag my-scratch ihtemad/my-scratch # defaults to latest
	docker push ihtemad/my-scratch

	docker tag my-scratch ihtemad/my-scratch:0.0.0
	docker push ihtemad/my-scratch:0.0.0

# Have to authenticate to ghcr.io first
# https://docs.github.com/en/packages/working-with-a-github-packages-registry/working-with-the-container-registry#authenticating-to-the-container-registry
.PHONY: push-github-packages
push-github-packages:
	docker tag my-scratch-image ghcr.io/sidpalas/my-scratch-image # defaults to latest
	docker push ghcr.io/sidpalas/my-scratch-image

	docker tag my-scratch-image ghcr.io/sidpalas/my-scratch-image:abc-123 # defaults to latest
	docker push ghcr.io/sidpalas/my-scratch-image:abc-123
