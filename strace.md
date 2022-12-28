# STRACE

<p>
Use the command Strace to view the kernel calls that SSH makes when users send commands.  
This is convenient when you are unable to intercept the encrypted SSH traffic but have access to
the SSH server.  View the commands which are being sent to the server and monitor for nefarious traffic.


Command
```
root$ strace -p <pid> -f 2>&1 | grep 'read(0'
```