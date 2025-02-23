# Arch Pacman Cheat Sheet

## Search for a package in pacman repository:
```sudo pacman -Ss packageName```

## Search every package by name / word / string:
```pacman -Q | grep python```

## Install package
```pacman -S packageName```

## Install with 'yes' all prompts
### Method with --noconfirm
```yay -S --noconfirm davinci-resolve-beta```

### Method with `yes` piping
```yes | yay -S davinci-resolve-bet```

