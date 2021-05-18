# Mate-i3-dotfiles

## Details ##
+ **OS**: Fedora 34
+ **Shell**: ZSH
+ **DE**: Mate
+ **WM**: i3-gaps
+ **Theme**: WhiteSur-dark
+ **Icons**: Tela Blue
+ **Cursor**: Bibata Oil
+ **Terminal**: Alacritty


## Dependencies ##
|Dependency|Description|
|:----------:|:-------------:|
|`i3-gaps`|Window manager|
|`feh`|Fast image viewer used as wallpaper setting utility|
|`mate-desktop`|My DE of choice, lightweight and solves some problems you may have with only a wm|
|`mate-session-manager`|Needed to make the display manager show mate as an option|
|`rofi`|Application launcher|
|`slock`|Used to lock the screen|

### Optional Dependencies ###
+ `acpi`: Battery managing cli application, used by top bar widget to determine battery status
+ `bluez`: Bluetooth cli application, used to determine if bluetooth is on
+ `blueman`: Bluetooth managing application, spawns in the bluetooth top panel
+ `nm-connection-editor`: GUI wifi connection editor, spawns in the top panel
+ `xbacklight`: Controls display brightness, which the control of has been mapped to brightness keys

### Fonts You Should Install ###
+ `SF Pro Text`: System font
+ `Inconsolata`: Terminal font.


## Installation ##
You will need to use the `dconf-editor`. You may need to install it as seems most distros don't provide it by default. Once you've got it open, head to `org > mate > desktop > session > required-components`. Change windowmanager from `marco` to `i3`.
Then head up one level to `org > mate > desktop > session` and in required-component-list, delete `filemanager` and `panel`. This is needed otherwise MATE will open a background window for your desktop that will cover everything.
Now log out and back in, and you should find yourself in MATE, but with i3 running too.
[Source](https://mattgreer.dev/blog/mate-and-i3/).

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
