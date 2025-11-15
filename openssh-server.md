# Setup OpenSSH Server

## Langkah-langkah

Check if SSH is installed:
```bash
dpkg -l | grep openssh-server
```

If SSH is not installed yet, install with command:
```bash
sudo apt install openssh-server
```

Enable and start the SSH service:
```bash
sudo systemctl enable ssh
sudo systemctl start ssh
```

Verify that SSH is running:
```bash
systemctl status ssh
```


## How to Access from Another Computer

```bash
ssh $USER@<ip>
```