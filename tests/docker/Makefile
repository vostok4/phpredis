
all:
	@echo "Run 'make images' to build docker images"

images:
	make image VERSION=2.6.16
	make image VERSION=2.8.0-rc4

image:
	sed -e "s/VERSION/$(VERSION)/g" Dockerfile.template > Dockerfile
	sudo docker build -t redis:$(VERSION) .
	rm -f Dockerfile

