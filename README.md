# Pixi Pack Action Example 

This is an example repo that uses the [pixi-pack](https://github.com/marketplace/actions/pixi-pack-action) and [install script](https://github.com/Wytamma/pixi-pack-install-script) actions to create cross-platform self-extracting binaries of environments and and install script for python on each release e.g. https://github.com/Wytamma/pixi-python/releases/latest.

See the GutHub workflow for examples of how to use the actions.

## Usage

Download and activate the self-extracting environments 

```bash
# Download the environment
wget https://github.com/Wytamma/pixi-python/releases/download/v1.0.8/pixi-python-v1.0.8-osx-arm64.sh -O environment.sh
# Setup the environment
chmod +x environment.sh
./environment.sh
# Activate the environment
source ./environment.sh
```

Install python from this environment on a unix system

```bash
curl -sSL https://github.com/Wytamma/pixi-python/releases/latest/download/install.sh | bash -s -- --name pixi-python
pixi-python -V
```
