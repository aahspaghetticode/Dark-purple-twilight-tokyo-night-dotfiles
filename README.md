# Dotfiles for my first rice, dark purple/twilight/tokyo night.
# Install instructions (KDE&ARCH ONLY): 
*install kvantum*
```sudo pacman -S kvantum```
Open kvantum and install the "kvantum-theme" theme
*install wallpaper*
Navigate to the folder with wallpaper.png from this repo
```plasma-apply-wallpaperimage ./wallpaper.png```
# Konsole tweaks
System settings -> Window management -> Desktop effects
Enable blur
Adjust settings:
Misty (used in unixporn screenshot): Defaults + Turn noise all the way down
Glass: Blur: none Noise: none Saturation: none
Glass: Blur: none Noise: Adjust to liking Saturation: none
Open konsole
right click -> Edit current profile/Create new profile
Set "Command" to /usr/bin/zsh (For later)
Appearance -> Edit
Foreground color: #a29bff  Foreground intense color: #7c77ff Foreground faint color: #b8bdff
OK, OK (DO NOT CLOSE KONSOLE)
Cool looking terminal prompt: ```sudo pacman -S zsh starship
chsh -s $(which zsh)
eval "$(starship init zsh)"
echo 'eval "$(starship init zsh)"' >> ~/.zshrc
cat > ~/.config/starship.toml << 'EOF'
"$schema" = 'https://starship.rs/config-schema.json'

format = """
[░▒▓](#a3aed2)\
[ bash/zsh ](bg:#a3aed2 fg:#090c0c)\
[](bg:#769ff0 fg:#a3aed2)\
$directory\
[](fg:#769ff0 bg:#394260)\
$git_branch\
$git_status\
[](fg:#394260 bg:#212736)\
$nodejs\
$rust\
$golang\
$php\
[](fg:#212736 bg:#1d2230)\
$time\
[ ](fg:#1d2230)\
\n$character"""

[directory]
style = "fg:#e3e5e5 bg:#769ff0"
format = "[ $path ]($style)"
truncation_length = 3
truncation_symbol = "…/"

[directory.substitutions]
"Documents" = "󰈙 "
"Downloads" = " "
"Pictures" = " "

[git_branch]
symbol = ""
style = "bg:#394260"
format = '[[ $symbol $branch ](fg:#769ff0 bg:#394260)]($style)'

[git_status]
style = "bg:#394260"
format = '[[($all_status$ahead_behind )](fg:#769ff0 bg:#394260)]($style)'

[nodejs]
symbol = ""
style = "bg:#212736"
format = '[[ $symbol ($version) ](fg:#769ff0 bg:#212736)]($style)'

[rust]
symbol = ""
style = "bg:#212736"
format = '[[ $symbol ($version) ](fg:#769ff0 bg:#212736)]($style)'

[golang]
symbol = ""
style = "bg:#212736"
format = '[[ $symbol ($version) ](fg:#769ff0 bg:#212736)]($style)'

[php]
symbol = ""
style = "bg:#212736"
format = '[[ $symbol ($version) ](fg:#769ff0 bg:#212736)]($style)'

[time]
disabled = false
time_format = "%R" # Hour:Minute Format
style = "bg:#1d2230"
format = '[[ $time ](fg:#a0a9cb bg:#1d2230)]($style)'
EOF```
/ \
 |
Paste this codeblock into Bash 
