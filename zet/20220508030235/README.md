# Port Forwarding to enable SSH into Virtualbox VM

By default, virtualbox network type is set to NAT.  Devices outside virtualbox will not be able
to  access the services within.  To allow it to do so you would need to setup port forwarding.
Go to Machine -> Settings -> Network -> Advanced -> Port Forwarding.

Make sure to select the plus icon on the side of the window that opens up.

* Name: SSH Port Forwarding (Example Name, but you can make it what you want)
* Protocol: TCP
* Host IP: Your Physical Machine's IP Address (in this case you can put the loopback address)
* Host Port: The port your Physical Machine will be using to communicate with the VM
* Guest IP:  This will be the IP Address of your VM
* Guest Port:  Typically for SSH this would be port 22

Then from your terminal on the host machine you can do `ssh -p <hostport> <user>@127.0.0.1` to
connect.

* https://bobcares.com/blog/virtualbox-ssh-nat/

    #virtualbox #ssh #remote #port-forward
