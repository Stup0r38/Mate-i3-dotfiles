# i3-dotfiles

![](/Screenshot.png)

## Details ##
+ **OS**: Ubuntu 20.04
+ **Shell**: ZSH
+ **WM**: i3-gaps
+ **Theme**: WhiteSur-dark
+ **Icons**: Tela Blue
+ **Cursor**: Bibata Oil
+ **Terminal**: Alacritty


## Dependencies ##
|Dependency|Description|
|:----------:|:-------------:|
|`i3-gaps`|Window manager|
|`picom`|Compositor, needed mostly for vsync|
|`feh`|Fast image viewer used as wallpaper setting utility|
|`lxpolkit`|Minimal polkit service|
|`rofi`|Application launcher|
|`slock`|Used to lock the screen|
|[i3altlayout](https://github.com/deadc0de6/i3altlayout)|Used for better windows placement|

### Optional Dependencies ###
+ `acpi`: Battery managing cli application, used by top bar widget to determine battery status
+ `bluez`: Bluetooth cli application, used to determine if bluetooth is on
+ `blueman`: Bluetooth managing application, spawns in the bluetooth top panel
+ `nm-connection-editor`: GUI wifi connection editor, spawns in the top panel
+ `xbacklight`: Controls display brightness, which the control of has been mapped to brightness keys
+ `seahorse`: Used to change the keyring password to nothing, to avoid an annoying popup on chromium 

### Fonts You Should Install ###
+ `SF Pro Text`: System font
+ `Inconsolata`: Terminal font.


## My Preferred Applications ##
+ **Text Editor - Micro:** It's just cool and easy to use
+ **File Manager - Thunar**: One of the most lightweight gui file browser and it has very few dependencies (works better with `thunar-archive-plugin`)
+ **Archive Manager - File-roller**: It just works
+ **Web Browser - Brave-browser**: Privacy friendly browser
+ **Terminal - Alacritty**: Faster than kitty and more customizable than st
+ **Theme / Look & Feel Manager - lxappearance**: makes managing icon / cursor / application themes easy, only theme manager with no DE dependencies, and works very well
+ **Task Manager - Lxtask**: Very few dependences and super lightweight


### Other cool applications you should install ###
+ `redshift`: Changed screen warmth based on the time of day
+ `neofetch`: Displays system information in the terminal



## Application Theming ##
### Zsh ###
1. Install oh-my-zsh
```
sh -c "$(curl -fsSL https://raw.github.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"
```
2. Change the zsh theme to powerlevel10k
  + Install powerlevel10k with the command below:
  ```
  git clone --depth=1 https://github.com/romkatv/powerlevel10k.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/themes/powerlevel10k
  ```
  + Open `~/.zshrc` with your fave text editor
  + Set `ZSH_THEME="powerlevel10k/powerlevel10k"` and save the file
3. Install Plugins (Note that the ~/.zshrc edits are already done in this repo)
  + Syntax highlighting (copy and paste the below command to install)
    ```
    git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting
    ```
    + Edit `~/.zshrc`, add `zsh-syntax-highlighting` to the plugins section
  + Autosuggestions (copy and paste the below command to install)
    ```
    git clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions
    ```
    + Edit `~/.zshrc`, add `zsh-autosuggestions` to the plugins section
4. Done! Reopen the terminal to view the fruit of your labor
