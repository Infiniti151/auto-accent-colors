# Auto Adwaita Colors

[![GitHub release](https://img.shields.io/github/v/release/celiopy/auto-adwaita-colors?style=flat-square)](https://github.com/celiopy/auto-adwaita-colors/releases)  
A GNOME extension that **automatically changes the icon theme based on the accent color**.  

This extension is a complementary tool for the [Adwaita-colors Icons](https://github.com/dpejoh/Adwaita-colors), making your desktop experience more dynamic and visually cohesive.

## Features
- Automatically syncs the icon theme with the current accent color (Supports Adwaita and Papirus icon themes).
- Automatically syncs the cursor theme with the current accent color (Supports Oreo cursor theme).
- Automatically detects updates of **Adwaita Icons** and notifies the users to update it.
- *More to come...*

---

## 🛠 Installation  

### **Option 1: From the GNOME Extensions Website**  
[<img src="https://micheleg.github.io/dash-to-dock/media/get-it-on-ego.png" height="100">](https://extensions.gnome.org/extension/7529/auto-adwaita-colors/)

---

### **Option 2: Manual Installation**  
1. Download the latest `.zip` file from the [Release page](https://github.com/celiopy/auto-adwaita-colors/releases).  
2. Install it using the following command: 
```
gnome-extensions install --force "auto-adwaita-colors@celiopy.zip"
```

---
## 🔵 Papirus Icon Theme
[Papirus Folders](https://github.com/PapirusDevelopmentTeam/papirus-folders) is used to set the folder colors for [Papirus Icon Theme](https://github.com/PapirusDevelopmentTeam/papirus-icon-theme)

### System-wide install (Recommended):
Icon theme: ```wget -qO- https://git.io/papirus-icon-theme-install | sh```

Papirus-folders: ```wget -qO- https://git.io/papirus-folders-install | sh```

Remove password requirement for ```papirus-folders``` by adding a polkit rule:
```
cat <<EOF | sudo tee /etc/polkit-1/rules.d/10-papirus-folders.rules >/dev/null
polkit.addRule(function(action, subject) {
    if (action.id == "org.freedesktop.policykit.exec" &&
        action.lookup("program") == "/usr/bin/papirus-folders" &&
        subject.active == true && 
        subject.local == true) {
            return polkit.Result.YES;
    }
});
EOF
```

### Local install:
Icon theme: ```wget -qO- https://git.io/papirus-icon-theme-install | env DESTDIR="$HOME/.icons" sh```

Papirus-folders: ```wget -qO- https://git.io/papirus-folders-install | env PREFIX=$HOME/.local sh```

---

## ↖️ Oreo Cursor Themes
This extension also changes the [Oreo cursor theme](https://www.gnome-look.org/p/1360254) based on the accent color. You need to have the following cursors installed:
1. oreo-teal-cursors
2. oreo-purple-cursors
3. oreo-grey-cursors
4. oreo-spark-lime-cursors
5. oreo-spark-orange-cursors
6. oreo-spark-pink-cursors
7. oreo-spark-blue-cursors
8. oreo-spark-green-cursors
9. oreo-spark-red-cursors

---

## 🤝 Contributing  

Contributions are welcome!  
- Feel free to open issues for bug reports or feature requests.  
- Submit pull requests to propose improvements.  

---

## 📜 License  

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

---

## Links  
- **GitHub Repository:** [Auto Adwaita Colors](https://github.com/celiopy/auto-adwaita-colors)  
- **Adwaita-colors Icons Repository:** [Adwaita-colors](https://github.com/dpejoh/Adwaita-colors)

---

### Made with ❤️
