*Here, I go through the Leviathan Wargames from OverTheWire. A link is [here](https://https://overthewire.org/wargames/leviathan/).*

## Table of Contents
1. [level 0](#level0)
2. [level 1](#level1)
3. [level 2](#level2)
4. [level 3](#level3)
5. [level 4](#level4)
6. [level 5](#level5)
7. [level 6](#level6)
8. [level 7](#level7)
9. [level 8](#level8)

## level 0<a name="level0"></a>

- We sign in with `ssh leviathan0@leviathan.labs.overthewire.org -p 2223`

- The password is `leviathan0`

- We are now signed in.

![leviathan_0.png](https://github.com/starscreamF22/OverTheWire/blob/main/images/leviathan_0.png)

# level 0 to 1<a name="level1"></a>

- We sign in with `ssh leviathan0@leviathan.labs.overthewire.org -p 2223`

- The password is `leviathan0`

- We are now signed in.

- We are told that the data for the levels can be found in the homedirectories and you can look at /etc/leviathan_pass for the various level passwords.

- `ls -a`

- `cd .backup`

- `ls`

- `cat bookmarks.html`

- Using `grep` allows us to access a specific string, in this case `leviathan1`

- `grep leviathan1 bookmarks.html`

- And we see the password is `PPIfmI1qsA`

![leviathan_1.png](https://github.com/starscreamF22/OverTheWire/blob/main/images/leviathan_1.png)

# level 1 to 2<a name="level2"></a>

- We sign in with `ssh leviathan1@leviathan.labs.overthewire.org -p 2223`

- The password is `PPIfmI1qsA`

- We are now signed in.

- `ls -a`

- `./check` then enter `PPIfmI1qsA`

- `ltrace` is the way to see what the library calls are for the program `./check`

- `ltrace ./check` then enter `PPIfmI1qsA`

- We can see the password is sex.

- `./check (enter sex)`

- `whoami`

- `cat /etc/leviathan_pass/leviathan2`

- We see the password is `mEh5PNl10e`

![leviathan_2.png](https://github.com/starscreamF22/OverTheWire/blob/main/images/leviathan_2.png)

# level 2 to 3<a name="level3"></a>

- We sign in with `ssh leviathan2@leviathan.labs.overthewire.org -p 2223`

- The password is `mEh5PNl10e`

- We are now signed in.

- `ls`

- `./printfile`

- `./printfile leviathan3`

- `mkdir/tmp/water` I make a temporary directory

- `cd/tmp/water`

- `touch fanta.txt` I create a file

- `ls`

- `ltrace ~/printfile fanta.txt` I use ltrace to see what happens when `printfile` when it is run with the file `fanta.txt`

- `touch pass\ file.txt`

- `ls`

- `touch pass\ coke.txt`

- `ltrace ~/printfile "pass coke.txt"`

- `ln -s /etc/leviathan_pass/leviathan3 /tmp/water/pass` I create a link

- `ls`

- `~/printfile "pass coke.txt"`

- and the password is `Q0G8j4sakn`

![leviathan_3.png](https://github.com/starscreamF22/OverTheWire/blob/main/images/leviathan_3.png)

# level 3 to 4<a name="level4"></a>

- We sign in with `ssh leviathan3@leviathan.labs.overthewire.org -p 2223`

- The password is `Q0G8j4sakn`

- We are now signed in.

- `ls`

- `./level3` then enter `Q0G8j4sakn`

- `ltrace ~/level3`

- `./level3`

- enter the password 

- `snlprintf`

- `whoami`

- `cat /etc/leviathan_pass/leviathan4`

- And the password we get is `AgvropI4OA`

![leviathan_4.png](https://github.com/starscreamF22/OverTheWire/blob/main/images/leviathan_4.png)

# level 4 to 5<a name="level5"></a>

- We sign in with `ssh leviathan4@leviathan.labs.overthewire.org -p 2223`

- The password is `AgvropI4OA`

- We are now signed in.

- `ls -a`

- `file .trash`

- We see it is a directory.

- `cd .trash`

- `ls`

- `./bin`

- We see it is binary, so I go to google converter for binary.

- https://www.rapidtables.com/convert/number/binary-to-ascii.html

- I input the binary and we get out the password `EKKlTF1Xqs`.

![leviathan_5.png](https://github.com/starscreamF22/OverTheWire/blob/main/images/leviathan_5.png)

# level 5 to 6<a name="level6"></a>

- We sign in with `ssh leviathan5@leviathan.labs.overthewire.org -p 2223`

- The password is `EKKlTF1Xqs`

- We are now signed in.

- `ls`

- `./leviathan5`

- `ltrace ./leviathan5`

- `ln -s /etc/leviathan_pass/leviathan6 /tmp/file.log`

- `ls`

- `./leviathan5`

- The password is `YZ55XPVk2l`

![leviathan_6.png](https://github.com/starscreamF22/OverTheWire/blob/main/images/leviathan_6.png)

# level 6 to 7<a name="level7"></a>

- We sign in with `ssh leviathan6@leviathan.labs.overthewire.org -p 2223`

- The password is `YZ55XPVk2l`

- We are now signed in.

- `ls`

- `./leviathan6`

- `ltrace ./leviathan6`

- `mkdir /tmp/pluto`

- `cd /tmp/pluto`

- `vim sun.sh`

- Type in the following:

`#!/bin/bash 
for a in {0000..9999}
do
~/leviathan6 $a
done`
    
- `cat vim.sh`

- `chmod +x sun.sh`

- `./sun.sh`

- Wait until you get access and the loop ends

- `whoami`

- `cat /etc/leviathan_pass/leviathan7`

- And we get the password `8Gpz5f8Hze`

![leviathan_7.png](https://github.com/starscreamF22/OverTheWire/blob/main/images/leviathan_7.png)

# level 7 to 8<a name="level8"></a>

- We sign in with `ssh leviathan7@leviathan.labs.overthewire.org -p 2223`

- The password is  `8GpZ5f8Hze`

- `ls`

- `cat CONGRATULATIONS`

- And we see we are done.

![leviathan_6.png](attachment:leviathan_6.png)
