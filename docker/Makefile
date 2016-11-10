
REPO=cich.innoq.io:8091
NAME=scs

URI=$(REPO)/$(NAME)

DIRS = dashboard sys1 sys2 sys3

info:
	echo name: $(NAME)

image: 
	for i in $(DIRS); do docker build -t $(URI)-$$i:latest --rm=true --pull=true --no-cache=true --force-rm=true ./$$i; done

pushonly:
	docker push $(URI):latest

