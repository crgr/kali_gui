# kali_gui
Ansible role to set a GUI on the Kali headless Ludus template

By default, the role installs only the minimal Sway stack + foot.
If a user enables `kali_install_wayvnc: true`, the role also deploys the service and script.
noVNC is only installed and started if `kali_install_novnc: true`.
Users can install neither, either, or both browsers (firefox-esr and/or google-chrome-stable), and optionally add WezTerm alongside foot.
If you want Burp to work, you very likely want: `kali_install_xwayland: true`

Disk space needed:

sway waybar wofi                       Space needed: 339 MB
sway waybar wofi wayvnc                Space needed: 522 MB
sway waybar wofi wayvnc novnc          Space needed: 715 MB
sway waybar wofi wayvnc novnc xwayland Space needed: 727 MB
sway waybar wofi firefox-esr           Space needed: 620 MB
