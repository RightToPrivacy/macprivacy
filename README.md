# USE: Security/Privacy

Randomly change mac addresses/hostname at random continuously changing time intervals,
randomly chosen, continually changing mac address & is given a randomly chosen generic hostname 
on each mac address change:

To run as stand alone:
put OUI.final into /root/OUI.final (or whereever you set oui_file variable in macpriv script)
chmod +x macpriv
sudo ./macpriv

macprivacy install as command: 
move macpriv to /usr/bin/macpriv
chmod +x macpriv
sudo macpriv

Add as (optional) systemd service (continually changing mac changing/hostname changing running all the time): -=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-

1.) move OUI.final file to /root/OUI.final (or wherever you set $oui_file variable to)

2.) move macpriv to /usr/bin/macpriv 

3.) chmod +x /usr/bin/macpriv

4.) move macpriv.service to /etc/systemd/system/macpriv.service

5.) after first 4 steps run following as root if you want to activate an macpriv.service systemd:

systemctl daemon-reload

systemctl enable macpriv.service

systemctl start macpriv.service

then to stop it as service just enter:

systemctl stop macpriv.service

To restart as service:

systemctl restart macpriv.service

As mentioned, this package alone lets you run macpriv as a command or an at boot
systemd service for constant mac address/hostname privacy. If you need help email me below:

Contact: righttoprivacy@tutanota.com or @righttoprivacy on the Parrot Forums
