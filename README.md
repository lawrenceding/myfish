## my theme, comes from agnoster
## Install
### Linux
####1. install fish
```
sudo apt-add-repository ppa:fish-shell/release-2
sudo apt-get -y update
sudo apt-get -y install fish
```
####2. install oh-my-fish
```
curl -L https://github.com/oh-my-fish/oh-my-fish/raw/master/bin/install | fish
omf help
```
####3. install my configuration
```
git clone https://github.com/lawrenceding/myfish.git ~/.myfish

mkdir ~/.config/omf/themes
ln -snf ~/.myfish/themes/mytheme ~/.config/omf/themes/mytheme

```
####4. enable mytheme
modify ~/.config/omf/theme
change "default" to "mytheme"
####5. add fonts for prompt fancy
Got the powerline font from https://gist.github.com/qrush/1595572
and don't need to download manual, it's in the repository already.
```
mkdir ~/.fonts
cp ~/.myfish/fonts-for-airline/Inconsolata-dz-Powerline.otf ~/.fonts
fc-cache -vf
```
####6. make fish as default shell
```
chsh -s /usr/bin/fish
```
