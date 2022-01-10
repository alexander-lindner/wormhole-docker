# wormhole-docker
Small Docker image for wormhole (so you don't need the nasty python dependency)

## use
Use it like the normal wormhole cli:
```bash
docker run --rm -ti  --volume $(pwd):/data ghcr.io/alexander-lindner/wormhole-docker:v1.0.0 send --text "hi there"
```

## install

[![asciicast](https://asciinema.org/a/XmgVPkFk48ZSbtCcmU84GlfoY.svg)](https://asciinema.org/a/XmgVPkFk48ZSbtCcmU84GlfoY)

Run the following command
### zsh
```bash
echo 'alias wormhole="docker run --rm -ti  --volume $(pwd):/$(basename $(pwd)) -w /$(basename $(pwd)) -u $(id -u ${USER}):$(id -g ${USER})  ghcr.io/alexander-lindner/wormhole-docker:v1.0.0"' >> .zshrc && . .zshrc
```

### bash
```bash
echo 'alias wormhole="docker run --rm -ti  --volume $(pwd):/$(basename $(pwd)) -w /$(basename $(pwd)) -u $(id -u ${USER}):$(id -g ${USER})  ghcr.io/alexander-lindner/wormhole-docker:v1.0.0"' >> .bashrc && . .bashrc
```