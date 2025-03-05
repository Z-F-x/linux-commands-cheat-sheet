# The `ls` command

`ls` stand for list

## Creating symbolic lists with the `ls` command
Different Ways to Create Symbolic Links in GNU/Linux
Using the ln Command in the Terminal:

Basic Syntax:

bash
Kopier
ln -s /path/to/original /path/to/symlink
This creates a symbolic link at /path/to/symlink that points to /path/to/original.

Examples:

Linking a File:
bash
Kopier
ln -s /home/user/documents/report.txt /home/user/Desktop/report_link.txt
This creates a symlink on the Desktop pointing to report.txt in the documents folder.
Linking a Directory:
bash
Kopier
ln -s /var/www/html /home/user/web_project
Here, /home/user/web_project becomes a symbolic link to /var/www/html.
Using the symlink() System Call in a C Program:

If you need to create a symbolic link programmatically in C, you can use the symlink() function from <unistd.h>:

c
Kopier
#include <stdio.h>
#include <unistd.h>

int main(void) {
    const char *target = "/path/to/original";
    const char *linkpath = "/path/to/symlink";

    if (symlink(target, linkpath) == -1) {
        perror("symlink");
        return 1;
    }
    return 0;
}
This program creates a symbolic link just like the ln -s command.

Using Graphical File Managers:

Many desktop environments (like GNOME or KDE) allow you to create symbolic links through their file managers:

Right-click Method: You can often right-click on a file or directory and select an option like “Make Link” or “Create Shortcut.” The resulting link functions similarly to a symlink in the terminal.

