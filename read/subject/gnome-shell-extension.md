---
title: 擴充套件
nav_order: 5020
has_children: true
---


# 擴充套件




## 主題

* [擴充套件管理工具](https://samwhelp.github.io/note-about-ubuntu-gnome-shell/read/subject/gnome-shell-extension-management-tool.html)
* [統整列表](#統整列表)
* [相關專案](#相關專案)
* [相關連結](#相關連結)




## 統整列表

> Gnome Shell Extension

| Gnome Shell Extension | Source | Info |
| --------------------- | ------ | ---- |
| [blur-my-shell@aunetx](https://extensions.gnome.org/extension/3193/blur-my-shell/) | [Source](https://github.com/aunetx/blur-my-shell) | Info |
| [arcmenu@arcmenu.com](https://extensions.gnome.org/extension/3628/arcmenu/) | [Source](https://gitlab.com/arcmenu/ArcMenu) | Info |
| [dash-to-panel@jderose9.github.com](https://extensions.gnome.org/extension/1160/dash-to-panel/) | [Source](https://github.com/home-sweet-gnome/dash-to-panel) | Info |
| [dash-to-dock@micxgx.gmail.com](https://extensions.gnome.org/extension/307/dash-to-dock/) | [Source](https://github.com/micheleg/dash-to-dock) | Info |
| [date-menu-formatter@marcinjakubowski.github.com](https://extensions.gnome.org/extension/4655/date-menu-formatter/) | [Source](https://github.com/marcinjakubowski/date-menu-formatter) | [Info](https://samwhelp.github.io/note-about-ubuntu-gnome-shell/read/subject/gnome-shell-extension/date-menu-formatter.html) |
| [ding@rastersoft.com](https://extensions.gnome.org/extension/2087/desktop-icons-ng-ding/) | [Source](https://gitlab.com/rastersoft/desktop-icons-ng) | Info |




| Gnome Shell Extension | Source |
| --------------------- | ------ |
| [custom-hot-corners-extended@G-dH.github.com](https://extensions.gnome.org/extension/4167/custom-hot-corners-extended/) | [Source](https://github.com/G-dH/custom-hot-corners-extended) |




| Gnome Shell Extension | Source |
| --------------------- | ------ |
| [dash-to-plank@hardpixel.eu](https://extensions.gnome.org/extension/4198/dash-to-plank/) | [Source](https://github.com/hardpixel/dash-to-plank) |
| `shell-export-dbus-portal@localhost.home` | [Source](https://github.com/samwhelp/demo-gnome-shell-extension-export-dbus-portal) |
| `unsafe-mode-menu@linushdot.local` | [Source](https://github.com/linushdot/unsafe-mode-menu) |



| Gnome Shell Extension | Source |
| --------------------- | ------ |
| [appindicatorsupport@rgcjonas.gmail.com](https://extensions.gnome.org/extension/615/appindicator-support/) | [Source](https://github.com/ubuntu/gnome-shell-extension-appindicator) |
| [ubuntu-appindicators@ubuntu.com](https://extensions.gnome.org/extension/1301/ubuntu-appindicators/) | [Source](https://github.com/ubuntu/gnome-shell-extension-appindicator) |




| Ubuntu Packages |
| --------------- |
| [gnome-shell-ubuntu-extensions](https://packages.ubuntu.com/questing/gnome-shell-ubuntu-extensions) |
| [gnome-shell-extension-appindicator](https://packages.ubuntu.com/resolute/gnome-shell-extension-appindicator) |
| [gnome-shell-extension-desktop-icons-ng](https://packages.ubuntu.com/resolute/gnome-shell-extension-desktop-icons-ng) |
| [gnome-shell-extension-ubuntu-dock](https://packages.ubuntu.com/resolute/gnome-shell-extension-ubuntu-dock) |
| [gnome-shell-extension-ubuntu-tiling-assistant](https://packages.ubuntu.com/resolute/gnome-shell-extension-ubuntu-tiling-assistant) |




run to view [ubuntu-session](https://packages.ubuntu.com/resolute/ubuntu-session) Depends:

``` sh
apt-cache show ubuntu-session | grep '^Depends:'
```

show

```
Depends: gnome-session-bin (<< 51~), gnome-session-bin (>= 50.1-0ubuntu0.1), gnome-session-common (= 50.1-0ubuntu0.1), gnome-settings-daemon (>= 3.37.0), gnome-shell (>= 50~), gnome-shell-ubuntu-extensions, xdg-desktop-portal-gnome, xwayland, yaru-theme-gnome-shell (>= 20.04.3~), user-session-migration
Depends: gnome-session-bin (<< 51~), gnome-session-bin (>= 50.0-0ubuntu3), gnome-session-common (= 50.0-0ubuntu3), gnome-settings-daemon (>= 3.37.0), gnome-shell (>= 50~), xdg-desktop-portal-gnome, xwayland, yaru-theme-gnome-shell (>= 20.04.3~), user-session-migration
```




## 相關專案

| Gnome Shell Layout |
| ------------------ |
| [make-gnome-shell-layout-wincity](https://github.com/samwhelp/make-gnome-shell-layout-wincity) |
| [make-gnome-shell-layout-maccity](https://github.com/samwhelp/make-gnome-shell-layout-maccity) |




## 相關連結

| 相關連結 |
| ------- |
| [Gnome Shell Extensions](https://extensions.gnome.org/) |


| GitLab |
| ------ |
| [gnome-shell](https://gitlab.gnome.org/GNOME/gnome-shell) |
| [gnome-shell-extensions](https://gitlab.gnome.org/GNOME/gnome-shell-extensions) |


| GitHub |
| ------ |
| [gnome-shell](https://github.com/GNOME/gnome-shell) |
| [gnome-shell-extensions](https://github.com/GNOME/gnome-shell-extensions) |


| GJS |
| --- |
| [https://gjs.guide/](https://gjs.guide/) |
| [https://gjs-docs.gnome.org/](https://gjs-docs.gnome.org/) |


| Link |
| ---- |
| [gnome-shell-enhance](https://github.com/samwhelp/gnome-shell-enhance) |
