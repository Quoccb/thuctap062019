### top
The top command is the traditional way to view your system’s resource usage and see the processes that are taking up the most system resources. Top displays a list of processes, with the ones using the most CPU at the top.
<img src=https://www.howtogeek.com/wp-content/uploads/2012/03/xtop.png.pagespeed.gp+jp+jw+pj+ws+js+rj+rp+rw+ri+cp+md.ic.b5G8p2Z1Tv.png>

To exit top or htop, use the Ctrl-C keyboard shortcut. This keyboard shortcut usually kills the currently running process in the terminal.

### htop
The htop command is an improved top. It’s not installed by default on most Linux distributions — here’s the command you’ll need to install it on Ubuntu:

>sudo apt-get install htop

<img src=https://www.howtogeek.com/wp-content/uploads/2012/03/htop.png.pagespeed.ce.5LKyJezJyp.png>

htop displays the same information with an easier-to-understand layout. It also lets you select processes with the arrow keys and perform actions, such as killing them or changing their priority, with the F keys.

We’ve covered htop in more detail in the past.

### ps
The ps command lists running processes. The following command lists all processes running on your system:

>ps -A

<img src=https://www.howtogeek.com/wp-content/uploads/2012/03/xps-a.png.pagespeed.gp+jp+jw+pj+ws+js+rj+rp+rw+ri+cp+md.ic.wLiZSAtxHj.png>

This may be too many processes to read at one time, so you can pipe the output through the less command to scroll through them at your own pace:

>ps -A | less

Press q to exit when you’re done.

You could also pipe the output through grep to search for a specific process without using any other commands. The following command would search for the Firefox process:

>ps -A | grep firefox

<img src=https://www.howtogeek.com/wp-content/uploads/2012/03/ps-a-grep.png.pagespeed.ce.lYkEcmr88h.png>

### pstree
The pstree command is another way of visualizing processes. It displays them in tree format. So, for example, your X server and graphical environment would appear under the display manager that spawned them.

<img src=https://www.howtogeek.com/wp-content/uploads/2012/03/xpstree.png.pagespeed.gp+jp+jw+pj+ws+js+rj+rp+rw+ri+cp+md.ic.aocfoNta0h.png>

kill
The kill command can kill a process, given its process ID. You can get this information from the ps -A, top or pgrep commands.

>kill PID

<img src=https://www.howtogeek.com/wp-content/uploads/2012/03/kill.png.pagespeed.ce._ALgvWrJWZ.png>

Technically speaking, the kill command can send any signal to a process. You can use kill -KILL or kill -9 instead to kill a stubborn process.

pgrep
Given a search term, pgrep returns the process IDs that match it. For example, you could use the following command to find Firefox’s PID:

>pgrep firefox

<img src=https://www.howtogeek.com/wp-content/uploads/2012/03/pgrep.png.pagespeed.ce.4XIoXohRjb.png>

You can also combine this command with kill to kill a specific process. Using pkill or killall is simpler, though.
