## Mini Project in Shell Scripting
### Display information of User and System by using Shell Script Commands

- Create a file with command 'vim filename.sh'. It will create a file if it doesnt exist, else if it exists, it will open automatically.
- Press 'i' to go in insert mode.

> **NOTE - For better understanding, please do not copy paste the code. Type everything in editor.**

Code for project

    #!/bin/bash
    echo "~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~"
    echo ""
    echo "You are Welcome $1 - You are currently in $HOME"
    echo""
    echo "-------------------------------------------------------------"
    echo ""
    echo "Today is $(date | awk '{print $1,$2,$3}') and the time is $(date | awk '{print $4,$5}')"
    echo ""
    echo "============================================================="
    echo ""
    echo "The Uptime of system is:-"
    echo "$(uptime)"
    echo "You are currently using:- $(who -H | xargs | awk '{print $5}')"
    echo""
    echo "Last logins:"
    last -a | head -3
    echo ""
    echo "----------------------------------------------------------"
    echo ""
    echo "Last logged-in at:- $(uptime | xargs | awk '{print $1}') since $(uptime | xargs | awk '{print $3}') hours"
    echo "============================================================="
    echo ""
    echo "Free Disk Space on your system:- $(df -H | xargs | awk '{print "Free Space/Total Disk Space: "$10"/"$9}')"
    echo "-------------------------------------------------------------"
    echo ""
    echo "Free RAM available in system:- $(free -h | xargs | awk '{print "Free Memory/Total Memory: " $10"/"$13}')"
    echo "============================================================="
    echo ""
    top -b | head -3

- To come out of insert mode, press Esc key.
- Type ':wq' and press enter to save and quit from Vim editor
- Now, make the file executable by giving it permission to execute. 
- The command is *chmod 700 filename.sh*. Make sure the file is given executable permission by checking with *ls -la*
- To run the file, type *./filename.sh*

> Make sure you are in the current directory while running these commands.

## Happy Learning !!!
