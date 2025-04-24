# Customization_For_Developers 🧑‍💻🎨

# Linux Terminal Customization with Zsh (Video 03 Reference)

This guide provides all the commands and setup steps mentioned in the third video of my YouTube playlist: "Customization for Developers: 03 - Make your LINUX terminal LOOK AMAZING".

---

## Step 1: Change the Default Shell to Zsh
```bash
chsh -s $(which zsh)
```

---

## Step 2: Essential Zsh Plugins
Add these plugins to your `.zshrc` file under the `plugins` array:
```zsh
plugins=(
  git
  zsh-autosuggestions
  zsh-syntax-highlighting
  you-should-use
  aliases
  colorize
  command-not-found
  colored-man-pages
  frontend-search
  sudo
  web-search
  vscode
  npm
)
```

Clone plugin repositories:
```bash
git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting
git clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions
git clone https://github.com/MichaelAquilina/zsh-you-should-use.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/you-should-use
```

---

## Step 3: Install Powerlevel10k Theme
```bash
git clone https://github.com/romkatv/powerlevel10k.git $ZSH_CUSTOM/themes/powerlevel10k
```

Set the theme in `.zshrc`:
```zsh
ZSH_THEME="powerlevel10k/powerlevel10k"
POWERLEVEL9K_MODE="nerdfont-complete"
```

---

## Step 4: Fonts (Nerd Fonts)
To properly render icons and symbols:
- Visit: https://www.nerdfonts.com/
- Recommended: [FiraMono Nerd Font](https://github.com/ryanoasis/nerd-fonts/tree/master/patched-fonts/FiraMono)

Install and apply the font in your terminal settings.

---

## Step 5: Handy Aliases
Add these aliases to your `.zshrc`:
```bash
# Update Ubuntu & apps
alias update='sudo apt update && sudo apt upgrade -y && flatpak update -y && sudo snap refresh'

# Clean up system
alias clean='sudo apt autoremove && sudo apt clean all'

# Clear memory cache
alias cmc='sync && echo 3 | sudo tee /proc/sys/vm/drop_caches'
```

---

📌 For full tutorial, visit the video:
"03 - Make your LINUX terminal LOOK AMAZING" on my [YouTube Playlist](https://www.youtube.com/playlist?list=PL...)

Connect with Me:
- 🌐 Portfolio: https://mos3ab.tech
- 💻 GitHub: https://github.com/Mos3aB696
- 🔗 LinkedIn: https://www.linkedin.com/in/mosaab-abdelkawy
