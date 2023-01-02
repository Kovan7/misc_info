# STRACE

<p>
Use the command Strace to view the kernel calls that SSH makes when users send commands.  
This is convenient when you are unable to intercept the encrypted SSH traffic but have access to
the SSH server.  View the commands which are being sent to the server and monitor for nefarious traffic.
</p>

<p>
Command
`
root$ strace -p <pid> -f 2>&1 | grep 'read(0'
`

</p>
<p>
For defenders, this is a great tool to use when focusing on a single server to see what calls are being made.  
Also great for Red/Blue team CTFs.
</p>