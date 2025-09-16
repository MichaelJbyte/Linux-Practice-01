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
