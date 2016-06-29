---
layout: post
title:  "Basics of shell for Gnu/Linux based OS"
date:   2015-10-09 12:57:14 +0530
categories: Technical
author: devux@devakumar.mj
---
This blog is for the person who are all new to GNU/Linux based operating and not only for them I will explain some magical powerful code which normal GNU/Linux based OS

# What I felt !
After Installation of GNU/Linux based Operating System(OS) I don’t know how to operate the system? how to access the application?<br/>
Now got the answer? If you know how to use console then you will automatically a friend of OS.

I know all can have the same Peelings(feelings) so here after don’t worry :p  I’m gonna teach you how to make your GNU/Linux OS as your friend.How it is possible to have friendship with OS? yes there is an application program called Linux console(Terminal) which allow you to speak with OS(useful for input and output operation) and to make your kernel as friend.

# How to work with console?
Using shell commands. yes it pretty simple You just open your console and enter shell commands

# Shell
Shell is the program that takes command from the keyboard and interact with kernel

here is How we normally do?

* My computer-> Double click-> next->next->next

# How can we do in(via shell command)
I’m gonna explain some of the shell command to talk with your OS
Lets type something in console  `Devux`  and hit enter

![Screenshot from my machine](/images/screenshot-from-2015-06-29-224421.png)
it show command not found. yes have some default commands to execute in terminal we can’t any string but don’t question me only we can able to create default one? we cannot create new one like that???

yeah, we can create a new command that we will see later

#Basic commands

# List files in a folder(Directory)
`ls` list files inside the directory<br/>
**some more feature:**<br/>
`ls -a` display the list of file with hidden files<br/>
`ls -l` display the list of file with r/w permission and timing details

# Create Folder(Directory)
`mkdir` create new directory<br/>
**syntax:** `mkdir <directory_name>`<br/>
**example:** `mkdir fsftn`

#Open and Close Folder(Directory)
`cd` open&close-directory<br/>
**syntax:** `cd <directory_name>`<br/>
**example:** `cd fsftn`

# Remove/Delete file and folder(Directory)
`rm` remove files<br/>
**syntax:** `rm <file_name>`<br/>
**example:** `rm sample.txt`

`rm -r` remove folder<br/>
**syntax:** `rm <folder_name>`<br/>
**example:**`rm -r fsftn`

# Copy file and folder(Directory)
`cp` copy filec<br/>
**syntax:** `cp <source_file_location> <destination_file_location>`<br/>
**example:**  `cp /fsftn/sample.txt /Downlaods`

you can refer the image for simple example i have done created,copied and deleted directory,files etc <br/>
![Screenshot from my machine](/images/screenshot-from-2015-06-30-175447.png)

# Interesting commands
 `ls /etc /bin` list the file in both etc and bin directory

#"ls -la" list
by using the above command you can see filename,modification time at last,size of file,group and owner of file and file permissions

#"type" display the type of command
**syntax:** `type <command-name>`<br/>
**example:**  `type ls`

#"file" display the type of content which is present inside the file
**syntax:** `file <file name>`<br/>
**example:** `file fsftn.txt`

[Refer here](http://linuxcommand.org/lc3_lts0030.php)

#Mouse work
There is no work of mouse in you console you can easily handle by using only keyboard.only thing<br/>

* right_click-> you can get more options like copy,cut & paste
* left_click-> to select
* Wheel_mouse_button-> to paste the slected content

#File system in GNU/Linux user group
Hierarchical file system.All the directory comes under the root directory(/)

#Access permission and User
we can have more then one user but only one super user

#Difference between Normal and Super user
Normal user can able to create delete,update only in particular directory
Super user can have all right in whole OS.To work as a super user you just type

 `su or sudo su`

hit -> enter give your password

Now you can able to access all the file in your file system.

[you can learn file permission here](http://linuxcommand.org/lc3_lts0090.php)

[for more details you can visit](http://linuxcommand.org)

Let me complete this blog with functions <br/>

# Functions <br/>
you can also define functions in console itself.<br/>
**Syntax:**<br/>
{% highlight ruby %}
function_name()
  {
    <commands>
    <shell script>
    <etc>
  }
{% endhighlight %}
**example:**<br/>
{% highlight ruby %}
 details()
    {
      date
      ls
      ls -a
    }
{% endhighlight %}

and then type details and hit enter you will see that three commands executed at same time one by one in the order which we gave in details() function.

####Let us see shell scripts in next blog [Shell scripting Part-2]()

#video tutorial on this part(..comming soon..)<br/>
And this is specially dedicated to rocking  `echo "village boys"`.
