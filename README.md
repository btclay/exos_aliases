# EXOS CLI Aliases

Starting in EXOS 22.3, alias functionality is available. These aliases are per session, but a new auto-executing `exshrc.xsf` file has been defined that allows commands to be executed on login (allowing aliases to be restored).

In order to get these aliases to be persistent across sessions, place the commands in a file named `exshrc.xsf` in the  `/usr/local/cfg/` directory of the switch.

## Ports

### Show current link state as well as history for all ports

```
alias port_link_history "show port info detail | include Port:|Link\sState:|Link\sUps:|Link\sDowns:"
```
#### Example output:
```
X440G2-12t-10G4.18 # port_link_history
Port:	1
	Link State:	Active, 1Gbps, full-duplex
	Link Ups:       1        Last: Thu Aug 03 16:59:29 2017
	Link Downs:     0        Last: --
Port:	2
	Link State:	Ready
	Link Ups:       0        Last: --
	Link Downs:     0        Last: --
```
