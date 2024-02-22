Things to do after install Pop-Os!

1. Update

```
sudo apt-get update
sudo apt-get upgrade
```

2. install brave browser

```
sudo curl -fsSLo /usr/share/keyrings/brave-browser-archive-keyring.gpg https://brave-browser-apt-release.s3.brave.com/brave-browser-archive-keyring.gpg

echo "deb [signed-by=/usr/share/keyrings/brave-browser-archive-keyring.gpg arch=amd64] https://brave-browser-apt-release.s3.brave.com/ stable main"|sudo tee /etc/apt/sources.list.d/brave-browser-release.list

sudo apt update

sudo apt install brave-browser
```

3. install necessary packages

```
sudo apt-get install fish bat exa trash-cli texlive-full lyx htop xournalpp axel neofetch vlc telegram-desktop rclone calibre alacritty
```

4. install miniconda

```
mkdir -p ~/miniconda3
wget https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh -O ~/miniconda3/miniconda.sh
bash ~/miniconda3/miniconda.sh -b -u -p ~/miniconda3
rm -rf ~/miniconda3/miniconda.sh
~/miniconda3/bin/conda init fish
```

5. install visual studio code

```
wget 'https://code.visualstudio.com/sha/download?build=stable&os=linux-deb-x64' -O code_amd64.deb
sudo dpkg -i code_amd64.deb

```

6. install zoom meeting

```
wget https://zoom.us/client/5.17.5.2543/zoom_amd64.deb
sudo dpkg -i zoom_amd64.deb
sudo apt-get --fix-broken install

```

7. install pycharm

```
wget https://download.jetbrains.com/python/pycharm-community-2023.3.3.tar.gz
tar -xzvf pycharm-community-2023.3.3.tar.gz
sudo bash pycharm-community-2023.3.3/bin/pycharm.sh
rm -r pycharm-community*
```

8. install zotero

```
wget 'https://www.zotero.org/download/client/dl?channel=release&platform=linux-x86_64&version=6.0.30' -O zotero.tar.bz2
tar -xvf zotero.tar.bz2
sudo mv Zotero_linux-x86_64 /opt/zotero
sudo bash /opt/zotero/set_launcher_icon
ln -s /opt/zotero/zotero.desktop ~/.local/share/applications/zotero.desktop
```

