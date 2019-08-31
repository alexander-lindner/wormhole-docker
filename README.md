# wormhole-docker
Docker images for wormhole

## use
Use it like the normal wormhole cli:
```bash
docker run --rm -ti  --volume $(pwd):/data  alexanderlindner/wormhole:alpine wormhole send --text "hi there"
```
## tags

-	[`latest`](https://github.com/alexander-lindner/wormhole-docker/blob/master/Dockerfile.ubuntu)
-	[`alpine`](https://github.com/alexander-lindner/wormhole-docker/blob/master/Dockerfile.alpine)

## install

[![asciicast](https://asciinema.org/a/XmgVPkFk48ZSbtCcmU84GlfoY.svg)](https://asciinema.org/a/XmgVPkFk48ZSbtCcmU84GlfoY)

Run the follwing command

```bash
echo 'alias wormhole="docker run --rm -ti  --volume $(pwd):/data  alexanderlindner/wormhole:alpine wormhole"' >> .bashrc
```
restart your shell or open a new one and start using `wormhole`
