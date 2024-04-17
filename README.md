# samba_install

sudo apt-get install samba

Change [global]

Configure /etc/samba/smb.conf   (nano /etc/samba/smb.conf)

workgroup = windows-workgroup-or-domain-name

security = user
 
 OR
 
 Create [share]

Configure /etc/samba/smb.conf


comment = Ubuntu File Server Share

path = /path/to/share/Alagesan     (which location do you want)

browsable = yes

writeable = yes

guest ok = yes

read only = no

valid user = Alagesan

create mask = 0755

Then save it and close


Create Shared Directory

sudo mkdir -p /path/to/share

sudo chown nobody.nogroup /path/to/share


Restart Samba Server

sudo restart smbd

sudo restart nmbd

Create Samba Client Account

sudo smbpasswd -a Alagesan

sudo mkdir /path/to/share/Alagesan

sudo chown alagesan:alagesan /path/to/share/Alagesan

Done!!!



OPEN WINDOWS MECHINE AND PUT LINUX IPADDRESS ENTER PASSWORD AND ENJOY!!!!!
