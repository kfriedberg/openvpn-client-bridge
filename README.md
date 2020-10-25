Get OpenVPN L2 client files from your server software and follow instructions in etc/openvpn/client/example_bridge.conf

In etc/openvpn/bridge/bridge-start  
`eth=` must match the name of the interface you are using for your bridge (as seen in `ip link` command)  
`eth_ip=` is a free, reserved IP on your VPN  
`eth_netmask=` and `eth_broadcast=` must match what is set on the VPN

Example commands:
```
systemctl start openvpn-client-bridge@example_bridge
systemctl status openvpn-client-bridge@example_bridge
systemctl stop openvpn-client-bridge@example_bridge
```
