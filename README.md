Freifunk OpenVPN-Exit
=========

This role installs and configures OpenVPN. It is used to provide an Internet-Exit for Freifunk nodes.

Please note, that neither any dhcp, nor any radvd configuration is provided by this role - it's OpenVPN only.
TAP devices are use. Configuring them statically using standard system configuration files is outside the scope of this role.

Note: This role creates an easy_rsa user having a skeleton - but private key material is not included.



Role Variables
--------------
```
openvpn_exit:
  identifier:      # Instance name - used for logging to /var/log/openvpn_name.log
    port      # TCP / UDP Port 
    dev       # Tap device name
    proto     # (tcp-server / udp)
    cert      # Certificate file name
    ca        # CA certificate file
    tls-auth  # Static key for hmac firewalling 
```   

Example Playbook
-------------------

```
```

License
-------

GPLv3

