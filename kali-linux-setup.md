# Kali Linux Setup

### Login with the username root and the default password toor

### Open a Terminal

### Change Password

> Always important to change the root password, especially if you enable SSH services.

###    Update Image with the Command

```bash
> apt-get update
> apt-get dist-upgrade
```

### Setup database for Metasploit

* This is to configure Metasploit to use a database for stored results and indexing the modules.
* `service postgresql start`
* `service Metasploit start`

### Optional for Metasploit - Enable Logging

```bash
echo “spool/root/msf_console.log” >/root/.msf4/msfconsole.rc
```

* Logs will be stored at/root/msf\_console.log

### Install Discover Scripts \(originally called Backtrack-scripts\)

 - Discover is used for Passive Enumeration 

```bash
> cd/opt/
> git clone https://github.com/leebaird/discover.git
> cd discover/
> ./setup.sh
```

### Install Smbexec

```bash
> cd/opt/
> git clone https://github.com/brav0hax/smbexec.git
> cd smbexec
> ./install.sh
```

### Adding Nmap script

> The banner-plus.nse will be used for quicker scanning and smarter identification

```bash
> cd/usr/share/nmap/scripts/
> wget https://raw.github.com/hdm/scan-tools/master/nse/banner-plus.nse
```

### Installing PowerSploit

> PowerSploit are PowerShell scripts for post exploitation

```bash
> cd/opt/
> git clone https://github.com/mattifestation/PowerSploit.git
> cd PowerSploit
> wget https://raw.github.com/obscuresec/random/master/StartListener.py
> wget https://raw.github.com/darkoperator/powershell_scripts/master/ps_encoder.py
```





