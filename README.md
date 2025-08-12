# OpenFOAM 11 — Ubuntu Install (Foundation)

Tested on Ubuntu 22.04/24.04.

## Install

```bash
# Add repo + key
sudo sh -c "wget -O - https://dl.openfoam.org/gpg.key > /etc/apt/trusted.gpg.d/openfoam.asc"
sudo add-apt-repository http://dl.openfoam.org/ubuntu

# Update & install
sudo apt update
sudo apt install openfoam11

# Enable in current shell
source /opt/openfoam11/etc/bashrc

# Optional: alias to load OF11 later (installed under /opt)
echo 'alias of11="source /opt/openfoam11/etc/bashrc"' >> ~/.bashrc
source ~/.bashrc

# Verify
of11         # loads env (or just source /opt/... again)
foamVersion
simpleFoam -help
```

> Note: If you built OpenFOAM from source under `$HOME/OpenFOAM/OpenFOAM-11`, change the alias to:
> ```bash
> alias of11="source $HOME/OpenFOAM/OpenFOAM-11/etc/bashrc"
> ```
