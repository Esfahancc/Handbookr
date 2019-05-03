# Install
```
yum install -y tor
systemctl start tor
systemctl enable tor
```

# Location
```
printf "\n ExitNodes {US}" >> /etc/tor/torrc
systemctl restart tor
```
