1 - Enumerate ports

2 - Enumerate possible web things like: cookies, subdomains, directories and files

3 - Once you've listed the subdomains add to your `/etc/hosts` the page `artcorp.htb` and `dev01.artcorp.htb` in order to have full access to the page

4 - Now go to `dev01.artcorp.htb` and you'll see a simple page that, using exiftool, gives you all the metadata of a certain image you upload. You can take advantage of this feature by employing a simple exploit that enables you to do a RCE. This RCE can be done as explained in [Exiftool](</General Info/Tools/Exiftool.md>)

5 - Now that you should've gained a reverse shell as www-data you need to pivot to the `thomas` user in order gain the user flag and have the possibility to get into the root user

6 - Once you've gone through all the [Things to enumerate (Machine)](</General Info/Enumeration/Things to enumerate (Machine).md>) you'll find a process that makes a call to the `mogrify` file located in `/usr/local/bin`, you can type `file mogrify` and later on type `magick` or simply just type `mogrify` in order to know that you're facing an Imagemagick app

7 - The main approach to hack this kind of tools can be seen in [ImageTragick](</General Info/Tecnologias Web/Imagemagick.md>)

8 - Now that you've exploited the app via .SVG file in order to get a reverse shell you can go on an enumerate the system as explained in [Things to enumerate (Machine)](</General Info/Enumeration/Things to enumerate (Machine).md>)

9 - Once you've run the `sudo -l` command you'll see two interesting things:
- One is the condition `env_keep+=XDG_CONFIG_HOME` explained in [Sudo](</General Info/Linux commands/Sudo>)
- The second one is that the user thomas can run neofetch as root without password

10 - This being said you can go directly to GTFOBins and learn how to exploit the neofetch with SUDO. Steps to do it:
- Trying to recognize what GTFOBins is doing you will realize that we can't do that because we can't add flags, so, we've to kinda do the same but with some changes.
- The first step would be to change the `XDG_CONFIG_HOME` env variable in order to make root execute neobins with our config file located in `~/.config` or `/home/thomas/.config`, this is a must because, unlike GTFOBins, we can't specify a config file, so we've to make the default config file path change via the env variable
- Now that we've the env variable changed making neobins tool being run with our own config, we can change the config file located in `~/.config/neofetch/config.conf` adding `chmod u+s /bin/bash` to one of the first lines in order to add the SUID permisson to the bash tool
- Lastly you've to run `bash -p` in order to run bash with root privileges and cat out the root flag located in `/root/root.txt`