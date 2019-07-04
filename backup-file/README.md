# ansible-backup-files
Ansible task for applying prometheus values updates (or performing some shell task) and backing up values outside of helm chart directory or other file)

It is not abundantly clear how to backup up a file with Ansible, nor is it clear how to move that ansible created backup file to another directory.  I hope that I have provided a clear solution in the tasks/main.yml.  

The main issue is allowing ansbile to create it's own version of backup_file, then you register that new timestamped filename as a new variable that you control.  Then to move that backup file you'll add another step to allow the shell module to move the file (filename which is was captured by your variable register) to whatever directory you need on the target host.
