# OverTheWire Level 4

## Objective

The OverTheWire Bandit wargame level 4 requires the user to change directories and extract the only human readable password from various files. This level focuses on navigating different directories and understanding and efficiently reading multiple files at once. 

### Skills Learned

- Directory traversal using commands like `cd` and `cd ..`
- Opening multiple files at once using the wild card `*`
- Problem solving and critical thinking


### Tools Used

- Linux terminal
- `ls`, `file`, `ssh`, `*`, `cat`, `cd`

## Steps

![Screenshot 2024-10-02 004637](https://github.com/user-attachments/assets/358e8119-3cc7-4279-bd80-ee246fb21a14)

Upon entering Level 4, the first step was to use the `ls` command to list the contents of the current directory and then `cd` into the `inhere` directory.

From there, I performed another `ls`, which revealed nine files to check for the human-readable password. Using `cat` on each file seemed tedious and inefficient, especially with the clutter created by the large amounts of information displayed from cat when checking incorrect files. Instead, I used `./file0*`, which returned any files matching that name pattern.

This command provided a list of each file along with its type, and `-file07` was the only one identified as containing ASCII text—a format easily readable by humans. I then executed `cat ./-file07` and retrieved the password for the next level.

Overall, this experience taught me the importance of efficiently navigating file structures and using wildcards to simplify the process of locating specific files.


