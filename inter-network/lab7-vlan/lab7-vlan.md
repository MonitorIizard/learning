```
show vlan
```

**Before assign Vlan**

VLAN Switch1

```bash
VLAN Name                             Status    Ports
---- -------------------------------- --------- -------------------------------
1    default                          active    Fa0/1, Fa0/2, Fa0/3, Fa0/4
                                                Fa0/5, Fa0/6, Fa0/7, Fa0/8
                                                Fa0/9, Fa0/10, Fa0/11, Fa0/12
                                                Fa0/13, Fa0/14, Fa0/15, Fa0/16
                                                Fa0/17, Fa0/18, Fa0/19, Fa0/20
                                                Fa0/21, Fa0/22, Fa0/23, Fa0/24
                                                Gig0/1, Gig0/2

```

VLAN Switch2

```bash
VLAN Name                             Status    Ports
---- -------------------------------- --------- -------------------------------
1    default                          active    Fa0/1, Fa0/2, Fa0/3, Fa0/4
                                                Fa0/5, Fa0/6, Fa0/7, Fa0/8
                                                Fa0/9, Fa0/10, Fa0/11, Fa0/12
                                                Fa0/13, Fa0/14, Fa0/15, Fa0/16
                                                Fa0/17, Fa0/18, Fa0/19, Fa0/20
                                                Fa0/21, Fa0/22, Fa0/23, Fa0/24
                                                Gig0/1, Gig0/2
```

default VLAN of every port will be on Port 1

<hr>

```bash
show running config
```

```bash
interface FastEthernet0/1
!
interface FastEthernet0/2
!
interface FastEthernet0/3
!
interface FastEthernet0/4
```

<hr>

### to config Vlan

inconfig mode
```bash
interface vlan 1
ip address 192.168.1.1 255.255.255.0
no shutdown
exit
```

assign ip to Vlan1 in order to edit something in `Switch`

```bash
ip default-gateway 192.168.1.1
```

```bash
vlan `NUMBER`
name `DESIRE NAME`
```

after set name for Vlan

```bash
10   CS                               active    
20   MCS                              active    
30   DCS                              active
```

assign port to Vlan

```bash
interface `PORT TO ASSIGN VLAN`
switchport access vlan `VLAN NUMBER`
```

or 

```bash
interface range `PORT TO ASSIGN VLAN - end eg : Fa0/2 - 8`
switchport access vlan `VLAN NUMBER`
```

**After assign Vlan**

```bash
VLAN Name                             Status    Ports
---- -------------------------------- --------- -------------------------------
1    default                          active    Fa0/1, Fa0/3, Fa0/6, Fa0/7
                                                Fa0/8, Fa0/11, Fa0/12, Fa0/13
                                                Fa0/14, Fa0/15, Fa0/16, Fa0/17
                                                Fa0/18, Fa0/19, Fa0/20, Fa0/21
                                                Fa0/22, Fa0/23, Fa0/24, Gig0/1
                                                Gig0/2
10   CS                               active    Fa0/2
20   MCS                              active    Fa0/4, Fa0/5
30   DCS                              active    Fa0/9, Fa0/10
```