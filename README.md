RouteUpdate
===========
The updateRoute script can be used in order to add or delete
routes from the routing table.

## INSTALLATION 
updateRoute can be run / installed on any device that runs
Python 2.7 or later. In order to run updateRoute against a
switch, first enable Command API on the switch as follows:

```
   (config)# management api http-commands
   (config)# protocol [http|https]
   (config)# no shutdown
```

updateRoute can then be executed directly from bash as shown in
the example below:

```
(bash:root)# updateRoute 1.1.1.0/24 ethernet1 192.168.3.34 test test
```
### Command-line arguments:
```
- route with CIDR mask
- egress interface or next-hop address
- host name / ip address of switch to push/pull route
- username
- password
```

### Optional arguments:
```
--delete: removes route from routing table instead of adding it
--http: use HTTP instead of the default HTTPS
--enable-password: enable-mode password
```

## COMPATIBILITY
Version 1.0 has been developed and tested against EOS-4.12.x and is using 
the eAPI interface so should maintain backward compatibility with future
EOS versions.

## LIMITATIONS
None known.
    
## LICENSE
BSD-3, See LICENSE file