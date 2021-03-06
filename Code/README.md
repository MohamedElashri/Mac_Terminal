# Custom My Terminal


## Oh My Zsh

To install the famous framework

```
curl -fsSL --output omz_installer.sh
https://raw.github.com/robbyrussell/oh-my-zsh/master/tools/install.sh
```

Read the script over to ensure it's safe, and then execute it:

```
zsh omz_installer.sh
```

Restart iTerm2 to experience the new world of Oh My Zsh.

```
sh ./omz_installer.sh
```


Check the installed version with:


```
zsh --version
```

Upgrade it with

```
upgrade_oh_my_zsh
```

## My terminal's theme

Powerlevel10k is a popular theme for zsh. It emphasizes speed, flexibility, and out-of-the-box experience. To install it we use 

```
git clone https://github.com/romkatv/powerlevel10k.git $ZSH_CUSTOM/themes/powerlevel10k

```


Then enable it in ~/.zshrc. Open the config file (.zshrc) by running:


```
nano ~/.zshrc
```

Change the ZSH_THEME value to: 

```
ZSH_THEME="powerlevel10k/powerlevel10k"
```

Save and update the changes by running the command `source ~/.zshrc`. Powerlevel10k's configuration wizard should start automatically; enter p10k configure if it doesn't. Now you can start choosing the user interface options.


## plugins


1. [zsh-autosuggestions](zsh-autosuggestions): Autocompletes suggestions based on your history. It's really useful for commonly used commands like docker run, make, and magerun. Install it with

```
$ git clone https://github.com/zsh-users/zsh-autosuggestions \
${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions
```


2. [zsh-syntax-highlighting](https://github.com/zsh-users/zsh-syntax-highlighting): This feature highlights correctly typed commands green, incorrect commands red, and underlines folders and files. To install we run the following: 

```
$ git clone https://github.com/zsh-users/zsh-syntax-highlighting.git \
${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting
```

3. [exa-zsh](https://github.com/MohamedElashri/exa-zsh): This plugin defines useful aliases that can be used for `exa` the moden alternative of `ls.`Install with the following code 

```
cd $ZSH_CUSTOM/plugins/
git clone https://github.com/MohamedElashri/exa-zsh
```

4. [cp](https://github.com/ohmyzsh/ohmyzsh/tree/master/plugins/cp): This plugin defines a `cpv` function that uses `rsync` so that you get the features and security of this command. Install using the following: 

```
cd $ZSH_CUSTOM/plugins/
git clone https://github.com/ohmyzsh/ohmyzsh/tree/master/plugins/cp
```


5. [copyfile](https://github.com/ohmyzsh/ohmyzsh/tree/master/plugins/copyfile):  Puts the contents of a file in your system clipboard so you can paste it anywhere. Install using the following:

```
cd $ZSH_CUSTOM/plugins/
git clone https://github.com/ohmyzsh/ohmyzsh/tree/master/plugins/copyfile
```



To activate the plugins, in ~/.zshrc, change the line that starts with plugins= to:

```
plugins=( git zsh-syntax-highlighting zsh-autosuggestions exa-zsh cp copyfile) 
```

Restart the terminal to start the journey. 
