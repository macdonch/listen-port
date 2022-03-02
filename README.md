# listen-port
This  powershell script creates a temporary tcp listener on a windows system for a given ipaddress and port. It can be used in conjuction with the 'Port Query' utility to test firewall rules.

It is a modifed version of a script that was found at https://gallery.technet.microsoft.com/scriptcenter/Listen-Port-Powershell-8deb99e4#content

On windows systems, listeners can be displayed using 'netstat -a'

For systems with multiple nics, ensure that there is a route in place between the listener and the system sending the queries. e.g. if the listener is on 100.66.154.6 and the query system is at 75.153.182.99, you may need to add a route like:
```
route add 75.153.182.99 MASK 255.255.255.255 100.66.154.1
```

### Example Invocation
listen-port -ip 100.66.154.6 -port 443

## Built with
- Powershell

## Authors
- [Charles Macdonald](mailto:charles.macdonald@telus.com)
