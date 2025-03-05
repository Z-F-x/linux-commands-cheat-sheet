# Pacman / Aur Cheat Sheet

## Search for a package in pacman repository:
```sudo pacman -Ss packageName```

## Search for package details
```pacman -Si packageName```

## Search every package by name / word / string:
```pacman -Q | grep python```

## Install package
```pacman -S packageName```

## Search for installed package
```pacman -Qs firefox```

## Explicitly list packages installed manually or with AUR (will not list flatpak or snap)
```pacman -Qm```
##### NOTE: For flatpak and snap use the ```list``` option.
- ```snap list```
- ```flatpak list```

## Install with 'yes' all prompts
### Method with --noconfirm
```yay -S --noconfirm davinci-resolve-beta```

### Method with `yes` piping
```yes | yay -S davinci-resolve-bet```

## Prevent password timeout: runs sudo in a loop to prevent password input dialogue timeout
```--sudoloop```

