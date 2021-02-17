## OS workflow

* i3 window manager
	* basic install command
		* > sudo apt install i3
	* basic settings
		* high dpi scaling (at the time i'm writing this i'm using a 4k 32" monitor)
			* add to ~/.config/i3/config (for i3)
				* > exec xrandr --dpi 220
			* add to ~/.profile (for other applications)
				* > export GDK_SCALE=2
	* set custom config ( WIP )
		* rofi related
			* bind alt + tab in i3 to show windows open
				* (on ~/.config/i3/config)
				* > bindsym Mod1+Tab exec --no-startup-id rofi -modi combi -combi-modi window -show combi
			* bind super + d in i3 to show run dialog 
				* (on ~/.config/i3/config)
				* > bindsym $mod+d exec rofi -show run

* rofi application launcher
	* basic install command
		* > sudo apt install rofi
	* custom settings
		* TO-DO

* tmux
	* basic install command
		* > sudo apt install tmux
	* custom settings
		* TO-DO

* alacritty
	* basic install commands
		* git clone https://github.com/alacritty/alacritty.git
		* cd alacritty
		* sudo apt install curl
		* curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
		* rustup override set stable
		* rustup update stable
		* apt-get install cmake pkg-config libfreetype6-dev libfontconfig1-dev libxcb-xfixes0-dev python3
		* cargo build --release
		* check terminfo
			* infocmp target/release/alacritty
				* if this command returns without any errors, the alacritty terminfo is already installed
				* otherwise, you can install it globally with the following command
					* sudo tic -xe alacritty,alacritty-direct extra/alacritty.info
		* sudo cp target/release/alacritty /usr/local/bin # or anywhere else in $PATH
		* sudo cp extra/logo/alacritty-term.svg /usr/share/pixmaps/Alacritty.svg
		* sudo desktop-file-install extra/linux/Alacritty.desktop
		* sudo update-desktop-database
		* sudo mkdir -p /usr/local/share/man/man1
		* gzip -c extra/alacritty.man | sudo tee /usr/local/share/man/man1/alacritty.1.gz > /dev/null
		* mkdir -p ~/.bash_completion
		* cp extra/completions/alacritty.bash ~/.bash_completion/alacritty
		* echo "source ~/.bash_completion/alacritty" >> ~/.bashrc

## programming

* neovim
	* basic install command
		* > sudo apt install neovim
	* basic settings
		* on (~/.config/nvim/init.vim)
			* show line nums + relative line nums
				* > set number
				* > set relativenumber
			* set tab to 2 spaces
				* > set expandtab
				* > set tabstop=2
				* > set softtabstop=2
				* > set shiftwidth=2
	* custom settings
		* TO-DO

* nodejs & npm
	* basic install command
		* > sudo apt install nodejs npm

* vscode
	* basic install command
		* > sudo snap install --classic code

* git
	* basic install command
		* > sudo apt install git
	* basic configuration
		* TO-DO

## web

* chrome
	* basic install command
		* > wget https://dl.google.com/linux/direct/google-chrome-stable_current_amd64.deb
		* > sudo apt install ./google-chrome-stable_current_amd64.deb
