Once an SSH key has been created, the ssh-copy-id command can be used to install it as an authorized key on the server. Once the key has been authorized for SSH, it grants access to the server without a password.
[ssh-copy-id](https://www.ssh.com/ssh/copy-id)
> Use a command like the following to copy SSH key:
```sh
ssh-copy-id -i ~/.ssh/mykey user@host
```
