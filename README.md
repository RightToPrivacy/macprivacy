Disable/Enable randomly changing mac addresses at random continuously changing time intervals:

simply make sure anonsurf has CHANGING_MAC variable set to 'yes' to enable mac/hostname changing feature. Set CHANGING_MAC variable to 'no' to disable feature and it will disregard entire process. It stops the process in the stop function and starts with start function when enabled.

I also added (completely optional- read below) ability to run macpriv as a daemon/systemd service.

macprivacy install as command: simply follow run make and skip the rest of below

Add as systemd service (keep anonsurf w/optional mac changing/hostname changing running all the time): -=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-

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

As mentioned, this package alone lets you run anonsurf as simply a command just by skipping all systemctl commands. If you need help email me below:

Contact: righttoprivacy@tutanota.com or @righttoprivacy on the Parrot Forums
