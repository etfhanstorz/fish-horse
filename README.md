# fish-horse

Apt repository for custom Raspberry Pi OS packages.

Add to a Pi (Raspberry Pi OS Trixie, arm64):

    sudo install -d /etc/apt/keyrings
    curl -fsSL https://etfhanstorz.github.io/fish-horse/fish-horse-archive-key.asc | sudo gpg --dearmor -o /etc/apt/keyrings/fish-horse.gpg
    echo "deb [signed-by=/etc/apt/keyrings/fish-horse.gpg] https://etfhanstorz.github.io/fish-horse trixie main" | sudo tee /etc/apt/sources.list.d/fish-horse.list
    sudo apt update && sudo apt full-upgrade
