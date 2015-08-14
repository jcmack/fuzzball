brctl - manages linux bridges

Show help text:
```
[root@ovn86-18 ~]# brctl
Usage: brctl [commands]
commands:
	addbr     	<bridge>		add bridge
	delbr     	<bridge>		delete bridge
	addif     	<bridge> <device>	add interface to bridge
	delif     	<bridge> <device>	delete interface from bridge
	setageing 	<bridge> <time>		set ageing time
	setbridgeprio	<bridge> <prio>		set bridge priority
	setfd     	<bridge> <time>		set bridge forward delay
	sethello  	<bridge> <time>		set hello time
	setmaxage 	<bridge> <time>		set max message age
	sethashel 	<bridge> <int>		set hash elasticity
	sethashmax	<bridge> <int>		set hash max
	setmclmc  	<bridge> <int>		set multicast last member count
	setmcrouter	<bridge> <int>		set multicast router
	setmcsnoop	<bridge> <int>		set multicast snooping
	setmcsqc  	<bridge> <int>		set multicast startup query count
	setmclmi  	<bridge> <time>		set multicast last member interval
	setmcmi   	<bridge> <time>		set multicast membership interval
	setmcqpi  	<bridge> <time>		set multicast querier interval
	setmcqi   	<bridge> <time>		set multicast query interval
	setmcqri  	<bridge> <time>		set multicast query response interval
	setmcqri  	<bridge> <time>		set multicast startup query interval
	setpathcost	<bridge> <port> <cost>	set path cost
	setportprio	<bridge> <port> <prio>	set port priority
	setportmcrouter	<bridge> <port> <int>	set port multicast router
	show      	[ <bridge> ]		show a list of bridges
	showmacs  	<bridge>		show a list of mac addrs
	showstp   	<bridge>		show bridge stp info
	stp       	<bridge> {on|off}	turn stp on/off
```	

Show all of the current linux bridges on the system:
```
[root@ovn86-18 ~]# brctl show
bridge name	bridge id		STP enabled	interfaces
qbrdb90fd6f-90		8000.4220b6ce9615	no		qvbdb90fd6f-90
							tapdb90fd6f-90
```
Verify the linux bridge is up to be used by tcpdump

```	
[root@ovn86-18 ~]# ifconfig | grep qbrdb90fd6f-90
qbrdb90fd6f-90 Link encap:Ethernet  HWaddr 42:20:B6:CE:96:15  
```
