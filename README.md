# Linux-Practice-01
Learning how to use Linux.

Today I begin learning how to use Linux. I will begin by starting with the LabEX [Linux Journey](https://labex.io/linuxjourney).

## Topics Covered 9/5/25 
 
Day 1 covers the basics of the Linux kernal, commonly used commands, command line shortcuts, and three labs familiarizing with all of the topics.

  Below will be the notes I took during this time:

  ### Commands

  - _man_ ____: manual for any command in linux.
    * (use h to make it easier to search for options)
  - _echo_:  repeats whatever you type.
    * (also acts like print use echo ___ > ____.txt || to insert txt)
  - _expr_: calculates any expression that follows.
  - _figlet_: prints a phrase you write in ASCII characters.
  - _pwd_: prints what directory/file you are in.
  - _cd_: changes directory. Use ~ after cd to take you to home dir
  - _ls_: shows all files and directories.
    * (can use *.filetype to list all files of that type.) [* called a wildcard]
  - _mkdir_: makes a new dir(folder).
  - _touch_: makes an empty file.
  - _cat_: displays file contents.
  - _cp_: copy. Can copy files to other files.
  - _mv_: moves any file to whatever directory listed after the file.
    * ‘..’ stands for parent dir.
  - _rm_: remove file.
  - _--help_: type after a command.
    * Like man, but gives a more concise list.

### Command Line shortcuts:

  * _Tab_ > auto fills words. Use it. 
  * _Ctrl + L_ > clears the screen.

---

## Topics Covered 9/10/25 
 
Day 2 covers common file manipulation commands such as cp (copy), rm (remove), and mv (move). I reinforce these commands by interacting with them and using their respective flags.  

Below will be the notes I took during this time:

### Notes
  
- _~_: Stands for home directory.
- _Absolute Paths_: Can be used in place of directory names. Begins with root '/' and gives full location.
  * [ex: /~/home/Desktop/Directory]
- _Hidden Files_: Can be made like other files, always begin with a '.'
  * [ex: .hiddenfile]
- _ls -l_: This flag gives a long detailed list about everything in the directory.
- _cp -r_: You must use the '-r' flag when copying a directory in order to copy all of its contents over.
  * [similarly, rm shares the '-r' flag and must be used with directories]
- _mv_: Has two functions. Can both move contents over to a new name and directly rename a directory or file.
- _ll -a_: This is another way to write 'ls -la'
- _rm -i_: The '-i' flag asks for confirmation before deleting.
- _-R_: Can be used with 'ls.' Lists everything, even the subdirectories.
- _rm -rf_: This is a complete removal of data. '-r' allows for deletion of directories while '-f' forces the removal, ignoring any confirmation.

---

## Topics Covered 9/12/25 
 
Day 3 

Below will be the notes I took during this time:

### Notes

- _cat -n_: Numbers the contents of a file. Helpful for large files full of content.
- _head/tail -n#_: '-n#' can be used to list the content for only that line
- _head/tail -c#_: Displays the characters assoicated with the chosen number, up to that point, in the file.
- When using 'tail -c1,' you might return nothing. The last character may be empty, so be sure to try -c2 after.
- when making both a parent directory and subdirectory with 'mkdir,' you must use the '-p' flag and format the code as such: 'mkdir -p dir/subdir' to properly execute the command.

### Commands

  - _history_: Allows you to look at all the commands you have previously typed.
  - _whatis_: Gives a small blurb of a command.
    * Truncated 'man.'
  - _alias_: Can name certain commands to prevent repetitive typing.
    * [ex: alias foobar='ls -la']
    * can remove them by using: 'unalias.'
  - _exit_: Use exit to leave a terminal if you have no GUI.
  - _head_: Shows the first ten lines of the file.
  - _tail_: Shows the last ten lines of the file.
  - _diff_: Shows differences and changes between two files.
    * If comparing directories, make sure to use '-r' before to recursively compare.
  - _chown_: Changes ownership of a file.
    * [ex: sudo chown root:root example.txt | 'root:root' changes the 'owner:group' of the file.]
    * Use '-R' to change directory ownership.
   
    
  ### _CHMOD_: Change mode. Allows you to change permissions for a file.
    > Regarding chmod: When using: 'ls -l,' to list the details of a file, the beginning details the permissions of said file. 
    it can start with either a '-, d,' or 'l' describing what type of file it is.
    > Next you will see 'r, w,' or 'x,' or any sort of combination of them. 'r' stands for read, 'w' for write, and 'x' 
    for execute permissions. A '-' means that permission is denied.
    > The group is ordered from owner to group to public permissions. 
   - When using 'chmod,' it may look something like this: 'sudo chmod 700 example.txt'
     * The numerical position stands for the permissions. The first digit being the owner perms, the second for the group, and the last one for the public.
     * The numerical value details what kind of permissions. Each digit can be a number from 0 to 7, and is added up from four basic numbers with permissions:
       [4: Read | 2: Write | 1: Execute | 0: None ]
   - When using 'chmod' for a directory, you must use the flag '-d.'


### Command Line shortcuts:

  - _Ctrl + R_: Pretty much Up Arrow, allowing you to go back to a previous command, except this time you can search for it.

---

## Topics Covered 9/15/25 
 
Day 4 covers all common commands regarding users.

Below will be the notes I took during this time:

### Commands

  - _useradd_: Adds a user. { _-m_: adds a home directory to file.}
  - _userdel_: removes a user. {_-r_ removes all directories and mail as well.}
  - _grep_: A search function for files.
    * [To verify a user, use grep on a username and search in the '/etc/passwd' file. This houses all user creations.]
  - _passwd_: adds a password to a selected user.
    * [You can lock a user out by using 'passwd -l username' The '-u' flag reverses it.]
    * [You can use the flag '-S' to check password expiration and if the account is locked.]
  - _usermod_: Allows you to modify user account settings.
    * [using '-d /home/dir username' can allow you to change a users' directory.]
    * [using '-s /bin/bash username' changes to users' shell.]
    * [using '-aG groupname username' will change what group the user belongs to. Often used for sudo.]
  - _groups_: Checks which groups a user is apart of.
  - _su - username_: Switches your user.

---

## Topics Covered 9/17/25 
 
Day 5 simulates a jr system administrator, tasking me to overlook a linux os and consolidate my findings just like an administrator would.

Below will be the notes I took during this time:

### Notes

  - **Output Redirection:** '>' and '>>' are operators which can direct command results into files. The single arrow allows you to insert, define, and replace and info any the current file with whatever information you want. The double arrow appends, or adds data on top of what is already in the file, allowing you to add multiple command outputs into a single file.
    * [For example, I used a similar command to save all lines, with the word "ERROR," found in a log: _grep "ERROR" app.log > ~/project/error_report.txt_ ]
  - **Wildcards:** Whenever using wildcards (ex: *.log) you should always specify and use them at the end of the command.
  - You can use the pipe symbol (|) to send the output of one command into another. Very useful for 'grep.'
  - When using the 'diff' command, the order does matter in which you put them. The result will differ.

### Commands

  - _uname_: shows the name of the kernal being used.
    * ['-a' shows all system information.]
  - _uptime_: Displays how long the system has been up and running.
  - _id_: Shows your user id, group id, and what groups your user belongs to.
  - _top_: Lists all processes running, uptime, current time, CPU usage, memory usage, and tasks.
  - _tree_: Displays directory and files in a branching format. (May have to be installed)
  - _tar_: Stands for Tape Archive. Used to create, modify, and extract archived files.
    * ['-czf' is a useful flag which creates and copies over files to a new archived file.]\
  - _dmesg_: A command which displays kernal messxages such as errors and running processes.
    * [To make a search for a certain word or phrase found in these messages, use this command:
      _sudo dmesg | grep "word1|word2"_]

---

## Topics Covered 9/22/25 
 
Day 6, once again, tasks me to be a system administrator. This time, I learn to create, remove, manage, and change user accounts and their permissions. I also deal with managing group, file, and directory permissions; learning how to set group and user permissions on directories and utilizing flags to assist in directory creation.

Below will be the notes I took during this time:

### Notes

  - Reminder that for 'chmod' the values are: Read (4), Write (2), and Execute (1).
  - 'setgid' and 'setuid' follow three basic terms. A Effective User ID is an ID which grants the user its designated permissions. The Real User ID is the actual user who ran a process, marking its permissions. The last one which plays a part is the Saved User ID; a process allowing the system switch between the Real and Effective ID's. This is the inner workings behind these two permissions, allowing them to work.
  - 'adduser' and 'useradd' both add a user, but prompt you differently. 'useradd' gives you a bit more control, but you have the specify everything with flags. 'adduser' prompts you immediately after creation, allowing you to fill in passwords and other information.
  - When adding users to a group, make sure to use the flags '-a' for appending and '-G' to add a group. (Must use 'usermod')
  - After locking an account, you can check by using this command (the highlighted part is the hash for a passwd for another account):

---

![hash_photo](https://github.com/MichaelJbyte/Linux-Practice-01/blob/e9f947868e86fb1382b2a36e352bae0a4a37a3ed/linux01%20-%20passwd_hash.png)

---

### Commands (Permssions)

  - _setgid_: Not neccessarily a command, but a permission. This sets a group id to a directory, making any new files created in the directory to be automatically applied to the group the directory is associated with. This also allows a user to act and access any files in this directory as if they were apart of the designated group which owns the directory itself.
    * [Must be used with chmod.]
    * [There are two notations for this permission: symbolic = 'g+s' or numeric '2###']
  - _setuid_: similar to the 'setuid' permission, but instead works for the users.
    * [There are two notations for this permission: symbolic = 'u+s' or numeric '4###']
  - _umask_: This command does the opposite of 'chmod.' Instead of adding/changing permissions, it can remove permissions with the same numerical values. It sets a new standard.
    * [ex: umask 021]
  - _the sticky bit_: This is another permissions which sticks and locks a certain file/directory. This means only the owner may delete whichever file/directory is modified with this permission.
    * [There are two notations for this permission: symbolic = '+t' or numeric '1###']
   
---

## Topics Covered 9/24/25 
 
Day 7 covers helpful commands which can assist in discovery regarding alternate commands and options. I also note some important information to remember regarding the linux system. Lastly, I read a page about user management and some common paths I should know regarding users and groups.

Below will be the notes I took during this time:

### Notes

- **man**: Some notes about the 'man' command. Use 'up/down arrows' to navigate. Use 'spacebar/b' to page up and down. Use '/' then type after to search. Use 'n/N' to navigate your search results.
- When using the 'apropos' command, you should send the information into a 'grep' command to help identify which command you are looking for. [ex: "apropos file | grep create"]
- When a new user is created, it must be assigned to a primary group. Every other group is considered secondary. If you do not specify the primary group during creation, the system will automatically make one and title it with the username.
- '/etc/group' is where group information is stored in a linux system.
  * [An useful way to search for what groups a user is related to is by using the following command:
    cat /etc/group | grep -E "username"]
- Sudo commands and actions are logged.
- "Daemon": A program that runs as a background process.

### User Management:
- Every user has a home directory. It can be found at: '/home/username'
- _su_: To enter a root terminal, use this command.
- The '/etc/passwd' path holds user information and details such as the name, password availability(x = stored in /etc/shadow, * = no login access, ! = locked acc, " " = no passwd), UID & GID, home directory, and shell.
- The '/etc/shadow' path holds password information for users such as the name, password hash, date of last change, min/max passwd age, and expiration info(3).
- The '/etc/group' path holds group information such as group name, group passwd (usually a *), GID, and the users associated.  

### Commands

  - _type_: This command details how a different command is interpreted by the shell.
  - _apropos_: Will deliver **_all commands_** associated with whatever input you enter.
  - _sort_: Will sort output alphabetically.
    * [Often used with other commands using the pipe operator '|' ]
  - _groups_: Command which displays what groups a user is in.

---

## Topics Covered 9/26/25 
 
Day 8 covers 

Below will be the notes I took during this time:

### Notes

-

### Commands

  - 

### Command Line shortcuts:

  - 


<!-- Template

---

## Topics Covered #/#/# 
 
Day # covers 

Below will be the notes I took during this time:

### Notes

-

### Commands

  - 

### Command Line shortcuts:

  - 
-->
