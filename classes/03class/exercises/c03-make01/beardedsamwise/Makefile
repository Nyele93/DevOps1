SHA = $(shell git rev-parse --short HEAD)
PORT ?= 8000
NAME = "Sam Bentley"

.PHONY: build
build:
	@echo "BUILDING DOCKER IMAGE WITH TAG c03-make01:$(SHA)"
	@echo "This image was created by $(NAME), based on the short commit $(SHA)" > index.html
	@docker build -t make01:$(SHA) .

.PHONY: push
push:
	@echo "PUSHING DOCKER IMAGE TO DOCKER HUB WITH TAG c03-make01:$(SHA)"
	@docker tag make01:$(SHA) beardedsamwise/c03-make01:$(SHA)
	@docker push beardedsamwise/c03-make01:$(SHA)

.PHONY: run
run:
	@echo "RUNNING DOCKER IMAGE WITH TAG c03-make01:$(SHA) ON PORT $(PORT)"
	@docker run -it -p $(PORT):80 make01:$(SHA)