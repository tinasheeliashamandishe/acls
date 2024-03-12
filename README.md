<h1>ACL: Access Control Lists</h1>

<h2>Description</h2>
In this lab, Access Control Lists will be configured for a small Enterprise. ACLs can configured Numbered(Standard and Extended) and Named(Standard and Extended).
<br />

<h2>Environments Used </h2>

- <b>Packet Tracer</b>

<h2>Lab walk-through:</h2>

<p align="center">
<h4>Lab Topology:</h4>
In this lab Numbered, standard and extended ACLs will be configured.<br />
The routers and PCs have been configured with their network addressing settigs. <br />
ROUTER 2 has learnt the routers the 10.10.11.0/24 and 10.10.12.0/24 through a routing protocol.
<img src="https://i.imgur.com/JZsSwy1.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />

<h4>Verify Connectivity:</h4> 
Before applying any Access control lists, verify that all PCs have connectivity to each other. <br/>
Ping every PC AREA2_PC1 <br/>
<img src="https://i.imgur.com/1gHCe4o.png" height="80%" width="80%" alt="Disk Sanitization Steps"/> <br/>
Verify that all PCs have connectivity to ROUTER 2 <br/>
Ping every PC from ROUTER 2 <br/>
<img src="https://i.imgur.com/TRq13YT.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />

<h4>Numbered Standard ACL: </h4>
Configure a numbered standard ACL on ROUTER_1 that denies traffic from the 10.10.12.0/24 subnet to ROUTER_2.<br/>
The PCs in the 10.10.11.0/24 and 10.10.12.0/24 subnets must maintain connecticity to each other.<br/>
The PCs in the 10.10.11.0/24 subnet should maintain connectivty to ROUTER_2.<br/><br/>
Configuration on ROUTER_1.
<img src="https://i.imgur.com/5F8gtEx.png" height="80%" width="80%" alt="Disk Sanitization Steps"/><br/>
AREA1_PC1 in the 10.10.11.0/24 still has connectivity to ROUTER_2 and the 10.10.12.0/24 subnet.
<img src="https://i.imgur.com/zPiaFET.png" height="80%" width="80%" alt="Disk Sanitization Steps"/><br/>
AREA2_PC1 in the 10.10.12.0/24 has no connectivity to ROUTER_2 but still has connectivity to the 10.10.11.0/24 subnet.
<img src="https://i.imgur.com/B1rIz58.png" height="80%" width="80%" alt="Disk Sanitization Steps"/><br/>

<br />

<br />
<h4>Numbered Extended ACL: </h4>
Configure a numbered extended ACL on ROUTER_1 that permits Telnet from AREA 1_PC1 to ROUTER_2.<br/>
Telnet to ROUTER_2 should be denied for all other PCs in the network<br/>
All other connectivity should be maintained.<br/><br/>
Configuration on ROUTER_1.
<img src="https://i.imgur.com/BllSF8X.png" height="80%" width="80%" alt="Disk Sanitization Steps"/><br/>
AREA1_PC1 can ping and Telnet to ROUTER_2 and still has connectivity with the 10.10.12.0/24 subnet.
<img src="https://i.imgur.com/XvdKKHx.png" height="80%" width="80%" alt="Disk Sanitization Steps"/><br/>
AREA1_PC2 can ping but not Telnet to router 2 and still has connectivity with the 10.10.12.0/24 subnet.
<img src="https://i.imgur.com/tEeC2xt.png" height="80%" width="80%" alt="Disk Sanitization Steps"/><br/>


