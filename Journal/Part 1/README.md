# [Evennia Beginner Tutorial Part 1 - Using Commands and Stuff](https://www.evennia.com/docs/latest/Howtos/Beginner-Tutorial/Part1/Beginner-Tutorial-Part1-Overview.html)
## Intro
Default syntax:
```
command[/switch/switch...] [arguments]
```

A _/switch_ is a special, optional flag to make to make the command act differently
**Example:**
```
create box
```
vs
```
create/drop box
```

In the first example, the command **create** creates an object named _box_ and by default adds it to your inventory.<br>
However, in the second example we add the **/drop** _switch_ to the **create** command. This changes the action of the **create** command and makes you drop the box into the room your avatar currently resides instead of placing it into your inventory.
## 1.1 Getting Help
For general help:
```
help
```
for help with a specific command
```
help <command>
```
## 1.2 Looking Around
The most common command is **look**. This will show you the description of the environment, a list of objects in the room, and exits. This is commonly shortened to:
```
l
```
## 1.3 Stepping Down from Godhood
Some puzzles, traps, and other interactive objects react differently depending on the permissions of the avatar you are playing. If you are an admin or superuser, objects may not act as intended when testing them. A simple command will remove your superuser status:
```
quell
```
This command will remove your superuser permissions and everything in your environment will react to you as if your were a normal player.<br>
To restore your superuser permissions simply enter the following command:
```
unquell
```
## 1.4 Creating an Object
First, create a box with the following command:
```
create box
```
