These are come files to try to make the setup of my pis faster, atm installing eduroam is a pain and I can't do anything without wifi, so hopefully this streamlines the process  
Clone the repo outside of the boot and then copy and paste the files into the boot partition, also make sure to change your eduroam username and password accordingly  

WIFI SETUP:
Okie so first copy the wpa_supplicant and make wpa_supplicant-wlan0.conf and then update username and password
Then with certs in the boot folder, move that to the /etc/ssl/certs/ folder
Some useful commands:
sudo wpa_cli -i wlan0 status
sudo systemctl restart dhcpcd
ip addr show wlan0
sudo systemctl status wpa_supplicant@wlan0
sudo systemctl restart wpa_supplicant@wlan0
sudo systemctl enable wpa_supplicant@wlan0
sudo systemctl restart wpa_supplicant@wlan0
