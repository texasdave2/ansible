# ansible
These are a few of the ansible projects that I was involved in either creating or helping to create.

The ansible 'backup files' directory is a handy way to let ansible safely backup a yaml file for a helm chart with reversion using ansible's built in timestamping format.  Once the file is backed up outside of the helm chart, the prometheus instance is restarted so the new values will take hold.

The non-idm-user-management files are handy to manage users with ansible for hosts that aren't controlled by IDM.  This allows the admin to easily and safely pull users in and out of priviledged groups as well as allowing them whitelisted kubectl commands in the sudoers file for higher environments where a user needs some specific privileges.

