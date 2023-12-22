# Git Tips
## Generate SSH Key

```
# Gen Key Pair
  ssh-keygen -t ed25519 -C "<Email Address>" -f  <Key Name>

# Activate ssh-agent
  eval "$(ssh-agent -s)"

# Add key
  ssh-add <Key Name or Path to Key>
  ssh-add -l
  
# Set Git Credentials
  git config --global user.name <Username>
  git config --global user.email <Email>
  
# Add key to git
  cat <Path to key>.pub
  Add key on github SSH & GPG Keys

# Test Connection
  ssh -vT git@github.com
```

## Change Ownership of Folder (from root)

```
sudo chown <username>:<username> <path>
```