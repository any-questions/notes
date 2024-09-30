Ctrl+Alt+T -> Open terminal

Time:
Open a terminal and type the following command to see what time zone your Raspberry Pi is currently configured for.

$ timedatectl

List available time zones with the following command. Pick one relevant to your location, and we’ll configure your system to that time zone in the next step.

$ timedatectl list-timezones

Once you’ve picked the correct time zone from the list, use the following syntax to set your system’s time zone.

$ sudo timedatectl set-timezone Australia/Sydney

To turn time synchronization on or off, use the respective command below.

$ sudo timedatectl set-ntp on
OR
$ sudo timedatectl set-ntp off

If you’d like to set the system clock to some arbitrary date and time, ensure that time synchronization is off (as we’ve shown in the previous step) and use the following `date` command. This command will set the date and time to `10 January 2021, 12:00 PM`, but substitute any values you want.

$ sudo date -s "10 JAN 2021 12:00:00"