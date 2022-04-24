# mtu

This script allows to get the MTU path (finding bottleneck in connection) to a host.
It was coded to have zero dependance to ifconfig or ip programs, only to ping. The initial goal was to be able to run it inside tiny containers, which had no way to reach the outside world (unable to install anything, just being able to do some icmp queries due to small packet size), especially because of some MTU limitation in the way.

Just run ./get_mtu_path *HOST*, where HOST can be a FQDN or an IP (v4) address.
