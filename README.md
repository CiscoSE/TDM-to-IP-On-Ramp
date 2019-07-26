
# TDM-to-IP-On-Ramp-Setup-with-Python

# Read Me notes

1. The python script provided here shows an example to provision muliple cisco products that serve the purpose of TDM to IP circuit emulation   i.e. NCS 4200s, to take those nodes to the point being ready to provision MPLS Tunnels and Services (Pseudowires).

2. The python script uses telnet connectivity to talk to the nodes.

3. This script has been tested in python version 3.6.4, 3.6.5 and 2.7.10.

4. This script uses routing protocol OSPF since the test bench in the lab uses it.

5. This script uses SyncE for network clock synchronization.

6. It takes input data from an Excel file with a specific format. The information should be placed at the correct row/column so that the script can parse the information accordingly.

7. Uses IPv4 addresses in the network.

8. The purpose of this demo is to show the initial configuration can be done in this way as well. Any required changes/updates in the script can be done by the users to make it better according to their requirements.

9. It is required to setup management ip, enable telnet, username, password and enable password for each node before using the script.

Other Project Derivatives:
	https://github.com/CiscoSE/CEM-Initial-Configuration-Setup-with-Python
 
# It Covers

1. Enable CDP in the global configuration mode.

2. Setup a Loopback IP address.

3. Create OSPF Routing process.

4. Setup OSPF Routing for Loopback interface. 

5. Setup MPLS LDP in Global Configuration mode.

6. Enable MPLS Traffic Engineering (MPLS-TE) in Global Configuration mode

7. MPLS TE setup under the OSPF Routing

8. At Interface Level: 
      * Enable CDP,
      * IP address setup,
      * OSPF Routing setup,
      * Enable MPLS TE, MPLS IP
      * RSVP setup,
      * Enable SyncE

9. Setup Network Clock SyncE



# It does not cover

1. Configurations for EPNM server.

2. Building MPLS Tunnels and Pseudo-wires

# Excel file content format

1. Using .xlsx type excel work sheet.

2. All the data should be placed in correct order.

3. For multiple data in one cell (example, column: interfaces, ips, clock source interfaces),  use new line to separate each entry.

4. On the column for rsvp, each cell format should be in text format, otherwise the percentage entry is converted to decimal entry (like: 100% becomes 1 when parsed by python). User can use either or % value(i.e. 100%) or, kbps value (i.e. 1000000). 

5. The number of NCS4200 nodes should be given at the cell shown in red circle. Users need to have add/remove the number of rows with data matching that number.

*The ip addresses and other information in the table below are just examples. Users need to use their own network information. 
![Alt text](images/exampleData.png?raw=true "ExampleExcelData")

* MPLS label range is 16 to 32768.

* If External bit source is "Y", then enter "R0" OR "R1". Users required to change in the code if more than one external source is required.

* If External bit source is "N", then enter the physical SyncE interface(s).  

* Clock source PRIORITIES range is 1 to 250 for IOS XE NCS 4200 device.

