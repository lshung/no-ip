# No-IP DUC
This simple Bash shell script works as Dynamic Update Client (DUC) for No-IP DDNS.

## Setup
1. Clone this repo to your disk
2. Change directory (*cd* command) to the cloned repo
3. Run command *`bash setup`*
4. Enter your No-IP username, password and hostname

## What the setup process does
1. The setup process will automatically save your username, password and hostname in a file named *.config*. You can also create your own file *.config* manually, which follows the format:
```
username=your_no_ip_username
password=your_no_ip_password
hostname=your_no_ip_hostname
```
2. Set file permissions properly (for *.config* and *update*)
3. Create a symlink named *__noipupdate__*, which is located in your *$HOME/bin*
4. Add a cron job, which runs every 5 minutes

## How to use
If you follow the setup process above, the program will update your IP every 5 minutes and you have to do nothing more.

In case you want to update your IP manually, run command: *`noipupdate`*
