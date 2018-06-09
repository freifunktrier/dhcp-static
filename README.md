Statische IPv4-Vergabe im FFTR-DHCP
===================================

[Subnetze](http://trier.freifunk.net/)

 Wir haben nun bis zu 16 Segmente mit entsprechenden IPv4-Ranges 
* seg_00 10.172.0.0 - 10.172.15.255  
* seg_01 10.172.16.0 - 10.172.31.255  
* seg_02 10.172.32.0 - 10.172.47.255  
* seg_03 10.172.48.0 - 10.172.65.255  
* seg_04 10.172.64.0 - 10.172.79.255  
* seg_05 10.172.80.0 - 10.172.95.255  

Die dann folgenden Ranges sind noch nicht vergeben.
 Die ersten 255 Adressen eines jeden Segments werden nicht dynamisch vergeben. Diese sollen in erster Linie für Infrastruktur genutzt werden.
 Die static-Adressen hier werden vom DHCP-Server aus dem dynamic-Pool heraus genommen. (hoffe ich mal)
 Sollte also jemand aus seg_05 sein Gerät ansprechen wollen, muss auch die feste IPv4 in das Segment_05 umgezogen werden. 

IP-Bereiche: 
* 1-9 Hosts mit Netzmonitor-Funktionen 
* 10 - 20 für GWs 
* 21 - 50 Infrastruktur 
* 51 - 149 Customer ohne Antrag (first-come, first-serve)
* 150 - 254 auf Antrag (Verpflichtung zur Freigabe, sobald 3 Monate ungenutzt) 
