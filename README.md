# linux_cmds
1) pwd - to print current working directory
2) cd - to change directory
3) cd .. - go to parent directory
4) ls - show content of directory
5) ls -la = show all hidden contents only(directory starting with .)
6) ls --help = show help
7) mkdir = make new directory
8) touch filename.extension = make new file with defined name and extension
9) vi file_name =  visual text editor
10) to exit from vim without saving = esc, :, q!
11) to exit from vim with saving = esc,:,wq
12) vi = get help related to vim editor
13) ls --help
14) chmod +x myfile.py = make myfile.py executable
15) chmod  <groups to assign the permissions><permissions to assign/remove> <file/folder names>
16) mv <file/folder we want to move> <destination>
17) mv ~/catkin_ws/src/linux_course_files/my_scripts ~/catkin_ws/src/linux_course_files/move_bb8_pkg
18) cp <file/folder we want to copy> <name of the new file/folder> = to copy file
19) cp -r my_scripts/ my_scripts_copy/ = to copy folder
20) rm <file to remove> =  to delete file
21) rm -r my_scripts_copy =  to delete folder
22) ls -la = tells about permission of files in the folder
 23) | grep can be used with any other command
  24) htop & top task manager for linux
  25) ps faux similar to htop
  
##  Arguments can be passed to the shell script example is as follows
Bash script starts here>>>>>>  
 ```bash
#!/bin/bash

ARG1=$1

if [ $ARG1 == 'forward' ]; then
    rostopic pub /cmd_vel geometry_msgs/Twist "linear:
  x: -0.1
  y: 0.0
  z: 0.0
angular:
  x: 0.0
  y: 0.0
  z: 0.0"

elif [ $ARG1 == 'rotate' ]; then
    rostopic pub /cmd_vel geometry_msgs/Twist "linear:
  x: 0.0
  y: 0.0
  z: 0.0
angular:
  x: 0.0
  y: 0.0
  z: 0.2"

elif [ $ARG1 == 'stop' ]; then
    rostopic pub /cmd_vel geometry_msgs/Twist "linear:
  x: 0.0
  y: 0.0
  z: 0.0
angular:
  x: 0.0
  y: 0.0
  z: 0.0"
fi
   ```
 <<<<Bash script ends here
  
   You can access an argument inside a script using the variables $1, $2, $3, and so on. The variable $1 refers to the first argument, $2 to the second argument, and $3 to the third argument. So, in this case, since we only have 1 argument, we access it using the variable $1.
   the value of the argument is assgined to the variable $ARG1
  
  
  
 ##If condition in bash format
   ```bash
  if CONDITION
then
  COMMANDS
fi
  ```
  
  The .bashrc file is a special bash script, which Linux executes whenever a new Shell session is initialized.
  
  In simple terms, environment variables are set when you open a new shell session. at any time if you change any of the variable values, the shell has no way of picking that change. The export command, on the other hand, provides the ability to update the current shell session about the change you made to the exported variable. You don’t have to wait until new shell session to use the value of the variable you changed.
 
 
## To kill some process
 
 ![image](https://user-images.githubusercontent.com/40294372/216338864-150fab1b-e1ee-4321-a955-ec9a1251f340.png)
 
Syntax 
 ```bash
 kill SIGNAL PID
  ```

