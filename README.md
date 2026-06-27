For TrueNAS Scale 24.10 Electric Eel and newer

Login to your Truenas Scale box
- go to Apps -> Discover Apps
- in the top right beside Custom App click the 3 dots ... and click Install via YAML
- Name: ps3netsrv (or whatever you want really)
- Custom Config: the contents of docker-compose-truenas.yml modified for your pools and file locations

I am an amateur but I did what I could to make this container setup and boot quickly and got it down to about 5 seconds on my truenas system, which is a pretty old Dell server

The volumes section is becuase I already have my games organized a folder structure and do not want to have to make copies of them to use with ps3netsrv and I don't want to deal with symlinks
Simply commend out any you are not using, only the base folder is required, and if you are not remapping other folders to it you must create PS3ISO and GAMES folders in it before booting the container
