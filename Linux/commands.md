
#### Must know Linux Commands for Devops ####

#### Symbols Section ####

1. ```~``` represents current users home direcotry
2. ```|``` represents piping operation on commands
3. ```$``` # represents normal user shell
4. ```#``` # represents root users shell 
5. ```/``` # when used in cd command like `cd /` will change directory to  root of file system
6. ```>``` output redirection
7. ```>>``` append mode output rediretion
8. ```1>>, 2>>, &>>``` std, error, std and error ouput
9. ```<``` input redirection
10. ```*``` wildcard charachter to get everything

#### Types of Files ####
1. ```-```, represents regular text file
2. ```c```, represents i/o handling files
3. ```l``` , represents a shortcut file
4. ```d```, represents the current file is a directory
5. ```s```, special file that provides interprocess networking
6. ```p```, file to communicate among processes without network semantics

#### Permissions ####
1. ```- --- --- ---```, first hypen represents filetype, first group of hypens user permissions, second group of hypens is for group permissions and last one is permissions for others
2. in ```---``` these three dashes first is read, second is write and last one is for execute.
3. r is assigned a number of 4, w is assigned a number of 2 and x is assigned a value of 1 based on these we can calculate numeric permissions like ```755```

#### Commands Section ####

| Title | Description | Examples |
|:------------ |:--------------:| -------------:|
| whoami or who | used to know the user know of currently logged in user | ```$> whoami or who``` |
| pwd | used to know current direcotry path | ```$> pwd``` |
| ls | list down contents of a direcotry | ```$> ls```, ```$> ls -ltrd``` sort by timestamp in descending order only directories |  
| cat | to read contents of a source (file, stream) | ```$> cat file.txt``` |
| head | to read first n lines from source | ```$> head -n 10  file.txt```  |
| tail | to read last n lines from source | ```$> tail -n 10  file.txt```, ```$> tail -f file.txt``` open file inmonitoring mode to see live file changes i.e log files  |
| sudo | uplift status from normal user to root user | ```$> sudo -i``` |
| cd | to change working direcotry | ```$> cd```, ```$> cd /path``` |
| clear | to clear out the console/shell | ```$> clear``` |
| mkdir | to create directory on given path | ```$> mkdir dev stage production```, ```$> mkdir directory{1..10}```, ```$> mkdir -p /nested/path/that/does/not/exist``` |
| cp | to copy source to destination path | ```$> cp dev/Dockerfile stage/```, ```$> cp -r dev backupdir/```, ```cp *.txt content/```| 
| mv | to move source to destination path | ```$> mv dev/Dockerfile stage/```, ```$> mv dev backupdir/```, ```mv *.txt content/``` |
| touch | to create a file with given filename | ```$> touch file{1..10}.txt``` |
| exit | to exit out of current user shell | ```$> exit```  |
| rm | to remove a file or directory | ```$> rm data.txt```, ```$> rm -r backupdir/``` |
| history | to check history of executed commands | ```$> history```, ```$> history 10``` last 10 executed commands |
| file | to check information of a file | ```$> file /bin/pwd``` |
| ln | to create link/shortcuts for files/commands | ```$> ln -s /bin/pwd p``` |
| grep | to search data from file | ```$> grep -i searchtext < file.txt```, ```$> grep -iR searchtext *``` recursively search |
| less | to read through a file, supports up/down arrow keys and search | ```$> less file.txt``` |
| more | to read through a file in % manner | ```$> more file.txt``` |
| cut | to parse information on delimited/formatted file| ```$> cut -d: -f1 /etc/passwd``` |
| awk | for advanced filtering and text manipulation |```$> awk -F':' '{print $1}' file.txt``` |
| sed | to manipulate a text file i.e search replace remove content from file | ```$> sed -i 's/searchtext/replacetext/g' < file.txt``` |
| free | to see available free memory | ```$> free -h``` |
| df | to see hard disk paritioning | ```$> df -h``` |
| uptime | to see current uptime | ```$> uptime``` |
| echo | to display content | ```$> echo "$1 is cool"``` |
| printenv | to display all available shell variables| ```$> printenv``` |
| date | to see cureent datetime | ```$> date``` |
| wc | to count word/lines in file | ```$> wc -l``` |
| find | to search for files | ```$> find .``` |
| updatedb | to update db for locate package | ```$> locate``` |
| locate | to search for a file  | ```$> locate file``` |
| id | to see uid, gid another user info | ```$> id root``` |
| useradd/adduser | to add a user | ```$> (useradd/adduser username``` |
| groupadd | to adda user group | ```$> groupadd groupname``` |
| usermod | to update a userinfo | ```$> usermod -aG/g groupname username```, G for secondary group and g for primary group |
| passwd | to update the password of a user | ```$> passwd username``` |
| last | to see list of las login of user| ```$> last``` |
| lsof | to see opened file by a user | ```$> lsof -u username``` |
| userdel | to delete a user | ```$> deluser -r username``` |
| groupdel | to delete a group | ```$> groupdel groupname``` |
| chmod | to update file permissions | ```$> chmod -R (+/-)(w/r/x) filename``` |
| visudo | to update sudoers file | ```$> visudo``` |
| systemctl | to start/stop/restart/reload/enable/is-active/is-enabled and check status of serives | ```$> systemctl (start/stop/status/restart/reload/enable/is-active/is-enabled) servicename``` |
| ps | to check all running processes | ```$> ps aux``` |
| kill | to kill a process | ```$> kill (-9) process-id``` |
| tree | to show a dir as tree view | ```$> tree directory``` |
| xargs | to pass multiple args to a command | ```$> ps aux \| grep 'httpd' \| xargs kill -9 ``` |
| tar | to create/extract tar balls | ```$> tar -(cx)zvf filename``` |