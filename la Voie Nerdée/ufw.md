*Uncomplicated Firewall (ufw)* is a frontend for [[iptables]].
It provides a user friendly way to create an IPv4 or IPv6 host-based firewall, GUI (gufw) and a simple command-line interface.

# 🛠️ Setup

- Install the package:

```bash
sudo apt-get install ufw
```

- Enable firewall:

```bash
sudo ufw enable
```

> ⚠️ If you are configuring over SSH, you may wish to allow SSH before enabling the firewall. If your connection gets interrupted before allowing SSH you may be locked out of your system.

- Set up default config:

```bash
sudo ufw default deny incoming
sudo ufw default allow outgoing
```

- Verify that the firewall is enabled:

```bash
sudo ufw status verbose
```

# 🚔 Rules

By default ufw denies all of the incoming connections, which will make it a problem if you are using SSH.
Therefore, you must create a rule which allows SSH connections:

```bash
sudo ufw allow ssh
```

Other rules may be added in the same way by simply specifying a name of the program.
Ufw comes with preloaded defaults for some commonly used software.
To list the default apps:

```bash
sudo ufw app list
```

Rules may be deleted with the following command:

```bash
sudo ufw delete allow ssh
```





[^1]: Sources:
	https://wiki.debian.org/Uncomplicated%20Firewall%20%28ufw%29
