# Omega2-Docker

Based on [borromeotlhs' dockerfile](https://hub.docker.com/r/borromeotlhs/docker-omega2plus/builds/bvdfelnmsdmeepz6hvtktcn/) I wrote a more refined version that sets everything beforehand (no menuconfig needed).



## How to use

Pull and run from [my Docker Hub](https://hub.docker.com/r/jlcs/omega2-sdk/) with the command:

```bash
docker run -it --name omega2-sdk-app -v /my_host_dir:/remote jlcs/omega2-sdk bash
```

If necessary (the built image being less than 1GB is an indicative) run ```make``` to build the SDK.

To resume the created container:

```bash
docker container ls -a              # Check the container's name if you didn't use --name
docker start <container-name>	      # Start the omega2SDK container
docker attach <container-name> 	    # Start interactive console
```




## Read more

Visit [my blog](http://developer.jlcs.es/2017-02-05-onion-omega2-docker-sdk/) for some more detailed information (if available).
