# fedora-virtmgr-setup
HOWTO Easily get going with Virt-Manager on Fedora

# Run the following
1. In a terminal, `sudo dnf install @virtualization` [ENTER]
2. `sudo nano /etc/libvirt/libvirtd.conf` [ENTER] and Ctrl+W to find `unix_sock_group = "libvirt"` and enable it
3. Find and enable `unix_sock_rw_perms = "0770"` and save the document and exit back to the terminal
4. Run the following: `sudo systemctl start libvirtd & sudo systemctl enable libvirtd` [ENTER]
5. Type: `sudo usermod -a -G libvirt $(whoami)` [ENTER]
6. In terminal (`virt-manager` [ENTER]) or in Gnome/KDE search for virtual manager
