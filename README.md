# Docker
# Docker Tutorials
### Installing docker.
I am using manjaro linux for this tutorial


	sudo pacman -S docker

## Checking Docker  On System
 Command: Docker version allows to check docker version.

	[utshav@utshav-pc Docker]$ docker version
	Client:
	 Version:           19.03.5-ce
	 API version:       1.40
	 Go version:        go1.13.4
	 Git commit:        633a0ea838
	 Built:             Fri Nov 15 03:19:09 2019
	 OS/Arch:           linux/amd64
	 Experimental:      false

	Server:
	 Engine:
	  Version:          19.03.5-ce
	  API version:      1.40 (minimum version 1.12)
	  Go version:       go1.13.4
	  Git commit:       633a0ea838
	  Built:            Fri Nov 15 03:17:51 2019
	  OS/Arch:          linux/amd64
	  Experimental:     false
	 containerd:
	  Version:          v1.3.2.m
	  GitCommit:        d50db0a42053864a270f648048f9a8b4f24eced3.m
	 runc:
	  Version:          1.0.0-rc9
	  GitCommit:        d736ef14f0288d6993a1845745d6756cfc9ddd5a
	 docker-init:
	  Version:          0.18.0
	  GitCommit:        fec3683


## Running a Basic Container to Check all things are working Fine.
Go to https://hub.docker.com/ and search for whalesay 
- It is a docker image which outputs the text you want the whale to say.

copy the docker image code.

	docker pull docker/whalesay

	[utshav@utshav-pc Docker]$ docker pull docker/whalesay
	Using default tag: latest
	latest: Pulling from docker/whalesay
	Image docker.io/docker/whalesay:latest uses outdated schema1 manifest format. Please upgrade to a schema2 image for better future compatibility. More information at https://docs.docker.com/registry/spec/deprecated-schema-v1/
	e190868d63f8: Downloading  13.96MB/65.77MB
	909cd34c6fd7: Download complete 
	e190868d63f8: Pull complete 
	909cd34c6fd7: Pull complete 
	0b9bfabab7c1: Pull complete 
	a3ed95caeb02: Pull complete 
	00bf65475aba: Pull complete 
	c57b6bcc83e3: Pull complete 
	8978f6879e2f: Pull complete 
	8eed3712d2cf: Pull complete 
	Digest: sha256:178598e51a26abbc958b8a2e48825c90bc22e641de3d31e18aaf55f3258ba93b
	Status: Downloaded newer image for docker/whalesay:latest
	docker.io/docker/whalesay:latest

##### Running the Image

existing images

	[utshav@utshav-pc Docker]$ docker images
	REPOSITORY          TAG                 IMAGE ID            CREATED             SIZE
	docker/whalesay     latest              6b362a9f73eb        4 years ago         247MB
	
##### Running images

	[utshav@utshav-pc Docker]$ docker run docker/whalesay cowsay hello
	 _______ 
	< hello >
	 ------- 
		\
		 \
		  \     
						##        .            
				  ## ## ##       ==            
			   ## ## ## ##      ===            
		   /""""""""""""""""___/ ===        
	  ~~~ {~~ ~~~~ ~~~ ~~~~ ~~ ~ /  ===- ~~~   
		   \______ o          __/            
			\    \        __/             
			  \____\______/   
#### Another instance
	[utshav@utshav-pc Docker]$ docker run docker/whalesay cowsay domain
	 ________ 
	< domain >
	 -------- 
		\
		 \
		  \     
						##        .            
				  ## ## ##       ==            
			   ## ## ## ##      ===            
		   /""""""""""""""""___/ ===        
	  ~~~ {~~ ~~~~ ~~~ ~~~~ ~~ ~ /  ===- ~~~   
		   \______ o          __/            
			\    \        __/             
			  \____\______/   









