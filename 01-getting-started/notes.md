# 01 Getting Started

## Setting Up Node

This couse will allow you to go through on code sandbox, or local development. I prefer local develepment...

### setting up node on windows.

Easiest way to setup node is to use NVM. You can get that from [here](https://github.com/coreybutler/nvm-windows/releases). Once downloaded, just run the installer. then you run

```
nvm version
```

this will verify it's working. Then you can install and use node lts:

```
nvm install lts
nvm use lts
```

You might have to accept a UAC prompt when you perform nvm use lts.


### setting up node on Mac.

Easiest way to setup node on mac is still to use NVM, but use the unix version. Easiest way to get it is brew install nvm. Then you'll need to add it to the path. The way I did that was to create a .zshrc file in my root directory (cd ~), and put in:

```
export NVM_DIR="$HOME/.nvm"
[ -s "/opt/homebrew/opt/nvm/nvm.sh" ] && \. "/opt/homebrew/opt/nvm/nvm.sh"
[ -s "/opt/homebrew/opt/nvm/etc/bash_completion.d/nvm" ] && \. "/opt/homebrew/opt/nvm/etc/bash_completion.d/nvm"
```

After that, nvm was registered and working:

```
nvm --version
```

Then you can install and use node lts:

```
nvm install --lts
nvm use --lts
```

You'll notice that the mac version has -- infront of all the arguments. Other then that, that is the only difference I've seen. 