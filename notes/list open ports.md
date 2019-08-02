---
tags: [network]
title: list open ports
created: '2019-07-30T06:19:49.165Z'
modified: '2019-08-02T07:48:12.341Z'
---

# list open ports

## ss -tuna,please!
```sh
ss -tunapls
  # -n - dont try to resolve ip addresses
  # -p show PIDs using the sockat
  # listening or connection         which protocols ?
  # default: connections            default: all
  # -l listening                      -t: TCP
  # -a both                           -u: UDP
  #                                   -x: unix domain sockets
```

## netstat
```sh
netstat -c              # continuasly

netstat -s              # summary
netstat -st             # summary of tcp

netstat -lptu           # -l, [--listening|-l] Show only listening sockets.  (These are omitted by default.)
                        # -p, [--program|-p] Show the PID and name of the program to which each socket belongs
                        # -t, [--tcp|-t]
                        # -u, [--udp|-u]

netstat -lptuna         # [--all|-a]

netstat -lptun          # -n, [--numeric|-n] Show numerical addresses instead of trying to determine symbolic host, port or user names
```

## nmcli
```sh
nmcli device show <interfacename> | grep IP4.DNS        # show dns nameserver
```

## scan network
```sh
nmap -sP 192.168.1.1/24

arp -a | awk '{ ahost=$1; aip=$2; gsub("()","",aip); print aip }';

arp -a | awk '{ gsub(/[()]/,""); print $1 " " $2}'
```