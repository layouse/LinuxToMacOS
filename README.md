# LinuxToMacOS

GNOME Linux'u WhiteSur tema, ikonlar ve uzantılarla macOS benzeri bir deneyime dönüştürme rehberi.

A complete GNOME customization guide to transform Linux into a polished macOS-inspired desktop using WhiteSur themes, extensions, blur effects and Apple-style UI components.

---

# 🍏 LinuxToMacOS

GNOME masaüstünüzü WhiteSur temaları, GNOME uzantıları, blur efektleri ve Apple tarzı özelleştirmeler ile modern bir macOS deneyimine dönüştürün.

Transform your GNOME Linux desktop into a clean, modern, macOS-inspired experience using WhiteSur themes, GNOME extensions, blur effects, and Apple-style customization.

---

## ✨ Özellikler / Features

### 🇹🇷 Türkçe

* WhiteSur GTK Teması
* WhiteSur İkon Paketi
* Apple San Francisco Yazı Tipleri
* macOS Benzeri Dock
* Blur Efektleri
* Spotlight Benzeri Arama
* Apple Tarzı Üst Menü
* Taşınabilir SSD Desteği

### 🇬🇧 English

* WhiteSur GTK Theme
* WhiteSur Icon Pack
* Apple San Francisco Fonts
* macOS-style Dock
* Blur Effects
* Spotlight-like Search
* Apple-style Top Menu
* Portable SSD Support

---

## 🖥️ Desteklenen Dağıtımlar / Supported Distributions

| Distribution       | Status |
| ------------------ | ------ |
| Debian 13+         | ✅      |
| Ubuntu 24.04+      | ✅      |
| Kali Linux (GNOME) | ✅      |
| Linux Mint (GNOME) | ✅      |
| Pop!_OS            | ✅      |
| Fedora Workstation | ⚠️     |

### 🇹🇷 Türkçe

XFCE, KDE Plasma ve Cinnamon masaüstü ortamları resmi olarak desteklenmemektedir.

### 🇬🇧 English

XFCE, KDE Plasma and Cinnamon are not officially supported.

---

# 1. Sudo Yetkilerinin Yapılandırılması (Sadece Debian)

# 1. Configure Sudo Permissions (Debian Only)

```bash
su -
usermod -aG sudo $USER
exit
```

### 🇹🇷 Türkçe

Komutları çalıştırdıktan sonra oturumu kapatıp yeniden açın.

### 🇬🇧 English

Log out and sign back in after running the commands.

---

# 2. Gerekli Paketlerin Kurulumu

# 2. Install Required Packages

```bash
sudo apt update && sudo apt install -y \
gnome-tweaks \
gnome-shell-extensions \
git \
curl \
chrome-gnome-shell \
alacarte
```

### 🇹🇷 Türkçe

Gerekli tüm paketleri tek komutla yükler.

### 🇬🇧 English

Install all required packages in a single command.

---

# 3. WhiteSur Tema ve İkon Kurulumu

# 3. Install WhiteSur Theme & Icons

```bash
mkdir -p ~/.themes ~/.icons
```

### GTK Teması / GTK Theme

```bash
git clone https://github.com/vinceliuice/WhiteSur-gtk-theme.git --depth=1

cd WhiteSur-gtk-theme

./install.sh -t all -N glassy
```

### İkon Paketi / Icon Theme

```bash
cd ~

git clone https://github.com/vinceliuice/WhiteSur-icon-theme.git --depth=1

cd WhiteSur-icon-theme

./install.sh
```

---

# 4. Apple San Francisco Yazı Tiplerinin Kurulumu

# 4. Install Apple San Francisco Fonts

```bash
git clone https://github.com/AppleDesignResources/SanFranciscoFont.git --depth=1

mkdir -p ~/.local/share/fonts

cp SanFranciscoFont/*.otf ~/.local/share/fonts/

fc-cache -fv
```

### 🇹🇷 Türkçe

GNOME Tweaks → Fonts bölümünden **SF Pro Display** seçin.

### 🇬🇧 English

Select **SF Pro Display** from GNOME Tweaks → Fonts.

---

# 5. Önerilen GNOME Uzantıları

# 5. Recommended GNOME Extensions

| Extension        | Purpose / Amaç   |
| ---------------- | ---------------- |
| Dash to Dock     | macOS Dock       |
| Blur my Shell    | Blur Effects     |
| Logo Menu        | Apple Menu       |
| App Menu Is Back | Active App Title |
| Search Light     | Spotlight Search |
| Just Perfection  | Hide Activities  |

---

# 6. Arayüz İnce Ayarları

# 6. Interface Tweaks

## Tarih Formatı / Date Format

```text
Settings → Region & Language
```

```text
English (United States)
```

---

## Uygulamalar Menüsü Butonunu Gizleme

## Hide Applications Grid Button

```bash
gsettings set org.gnome.shell.extensions.dash-to-dock show-show-apps-button false
```

---

## macOS Menü Çubuğu

## macOS Menu Bar

```text
Finder   File   Edit   View   Go   Window   Help
```

---

# 7. Taşınabilir SSD için GRUB Sabitleme

# 7. Portable SSD GRUB Fix

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

# 8. Sorun Giderme

# 8. Troubleshooting

### Tema değişiklikleri uygulanmıyor

### Theme changes are not applied

```text
Log Out → Log In
```

### Shell tema seçeneği görünmüyor

### Shell theme option missing

Enable:

```text
User Themes
```

---

# 9. Kali Linux Notları

# 9. Kali Linux Notes

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

# 🎯 Nihai Sonuç / Final Result

### 🇹🇷 Türkçe

* Apple tarzı masaüstü görünümü
* WhiteSur teması
* macOS benzeri Dock
* Blur efektleri
* SF Pro yazı tipleri
* Spotlight benzeri arama

### 🇬🇧 English

* Apple-inspired desktop
* WhiteSur theme
* macOS-style Dock
* Blur effects
* SF Pro typography
* Spotlight-like search

---

# 🤝 Katkıda Bulunma / Contributing

Pull request ve öneriler memnuniyetle karşılanır.

Pull requests and suggestions are welcome.

---

