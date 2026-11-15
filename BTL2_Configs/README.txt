BTL2 - THIET KE MANG BENH VIEN - CAU HINH BAN NOP CUOI
Nguon: running-config trich truc tiep tu file BTL2_MMT_FinalFinal2.1.pkt (Packet Tracer 9.0.1).

01_Bien_va_WAN         ISP-R, OuterEdgeRouter, HOSP-ASA, InnerEdgeRouter, PE-Main, P-Core, PE-DBP, PE-BHTQ, CE-DBP, CE-BHTQ
02_Core_va_Transit     MLS-A, MLS-A1, MLS-B, MLS-B1, TRANSIT-SW
03_Access_toa_nha      SW1 - SW10
04_Server_farm_va_DMZ  CORE-SW, SF-SW1, SF-SW2, DMZ-SW
05_Site_phu            Core-DBP, Acc-DBP-F1/F2, Core-BHTQ, Acc-BHTQ-F1/F2
06_Thiet_bi_dau_cuoi   IP server/PC, ban ghi DNS, DHCP pool, SSID, vi tri cong/VLAN

Dai dia chi chinh
  Transit ASA - MLS - Inner : 192.168.255.16/28 (ASA .17, MLS-A .18, MLS-A1 .19, MLS-B .20, MLS-B1 .21, Inner .22, HSRP .30)
  DMZ                       : 192.168.254.0/28  (ASA .1, WEB .10, MAIL .11, DNS .12)
  Server farm (VLAN 500)    : 192.168.254.64/26 (gateway HSRP .65)
  VLAN 10-100 phong ban     : 192.168.<VLAN>.0/24, gateway .1 (HSRP)
  VLAN 99 MGMT              : 192.168.253.0/24 | VLAN 200 Guest: 192.168.200.0/23 | VLAN 300 Camera: 192.168.252.0/24 | VLAN 400 Medical: 172.16.0.0/20
  Site phu DBP / BHTQ       : 10.2.0.0/16 / 10.3.0.0/16
  Outside ASA - Outer       : 203.0.113.128/28 | xDSL1 203.0.113.0/30 | xDSL2 198.51.100.0/30 | NAT tinh WEB: 203.0.113.140
