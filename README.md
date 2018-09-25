# backup-scripts
Bash scripts to automate backups for various different server configurations

# Backup Website and Database to remote Cloud Provider
Use the backup-webdir+database script for a quick and easy way to backup a single directory and MySQL or MariaDB database. It was largely created as an easy way to backup a Ghost Blog. The script dumps a copy of the current database, archives the directory and database dump into a tar.gz, and then backups up those archives periodically to a remote server. The script then cleans up old archives. I recommend setting a cron job to run the script daily.

[View setup guide](https://github.com/sgerner/backup-scripts/wiki/Setup-Guide-for-backup-webdir-database)

# Backup Directories Upon WiFi Connect over SSH
Use ssh-backup-on-wifi script for an automated way to backup directories on a local machine to a remote machine over SSH when your local machine connects to a specific WiFi network. Basically, I wanted an easy way to backup my laptop to my home server each night when I connected to the home wifi network.

[View setup guide](https://github.com/sgerner/backup-scripts/wiki/Setup-Guide-for-ssh-backup-on-wifi)