# Lab Report #1
## Step 1: Downloading VS Code
Begin by searching "VS Code download" and going to the official website of VS Code. The page should look something like this:
![DownloadPage](Screenshots/DownloadPage.png)
[Download Link](https://code.visualstudio.com/download)

Choose the appropriate download for your machine. I had an Apple Silicon MacBook so I chose the correponding zip file under Mac.

You should then see a startup screen after following the instructions to download the file.

![VSCodeStartupPage](Screenshots/VSCodeStartupPage.png)

## Step 2: Remotely Connecting
If you're like me and use a Mac, go into your terminal in VS Code and type the following command:
```
$ ssh cs15lwi22zz@ieng6.ucsd.edu
```
Of course, you should be using your own email address associated with ieng6, and mine is cs15lwi22abb@ieng6.ucsd.edu

When I began, I ran into trouble with my password. Here's what I saw:

![PasswordTrouble](Screenshots/PasswordTrouble.png)

Do not worry. Change your password on TritonLink and wait for around five minutes for the change to register, and then you should be able to log on. Here's what it should look like:

![SuccessfulLoginWithPassword](Screenshots/SuccessfulLoginWithPassword.png)

## Step 3: Run Some Commands
At this point, return to your personal machine, and try out some terminal commands. Here's what I tried:

![RunSomeCommands](Screenshots/RunSomeCommands.png)

A brief explanation: `cd` changed the directory to the root directory of my computer, and the subsequent `ls` command listed the folders I had in that root directory. `ls -a` simply gave more details to the root directory.

## Step 4: Moving Files over SSH with scp
To move a file using SSH and the `scp` command, first login to the remote machine at ieng6.

(insert "Successful Login with Password" here)

Notice the syntax I used here: `scp <file_name.java> <remote_address>:~/`

Use this format to transfer the file over SSH.

![ConfirmingSuccessfulTransfer](Screenshots/ConfirmingSuccessfulTransfer.png)

Above is me confirming that the file has indeed been transfered to the remote machine. I am in the remote machine, and I call the `ls` command, and the file I sent, `WhereAmI.java` shows up. The next two lines show that I can compile and run the file remotely without error. This tells you that you have succeeded.

## Step 5: SSH Keys
At this point, you must login each time with a long password (as mandated per Active Directory guidelines). That is inconvenient and ruins the fluidity of the workflow. Here is where SSH keys come in.

First type in the command `ssh-keygen`. The system will produce the following response:

1. Give you a file path where the key is stored. Make note of this!
2. Ask you to enter a passphrase. This is optional; you can leave it blank and you will be able to login without any password. I chose a short phrase as my passphrase.
3. If you chose a passphrase, you will need to confirm it like everywhere else you create a password.

![SettingUpTheKeys](Screenshots/SettingUpTheKeys.png)

In the picture above, notice the line that says "Enter the passphrase for...". That's where I entered my passphrase and was granted access to the remote machine.

## Step 6: Optimizing the Remote Running Experience


I think this part has a lot to do with personal preference. I do like the speed of having everything in one line, but also feel that this may make my work more prone to errors (syntax and typos).

In total, counting spaces and enter keys, I believe that the total number of keystrokes for that one line command was around 144. This is just me typing out everything on one line.

Seeing that that's not the most optimized route, I decided to utilize copy-pasting and the tab key. I was then able to decrease the number to around 49. This is using tab to autocomplete file names and copy-pasting the ieng6 email address.

![OneLiner](Screenshots/OneLiner.png)