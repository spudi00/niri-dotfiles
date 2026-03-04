<img width="1920" height="1080" alt="screenshot-2026-02-27_23-04-12" src="https://github.com/user-attachments/assets/4e7fea76-af29-4914-af41-395023d1c5f7" />

# 🖥️ Arch Linux Setup

Personal setup guide for getting an Arch system up and running — packages, mounts, and essentials.

---

## 📦 Prerequisites

### Install `yay` (AUR Helper)

```bash
sudo pacman -S --needed git base-devel
git clone https://aur.archlinux.org/yay.git
cd yay
makepkg -si
```

---

## 💾 Mounting HDD

Create the mount point and add the drive to `/etc/fstab` for automatic mounting on boot:

```bash
sudo mkdir /mnt/hdd
```

Add to `/etc/fstab`:

```
UUID=4ACAE882CAE86B9F  /mnt/hdd  ntfs-3g  uid=1000,gid=1000,umask=022  0  0
```

---

## 📥 Packages

### Official Repos (`pacman`)

```bash
sudo pacman -S --noconfirm \
  kitty vesktop steam mpv eog obs-studio \
  neovim ntfs-3g qbittorrent cava \
  rocm-smi-lib flatpak
```

| Package | Description |
|---|---|
| `kitty` | GPU-accelerated terminal emulator |
| `vesktop` | Discord client |
| `steam` | Gaming platform |
| `mpv` | Media player |
| `eog` | Image viewer |
| `obs-studio` | Streaming / screen recording |
| `neovim` | Text editor |
| `ntfs-3g` | NTFS filesystem support |
| `qbittorrent` | BitTorrent client |
| `cava` | Audio visualizer |
| `rocm-smi-lib` | AMD GPU monitoring |
| `flatpak` | Flatpak app support |

### AUR (`yay`)

```bash
yay -S --noconfirm spotify zen-browser-bin noctalia-shell
```

| Package | Description |
|---|---|
| `spotify` | Music streaming |
| `zen-browser-bin` | Firefox-based privacy browser |
| `noctalia-shell` | Shell theme |
