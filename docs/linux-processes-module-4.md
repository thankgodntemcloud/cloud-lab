A process is simply a program that is currently running.

PID is Process 

(ps, ps -e, ps aux)

ps → Shows processes associated with your current shell/session.

ps -e → Shows every process running on the Linux system.

PID 1 for systemd is very special.
When Linux boots:
Bootloader
      │
      ▼
Linux Kernel
      │
      ▼
systemd (PID 1)
      │
      ├── ssh
      ├── nginx
      ├── cron
      ├── Docker
      ├── NetworkManager
      └── ...

      The USER column, displayed by the ps aux command, shows the Linux user account that owns and started the process. This ownership determines who is allowed to manage or terminate the process without using sudo.

As a Cloud Engineer, i'll often SSH into a Linux server because "the application is slow."

One of the first commands i'll run is:
ps aux or more commonly: top

i am trying to answer questions like:
Which process is consuming all the CPU?
Which process is using too much memory?
Is nginx still running?
Did Docker crash?
Is the Java application still alive?

This is why understanding processes is such a foundational Linux administration skill.