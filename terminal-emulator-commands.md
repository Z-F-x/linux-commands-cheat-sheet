# Output the list of a specific filetype
`printf` `"%s\n"` `*.txt`

# Create an empty file
`touch` `< file_name >`

# Unzip and install `pkg.tar.zst` files
`sudo` `pacman` `-U` `--noconfirm` `your-package.pkg.tar.zst`

# Run a command and let it run in the background (in this example launch waybar and let it run in the background and you can use the terminal for other things):
`waybar` `&` `disown`

#To list processes in Linux, use one of the five commands: 
`ps`, `top`, `htop`, `atop`, and `pstree`.

# Kill task Identify the name of the process to be terminated. Execute the following command, replacing < process_name > with the name of the target process: 
`killall` `< process_name >`

### Directory Navigation ##
# List all items in a column instead of row:
`ls` `-1`

# List all folders 
`ls` `-d` `*/`

## Examples of Combinations:
# List all folders in a column:
`ls` `-1` `-d` `*/` 

# Print the path of current directory
`pwd`



# countnumber of lines in a file; 
`wc` `< file_name >` # wc = word count

        # Common Options:
        `-l` # Count lines.
        `-w` # Count words.
        `-c` # Count bytes (or characters, depending on the implementation).
        `-m` # Count characters (especially relevant for multi-byte character encodings).

# Set 500 mb limit to `root/var/log/journal` files (useful when you've run out of disk space on root partition and have gotten the error message: "your root partition is running out of disk space, you have 0 mib remaining (0%).":
`sudo` `journalctl` `--vacuum-size=500M`

# Flush pacman cached packages (Also useful when yoǘ've run out of disk space on your root partition. Pacman keeps backups of older versions of software you install.): 
`sudo` `pacman` `-Scc`


sudo chmod 666 /dev/vmnet*

The chmod 666 command is used to change the permissions of a file or device. In this context, the command sudo chmod 666 /dev/vmnet* is modifying the permissions of the /dev/vmnet* device files (which include /dev/vmnet1, /dev/vmnet0, etc.).
Breakdown of chmod 666

The 666 permission setting means:

    6 for the owner (read and write)
    6 for the group (read and write)
    6 for others (read and write)

Each digit represents a permission setting for different categories of users:

    Owner: The user who owns the file.
    Group: Users who are part of the file's group.
    Others: All other users.

Explanation of the Permission Digits

The 666 is derived from the octal number system, where each digit corresponds to a combination of read, write, and execute permissions:

    4: Read (r)
    2: Write (w)
    1: Execute (x)

Adding these values gives you different permission combinations:

    6 (Read + Write) = 4 + 2 = rw-
    7 (Read + Write + Execute) = 4 + 2 + 1 = rwx

So, 666 translates to:

    rw- rw- rw-: Read and write permissions for the owner, group, and others. There is no execute permission.

What This Means for /dev/vmnet*

Applying chmod 666 to /dev/vmnet* grants:

    The owner: Read and write access
    The group: Read and write access
    Others: Read and write access

Security Implications

#Using chmod 666 on device files allows all users (including unprivileged ones) to read from and write to these devices, which may pose a security risk. It's generally safer to use more restrictive permissions and only grant access to trusted users or groups.

For example, if you need to give only the root user and a specific group access, you might use more restrictive permissions, such as chmod 660 (owner and group have read/write access, others have none).
Conclusion

The command sudo chmod 666 /dev/vmnet* sets read and write permissions for everyone on the /dev/vmnet* device files, which is sometimes used to troubleshoot or ensure VMware has access to these devices. However, be cautious and consider reverting the permissions to a more secure setting once you’re done troubleshooting.

------------------------------------------------------------------------

#When the sudoers password / sudo password does not work
faillock --reset

