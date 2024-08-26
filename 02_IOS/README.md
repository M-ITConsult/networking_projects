# Packet Tracer - Navigating the IOS

Objectives

Part 1: Basic Connections, Accessing the CLI and Exploring Help

Part 2: Exploring EXEC Modes

Part 3: Setting the Clock

Background

In this activity, you will practice skills necessary for navigating the Cisco IOS, including different user access modes, various configuration modes, and common commands you use on a regular basis. You also practice accessing the context-sensitive Help by configuring the clock command.

## Part 1:     Basic Connections, Accessing the CLI and Exploring Help

In Part 1 of this activity, you connect a PC to a switch using a console connection and explore various command modes and Help features.

### Step 1:   Connect PC1 to S1 uses a console cable.

- Click the Connections icon (the one that looks like a lightning bolt) in the lower left corner of the Packet Tracer window.

- Select the light blue Console cable by clicking it. The mouse pointer will change to what appears to be a connector with a cable dangling off of it.

- Click PC1; a window displays an option for an RS-232 connection.

![Alt text](https://res.cloudinary.com/dceb4nzy9/image/upload/v1724683312/Screenshot_2024-08-26_162135_mhsu9d.png)


- Drag the other end of the console connection to the S1 switch and click the switch to bring up the connection list.

- Select the Console port to complete the connection.

### Step 2:   Establish a terminal session with S1.

- Click PC1 and then select the Desktop tab.

- Click the Terminal application icon; verify that the Port Configuration default settings are correct.

- Click OK.

- The screen that appears may have several messages displayed. Somewhere on the display there should be a Press RETURN to get started! message. Press ENTER.

![Alt text](https://res.cloudinary.com/dceb4nzy9/image/upload/v1724683323/Screenshot_2024-08-26_162112_hb5nqv.png)

### Step 3:   Explore the IOS Help.

- The IOS can provide help for commands depending on the level being accessed. The prompt currently being displayed is called User EXEC and the device is waiting for a command. The most basic form of help is to type a question mark (?) at the prompt to display a list of commands.

![Alt text](https://res.cloudinary.com/dceb4nzy9/image/upload/v1724683312/Screenshot_2024-08-26_162506_aktcff.png)

- At the prompt, type t, followed by a question mark (?).

![Alt text](https://res.cloudinary.com/dceb4nzy9/image/upload/v1724683312/Screenshot_2024-08-26_162519_rr0zph.png)

- At the prompt, type te, followed by a question mark (?).

![Alt text](https://res.cloudinary.com/dceb4nzy9/image/upload/v1724683312/Screenshot_2024-08-26_162538_uhjf4m.png)

This type of help is known as context-sensitive Help, providing more information as the commands are expanded.

## Part 2:     Exploring EXEC Modes

In Part 2 of this activity, you switch to privileged EXEC mode and issue additional commands.

### Step 1:   Enter privileged EXEC mode.

What information is displayed that describes the enable command?

- Type en and press the Tab key.

![Alt text](https://res.cloudinary.com/dceb4nzy9/image/upload/v1724683312/Screenshot_2024-08-26_162618_tq7chv.png)

This is called command completion or tab completion. When part of a command is typed, the Tab key can be used to complete the partial command. If the characters typed are enough to make the command unique, as in the case with the enable command, the remaining portion is displayed.

What would happen if you were to type te<Tab> at the prompt?

- Enter the enable command and press ENTER. How does the prompt change?

- When prompted, type the question mark (?).

![Alt text](https://res.cloudinary.com/dceb4nzy9/image/upload/v1724683312/Screenshot_2024-08-26_162714_m2mdcc.png)

Previously there was one command that started with the letter ‘C’ in user EXEC mode. How many commands are displayed now that privileged EXEC mode is active? (Hint: you could type c? to list just the commands beginning with ‘C’.)

### Step 2:   Enter Global Configuration mode.

- One of the commands starting with the letter ‘C’ is configure when in Privileged EXEC mode. Type either the full command or enough of the command to make it unique along with the <Tab> key to issue the command and press <ENTER>.

![Alt text](https://res.cloudinary.com/dceb4nzy9/image/upload/v1724683312/Screenshot_2024-08-26_162800_s07dee.png)


- Press the <ENTER> key to accept the default parameter enclosed in brackets [terminal].

![Alt text](https://res.cloudinary.com/dceb4nzy9/image/upload/v1724683312/Screenshot_2024-08-26_162833_xshvti.png)


- This is called global configuration mode. This mode will be explored further in upcoming activities and labs. For now exit back to Privileged EXEC mode by typing end, exit or Ctrl-Z.

## Part 3:     Setting the Clock

### Step 1:   Use the clock command.

- Use the clock command to further explore Help and command syntax. Type show clock at the privileged EXEC prompt.

![Alt text](https://res.cloudinary.com/dceb4nzy9/image/upload/v1724683312/Screenshot_2024-08-26_162926_ix9lgo.png)

- The % Incomplete command message is returned by the IOS indicating that the clock command needs further parameters. Any time more information is needed help can be provided by typing a space after the command and the question mark (?).

![Alt text](https://res.cloudinary.com/dceb4nzy9/image/upload/v1724683312/Screenshot_2024-08-26_163017_nj6ptr.png)

- Set the clock using the clock set command. Continue proceeding through the command one step at a time.

![Alt text](https://res.cloudinary.com/dceb4nzy9/image/upload/v1724692417/Screenshot_2024-08-26_191322_csmp7a.png)

What would have been displayed if only the clock set command had been entered and no request for help was made by using the question mark?

- Based on the information requested by issuing the clock set ? command, enter a time of 3:00 p.m. by using the 24-hour format of 15:00:00. Check to see if further parameters are needed.

![Alt text](https://res.cloudinary.com/dceb4nzy9/image/upload/v1724692614/Screenshot_2024-08-26_191646_oyhg8a.png)

The output returns the request for more information:

<1-31>  Day of the month

MONTH   Month of the year

- Attempt to set the date to 01/31/2035 using the format requested. It may be necessary to request additional help using the context-sensitive Help to complete the process. When finished, issue the show clock command to display the clock setting.  The resulting command output should display as:

![Alt text](https://res.cloudinary.com/dceb4nzy9/image/upload/v1724683312/Screenshot_2024-08-26_162926_ix9lgo.png)

- If you were not successful, try the following command to obtain the output above:

![Alt text](https://res.cloudinary.com/dceb4nzy9/image/upload/v1724683313/Screenshot_2024-08-26_163126_am85xd.png)

### Step 2:   Explore additional command messages.

- The IOS provides various outputs for incorrect or incomplete commands as experienced in earlier sections. Continue to use the clock command to explore additional messages that may be encountered as you learn to use the IOS.

- Issue the following command and record the messages:

![Alt text](https://res.cloudinary.com/dceb4nzy9/image/upload/v1724683313/Screenshot_2024-08-26_163343_kqtsto.png)