There is no vagrantfile for this box, instead create the virtual machine manually

Then create a user vagrant with the password vagrant

```
useradd -m vagrant
usermod -aG wheel vagrant
```

*Note that I use this to escalate to sudo in the inventory file it is not secure in any way and should only be used for dev/test purposes*

Next add port forwarding to your virutalbox. I used
```
host: 127.0.0.1
host_port: 2222
guest: <guest ip>
guest_port: 22
```

For ansible add in the authorized keys:
On the guest run:
```
systemctl enable sshd
```
On your host run:
```
ssh vagrant@127.0.0.1 -p 2222 "mkdir ~/.ssh"
scp -P 2222 -pr ~/.ssh/id_rsa.pub vagrant@127.0.0.1:/home/vagrant/.ssh/authorized_keys
```

Create a virtualbox share folder named manjaro_share

Ansible should be all set to configure the machine now, you can test with:
```
ansible all -i inventory -m "ping"
```
