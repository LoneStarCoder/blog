
### Reset the network connection or network manager

    systemctl restawrt NetworkManager

### Setup a Network Bridge
**Note:** where enp24s0 is the ethernet connection name. Many times it is just eth0. to get it, type ip link show or ip addr. This link may be helpful: https://unix.stackexchange.com/questions/255484/how-can-i-bridge-two-interfaces-with-ip-iproute2

    ip link add name br0 type bridge
    ip link set dev br0 up
    ip link set dev enp24s0 master br0
