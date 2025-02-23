# pgrep Cheat Sheet
**P**rocess **G**lobal **R**egular **E**xpression **P**

## Search for process by name
```pgrep -l firefox ```

## ps 
**P**rocess **S**tatus

---
## **Options**
```-f, --full```
- Search the entire command line (not just the process name). Useful when the process name is generic or when you need to match command-line arguments.

```-l, --list-name```

- List the process name along with the process ID. This can help you confirm which process was matched.

```-x, --exact```

- Only match processes whose name exactly matches the pattern. This prevents partial matches.

```-n, --newest```

- Select only the most recently started process among those that match the pattern.

```-o, --oldest```
- Select only the oldest process among the matching ones.

```-u, --euid```
- Match processes based on their effective user ID or username.
Example: pgrep -u alice firefox finds all Firefox processes running as user "alice".

```-U, --uid```
- Similar to -u but matches the real user ID.

```-G, --group and -g, --pgroup```
- Filter processes by their effective group ID or process group ID, respectively.

```-P, --parent```
- Limit the search to processes with a specific parent process ID.

```-s, --session```
- Match processes belonging to a particular session ID.

```-d, --delimiter```
- Specify a custom delimiter for the output when printing multiple process IDs.

```-c, --count```
- Instead of listing process IDs, print the count of matching processes.

```-v, --inverse```
- Invert the matching logic so that processes not matching the pattern are returned.


---

### List all running processes
ps -aux

## top t
**T**able **O**f **P**rocesses

### Display real-time process information
top

## kill
**K**ill **I**nterrupt **L**ive **L**ines

### Terminate a process by PID
kill -9 1234

## htop Cheat Sheet
**H**eavy **T**ask **O**verview **P**rocess

### Interactive process viewer
htop

## pidof Cheat Sheet
**P**rocess **ID** **O**f

### Find PID of a running program
pidof bash
