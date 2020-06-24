# Tristan Nguyen's answsers
## Do you know systemd, SysVinit or Upstart?'
They are all about linux system managers.
For systemd,  I mainly use the "systemctl" command.
I didn't use SysVinit and Upstart.

## Do you know FHS? How to manage package compile?
+ FHS is about he File System structure compositions of Linux based OS.
+ For packaged compilation apps , on Debian/Ubuntu based OS, we can use SNAP, FLATPAK, APT.(LInuxBrew is also a good options).
On REDHAT/Fedora I use DNF and YUM.

## Should you clean trash in your server when change role?
It's a good pratice for cleaning the TMP/ folder , caches related things, when changing user role.
But I dont thing emptying trash Bin could help us to secure anythings.

## Do you have server naming schema? What about hostname of you server?
YES, I do the naming schema for server, it wil base on the [PRODUCT]-[COMPONENT]-[ENVIRONMENT]-[Numbering]
For hostname naming convention, I will use (Service / Product) name for the hostname.
Name lenght limits should be under 63 characters.

## How long uptime of your server? Do you update new version OS?
The uptime for server will be about 48 Hours, restart scheduled on lowest traffic timeline.
For the IoT project I have managed,the OS on server will be update regularly in 2 weeks.

## Do you use key or password for ssh, do you have policy for password?
I standarize use KEY for SSH .
For password, the Policy applied is setup with SHA256 encryption, and the it shoud be above 16 characters lenght.

## Do you use firewall on your server?
On Ubuntu, I have used UFW.

## Do you know Heartbleed, Shellshock and POODLE?
Heartbleed, Shellshock and POODLE are OpenSSL related bugs for linux based OS.
We should take care about the updating for SSL and TLS version of the web servers.

## Do you use redis or mongod? How to authentication them? What user of process mongod or redis?
Yes I have worked with redis and mongod.
### For the AUTHEN:
+ "redis" command:  AUTH [user] [password]
+ "mongod" command: db.auth((user), (password))
### For the User of the process:
+ special "mongodb" is user of mongod
+ (curent-system-user) is Redis user

## How do you deploy code to server? Do you use git pull for deployment?
I am using GIT for deployment on dev/staging/product.
Yes, I used "GIT PULL" for deployment, but found out today that is not very good pratice.
It good if we which to use the "GIT SUBMODULE UPDATE" instead when having GIt with Submodules.
