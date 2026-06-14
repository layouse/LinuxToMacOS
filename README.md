# LinuxToMacOS
GNOME Linux'u WhiteSur tema, ikonlar ve uzantılarla macOS benzeri bir deneyime dönüştürme rehberi
--------------------------
A complete GNOME customization guide to transform Linux into a polished macOS-inspired desktop using WhiteSur themes, extensions, blur effects and Apple-style UI components.
# 🍏 LinuxToMacOS

Transform your GNOME Linux desktop into a clean, modern, macOS-inspired experience using WhiteSur themes, GNOME extensions, blur effects, and Apple-style customization.

GNOME masaüstünüzü WhiteSur temaları, GNOME uzantıları, blur efektleri ve Apple tarzı özelleştirmeler ile modern bir macOS deneyimine dönüştürün.

---

## ✨ Features / Özellikler

### 🇬🇧 English

* WhiteSur GTK Theme
* WhiteSur Icon Pack
* Apple San Francisco Fonts
* macOS-style Dock
* Blur Effects
* Spotlight-like Search
* Apple-style Top Menu
* Portable SSD Support

### 🇹🇷 Türkçe

* WhiteSur GTK Teması
* WhiteSur İkon Paketi
* Apple San Francisco Yazı Tipleri
* macOS Benzeri Dock
* Blur Efektleri
* Spotlight Benzeri Arama
* Apple Tarzı Üst Menü
* Taşınabilir SSD Desteği

---

## 🖥️ Supported Distributions / Desteklenen Dağıtımlar

| Distribution       | Status |
| ------------------ | ------ |
| Debian 13+         | ✅      |
| Ubuntu 24.04+      | ✅      |
| Kali Linux (GNOME) | ✅      |
| Linux Mint (GNOME) | ✅      |
| Pop!_OS            | ✅      |
| Fedora Workstation | ⚠️     |

### 🇬🇧 English

XFCE, KDE Plasma and Cinnamon are not officially supported.

### 🇹🇷 Türkçe

XFCE, KDE Plasma ve Cinnamon masaüstü ortamları resmi olarak desteklenmemektedir.

---

# 1. Configure Sudo Permissions (Debian Only)

# 1. Sudo Yetkilerinin Yapılandırılması (Sadece Debian)

```bash
su -
usermod -aG sudo $USER
exit
```

### 🇬🇧 English

Log out and sign back in after running the commands.

### 🇹🇷 Türkçe

Komutları çalıştırdıktan sonra oturumu kapatıp yeniden açın.

---

# 2. Install Required Packages

# 2. Gerekli Paketlerin Kurulumu

```bash
sudo apt update && sudo apt install -y \
gnome-tweaks \
gnome-shell-extensions \
git \
curl \
chrome-gnome-shell \
alacarte
```

### 🇬🇧 English

Install all required packages in a single command.

### 🇹🇷 Türkçe

Gerekli tüm paketleri tek komutla yükler.

---

# 3. Install WhiteSur Theme & Icons

# 3. WhiteSur Tema ve İkon Kurulumu

```bash
mkdir -p ~/.themes ~/.icons
```

### GTK Theme / GTK Teması

```bash
git clone https://github.com/vinceliuice/WhiteSur-gtk-theme.git --depth=1

cd WhiteSur-gtk-theme

./install.sh -t all -N glassy
```

### Icon Theme / İkon Paketi

```bash
cd ~

git clone https://github.com/vinceliuice/WhiteSur-icon-theme.git --depth=1

cd WhiteSur-icon-theme

./install.sh
```

---

# 4. Install Apple San Francisco Fonts

# 4. Apple San Francisco Yazı Tiplerinin Kurulumu

```bash
git clone https://github.com/AppleDesignResources/SanFranciscoFont.git --depth=1

mkdir -p ~/.local/share/fonts

cp SanFranciscoFont/*.otf ~/.local/share/fonts/

fc-cache -fv
```

### 🇬🇧 English

Select **SF Pro Display** from GNOME Tweaks → Fonts.

### 🇹🇷 Türkçe

GNOME Tweaks → Fonts bölümünden **SF Pro Display** seçin.

---

# 5. Recommended GNOME Extensions

# 5. Önerilen GNOME Uzantıları

| Extension        | Purpose / Amaç   |
| ---------------- | ---------------- |
| Dash to Dock     | macOS Dock       |
| Blur my Shell    | Blur Effects     |
| Logo Menu        | Apple Menu       |
| App Menu Is Back | Active App Title |
| Search Light     | Spotlight Search |
| Just Perfection  | Hide Activities  |

---

# 6. Interface Tweaks

# 6. Arayüz İnce Ayarları

## Date Format / Tarih Formatı

```text
Settings → Region & Language
```

```text
English (United States)
```

---

## Hide Applications Grid Button

## Uygulamalar Menüsü Butonunu Gizleme

```bash
gsettings set org.gnome.shell.extensions.dash-to-dock show-show-apps-button false
```

---

## macOS Menu Bar

## macOS Menü Çubuğu

```text
Finder   File   Edit   View   Go   Window   Help
```

---

# 7. Portable SSD GRUB Fix

# 7. Taşınabilir SSD için GRUB Sabitleme

```bash
su -

grub-install \
--target=x86_64-efi \
--efi-directory=/boot/efi \
--bootloader-id=debian \
--recheck \
--removable

update-grub
```

---

# 8. Troubleshooting

# 8. Sorun Giderme

### Theme changes are not applied

### Tema değişiklikleri uygulanmıyor

```text
Log Out → Log In
```

### Shell theme option missing

### Shell tema seçeneği görünmüyor

Enable:

```text
User Themes
```

---

# 9. Kali Linux Notes

# 9. Kali Linux Notları

```bash
sudo apt update

sudo apt install -y kali-desktop-gnome
```

Choose:

```text
gdm3
```

Then select:

```text
GNOME
```

at the login screen.

---

# 🎯 Final Result / Nihai Sonuç

### 🇬🇧 English

* Apple-inspired desktop
* WhiteSur theme
* macOS-style Dock
* Blur effects
* SF Pro typography
* Spotlight-like search

### 🇹🇷 Türkçe

* Apple tarzı masaüstü görünümü
* WhiteSur teması
* macOS benzeri Dock
* Blur efektleri
* SF Pro yazı tipleri
* Spotlight benzeri arama

---

---

# 📜 License / Lisans

MIT License
