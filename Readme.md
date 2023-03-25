# Remote container LaTeX starter
## Hacking
### Getting started
If you want to use this starter, you need to use :
- [Visual Studio Code](https://code.visualstudio.com/)
- [Docker](https://www.docker.com/)
- [Dev containers](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-containers)
- [LaTeX Workshop](https://marketplace.visualstudio.com/items?itemName=James-Yu.latex-workshop)

### Add LaTeX plugins
Edit [Dockerfile](.devcontainer/Dockerfile)

### LaTeX commands
If you want to edit your LaTeX commands (compilation, etc.):
- Open [The LaTeX Workshop command files](.vscode/settings.json)
- Edit it
- After refreshing VSC, you'll find your commands inside the LaTeX VSC plugin tab
- The clicked command will be applied on the file you're currently working on

## GitHub action
This repository comes with some [GitHub actions](.github/workflows/compileandmailandrelease.yml)
- Send mail (This action takes the LaTeX project, builds the PDF and send the artifact when you push a new Git tag)
- Create Release (This action creates a release when you push a new Git tag)
- Upload Release Asset (This action takes the LaTeX project, builds the PDF and adds the artifact inside the new release)

If you want to make them work, please go to the [GitHub Secrets and variables actions page](https://github.com/<username>/<forkname>/settings/secrets/actions) and add the keys :
- MAIL_PASSWORD (A new generated Google API secret key)
- MAIL_USERNAME (Your Gmail username)

## External links
- https://github.com/James-Yu/LaTeX-Workshop/wiki/Install#using-docker
- https://code.visualstudio.com/docs/devcontainers/containers

## PDF example
- [Located at the root of the repo](Project.pdf)