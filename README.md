# Linux Terminal Customization with Zsh (Video 03 Reference)

This guide provides all the commands and setup steps mentioned in the third video of my YouTube playlist: "Customization for Developers: 03 - Make your LINUX terminal LOOK AMAZING".

---

## Step 1: Install ZSH  
```bash
sudo apt install zsh
```

---

## Step 2: Change the Default Shell to Zsh
```bash
chsh -s $(which zsh)
```

---

## Step 3: Essential Zsh Plugins
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

## Step 4: Install Powerlevel10k Theme
```bash
git clone https://github.com/romkatv/powerlevel10k.git $ZSH_CUSTOM/themes/powerlevel10k
```

Set the theme in `.zshrc`:
```zsh
ZSH_THEME="powerlevel10k/powerlevel10k"
POWERLEVEL9K_MODE="nerdfont-complete"
```

---

## Step 5: Fonts (Nerd Fonts)
To properly render icons and symbols:
- Visit: https://www.nerdfonts.com/
- Recommended: [FiraMono Nerd Font](https://github.com/ryanoasis/nerd-fonts/tree/master/patched-fonts/FiraMono)

Install and apply the font in your terminal settings.

---

## Step 6: Handy Aliases
Add these aliases to your `.zshrc`:
```bash
# Update Ubuntu & apps
alias update='sudo apt update && sudo apt upgrade -y && flatpak update -y && sudo snap refresh'

# Clean up the system
alias clean='sudo apt autoremove && sudo apt clean all'

# Clear memory cache
alias cmc='sync && echo 3 | sudo tee /proc/sys/vm/drop_caches'
```

---
# 05-Explore different ways to INSTALL APPS on LINUX [Arabic]
```bash
# For Appimage
sudo apt install libfuse2 
```


---

---
# 06-Installing programming apps (Vs Code - Postman - MongoDB - MySQL - Obsidian) [Arabic]

---
## Postman
```bash
sudo tar -xvzf postman-linux-x64.tar.gz -C /opt/ (manually installed software packages).
sudo ln -s /opt/Postman/Postman /usr/bin/postman (Optional Software - Binary)
sudo nano /usr/share/applications/postman.desktop

[Desktop Entry]
Name=Postman
Exec=/usr/bin/postman
Icon=/opt/Postman/app/resources/app/assets/icon.png
Type=Application
Categories=Development;
Terminal=false
```
## Postman
```bash
sudo tar -xvzf postman-linux-x64.tar.gz -C /opt/ (manually installed software packages).
sudo ln -s /opt/Postman/Postman /usr/bin/postman (Optional Software - Binary)
sudo nano /usr/share/applications/postman.desktop

[Desktop Entry]
Name=Postman
Exec=/usr/bin/postman
Icon=/opt/Postman/app/resources/app/assets/icon.png
Type=Application
Categories=Development;
Terminal=false
```
---
## MySQL
```bash
sudo apt update && sudo apt upgrade -y
sudo apt install mysql-server -y
sudo systemctl enable --now mysql
sudo mysql_secure_installation
systemctl status mysql
sudo mysql -u root -p
```
---
## Obsidian
```bash
mkdir -p ~/AppImages
mv ~/Downloads/Obsidian-1.8.7.AppImage ~/AppImages/
chmod +x ~/AppImages/Obsidian-1.8.7.AppImage
nano ~/.local/share/applications/obsidian.desktop

[Desktop Entry]
Type=Application
Name=Obsidian
Exec=/home/[your-username]/AppImages/Obsidian-1.8.7.AppImage
Icon=obsidian
Comment=Markdown-based knowledge base
Categories=Office;Utility;
Terminal=false

update-desktop-database ~/.local/share/applications/
```

---

📌 For the full tutorials, visit the playlist:
"Customization for Developers 🎨" on my [YouTube Channel](https://youtube.com/playlist?list=PL-aLh5gc6xE2Z2oh5jvuZGNh6rD4tTiEk&si=X61SyJTSiRYhM10o)

Connect with Me:
- 🌐 Portfolio: https://mos3ab.tech
- 💻 GitHub: https://github.com/Mos3aB696
- 🔗 LinkedIn: https://www.linkedin.com/in/mosaab-abdelkawy
