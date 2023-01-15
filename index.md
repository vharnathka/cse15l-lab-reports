# Lab Report 1
Vedika Harnathka

This is a tutorial to show you how to successfully connect to and run commands on a remote computer in UCSD's CSE basement.

## Step 1: Logging into your CSE15L Account
Click this [link](https://sdacs.ucsd.edu/~icc/index.php) for your course-specific CSE 15L account.

Log in with your username and your student ID (it should start with either an A or a U)

[screenshot]
![Picture of page once logged in](https://github.com/vharnathka/cse15l-lab-reports/blob/main/15L%20SS1.png)

Click on the CSE 15L account name. it should be in a grey box.

There should be a link to change your password.

<span style="color:grey">
 ### Changing your password
 Enter the password you use for your UCSD account, and follow the requirements for your new password.

The next part is a little complicated:

![Picture of password change page](https://github.com/vharnathka/cse15l-lab-reports/blob/main/CSE15L%20SS2.png)
Make sure to click *No* for change MyTritonLink password and *Yes* for change course-specific account password. Now **don't** click on check password. Instead, after you have selected Yes for change course-specific account password, hit enter on your keyboard. 

The next page should start to load, and if your password is complex enough, it should reset.

Once you have successfully reset your password, wait for at least 15 minutes before doing step 3.
</span>

## Installing VS Code
In the meantime, let’s install Visual Studio Code.

Go to the Visual Studio Code website here, and follow the instructions specific to your device’s operating system to download and install the application.

Here is what it should look like once you’ve successfully installed the app:

[SCREENSHOT]

## Remotely Connecting
If it has been 15 minutes since you changed your password, you can connect to a remote computer. These instructions are specific to macOS users.

On VScode, open a terminal, using Command+`. Type in your first command:

```
ssh cs15lwi23xx@ieng6.ucsd.edu
```

Where xx is the code for your specific account. `ssh` is also known as secure shell, the main command to access a computer remotely.

Your first message should ask to confirm the authenticity of the host `ieng6.uced.edu`. Type in `yes` to move forward.

Then enter in your password - note that you won’t be able to see the text for your password as you type it.

You should now get a message that looks like this

[SCREENSHOT]

This means that you have successfully connected your terminal to a computer in the CSE building basement.

## Step 4: Runnig Commands
