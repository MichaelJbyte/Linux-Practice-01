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

## Topics Covered 9/8/25 
 
Day 2 covers common file manipulation commands such as cp (copy), rm (remove), and mv (move). I reinforce these commands by interacting with them and using their respective flags.  

Below will be the notes I took during this time:

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
