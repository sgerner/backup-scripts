# backup-scripts
Bash scripts to automate backups for various different server configurations

# Backup Website and Database to remote Cloud Provider
Use the backup-webdir+database script
This script is a quick and easy way to backup a single directory and MySQL or MariaDB database. It was largely created as an easy way to backup a Ghost Blog. The script dumps a copy of the current database, archives the directory and database dump into a tar.gz, and then backups up those archives periodically to a remote server. The script then cleans up old archives. I recommend setting a cron job to run the script daily.

[View setup guide](https://github.com/sgerner/backup-scripts/wiki/Setup-Guide-for-backup-webdir-database)