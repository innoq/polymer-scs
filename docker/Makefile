
REPO=cich.innoq.io:8091
NAME=scs

#URI=$(REPO)/$(NAME)
URI=$(NAME)

DIRS = cors-nginx dashboard sys1 sys2 sys3 assets

info:
	echo name: $(NAME)

images: 
	for i in $(DIRS); do docker build -t $(URI)-$$i:latest --rm=true --pull=false --no-cache=true --force-rm=true ./$$i; done

pushonly:
	docker push $(URI):latest

run: image
	docker-compose up -d

stop:
	docker-compose kill ; docker-compose rm -f

