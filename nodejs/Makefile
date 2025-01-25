.POSIX:
.SUFFIXES:
.SILENT:

DOCKER = docker
DOCKER_DIR = .docker
IID_FILE = iid
TAG = local/pnpm:latest

help: ## Show this help
	grep -E -h '\s##\s' $(MAKEFILE_LIST) | awk 'BEGIN {FS = ":.*?## "}; {printf "\033[36m%-20s\033[0m %s\n", $$1, $$2}'

shell: $(DOCKER_DIR)/$(IID_FILE) ## Run a shell inside the container
	$(DOCKER) run --rm --tty --interactive \
		--pull never \
		--volume "$(PWD):/app" \
		--workdir /app \
		$(TAG) /bin/ash

$(DOCKER_DIR)/$(IID_FILE):
	mkdir -p $(DOCKER_DIR)
	$(DOCKER) build \
		--iidfile $(DOCKER_DIR)/$(IID_FILE) \
		--tag $(TAG) \
		https://github.com/matijs/dockerfiles.git#main:pnpm

clean: ## Clean up
	rm -f $(DOCKER_DIR)/$(IID_FILE)
