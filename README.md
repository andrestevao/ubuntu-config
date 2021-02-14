## OS workflow

* i3 window manager
	* basic install command
		* > sudo apt install i3
	* basic settings
		* high dpi scaling (at the time i'm writing this i'm using a 4k 32" monitor)
			* add to ~/.config/i3/config (for i3)
				* > xrandr --dpi 220
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
