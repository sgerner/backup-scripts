# backup-scripts
Bash scripts to automate backups for various different server configurations

# Backup Website and Database to remote Cloud Provider
Use the backup-webdir+database script for a quick and easy way to backup a single directory and MySQL or MariaDB database. It was largely created as an easy way to backup a Ghost Blog. The script dumps a copy of the current database, archives the directory and database dump into a tar.gz, and then backups up those archives periodically to a remote server. The script then cleans up old archives. I recommend setting a cron job to run the script daily.

[View setup guide](https://github.com/sgerner/backup-scripts/wiki/Setup-Guide-for-backup-webdir-database)

# Backup website, server configuration, and database to cloud daily with periodic archives.
This guide is for the hybrid-current+archive script. It is a minor extension of backup-webdir+database that adds support for multiple directories and continuous file system backup, in addition to the archive snapshots in the other script.

This script will dump a MySQL / MariaDB database and backup several directories to a remote location each time the script is run. It will also create an archival snapshot of the monitored directories and database, periodically upload them to a cloud provider, and prune excess archives. My idea was to provide a daily real-time copy of our company website and ordering platform, associated database, and server configuration files to allow easy restoration in case something catastrophic happened to our server hardware. I also wanted periodic snapshots in case we messed up anything on the server and need to roll back.

[View setup guide](https://github.com/sgerner/backup-scripts/wiki/Setup-Guide-for-hybrid-current-archive)

# Backup Directories Upon WiFi Connect over SSH
Use ssh-backup-on-wifi script for an automated way to backup directories on a local machine to a remote machine over SSH when your local machine connects to a specific WiFi network. Basically, I wanted an easy way to backup my laptop to my home server each night when I connected to the home wifi network.

[View setup guide](https://github.com/sgerner/backup-scripts/wiki/Setup-Guide-for-ssh-backup-on-wifi)
