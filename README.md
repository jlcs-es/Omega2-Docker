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



## How to compile C code

Once you are in the Docker container, some environment variables are set (maybe not) for you to use:

```bash
mipsel-openwrt-linux-gcc [options] 
```

The compiler binaries are generated inside the directory:

```bash
/lede/staging_dir/toolchain-mipsel_24kc_gcc-5.4.0_musl-1.1.15/bin/
```

*Note: The 'el' in mipsel indicates it is a Little Endian version of MIPS.*



## I found a bug

Make a pull-request or create an issue.
