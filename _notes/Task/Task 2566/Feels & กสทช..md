---
Type: Case ร้องเรียน
Main_Issue: Feels แจ้ง กสทช. ว่าได้รับ service ไม่ดี จาก NT2
Date: 2022-12-12
Status:
  - done
Trip: true
tags:
  - Feels
  - MVNO
  - กสทช.
---


>[!Task Track]
>On Site Date::   2022-12-14  to 2022-12-17
>CloseDate::   2022-12-26

>[!info]
>Location(Coordinate)::  อุดรธานี, ขอนแก่น, โคราช


## Issue



## Information



## Solve
ดำเนินการโดยทำ Script ให้เหมือน Script ของ กสทช.
![[7498.jpg]]
##### 14 Dec 2022 อ.บ้านดุง จ.อุดรธานี ปัญหา 3G - iKool และ 4G - Feels
- Sim NT (sim-test), script - 3G_NBTC  Tag - Bandung / ไม่พบปัญหา / กสทช. ปิดเคส
- Sim NT (sim-test), script -Auto_NBTC  Tag - Bandung / ไม่พบปัญหา 
- Sim Feels, script -Auto_NBTC_SimFeels  Tag - Bandung / พบว่า...
- พบว่า SimFeels ของ กสทช.  เป็น 520 15,  SimFeels ของ NT  เป็น 520 17 จึงไม่สามารถเทียบได้
- กสทช. แจ้งว่า ประเด็นอยู่ที่ กสทช. ต้องการเปรียบเทียบคุณภาพบริการ ของ MVNO กับ NT ให้ได้รับบริการเหมือนกัน
- sim feels 15 ของ กสทช ใช้ได้ทุก network -   กรณีที่ รายงาน กสทช พบว่า Feels ใช้แต่ Network 4g2100 ไม่จับใช้ 4g2300 สันนิษฐานว่า มีสาเหตุจาก ใช้ Script ที่วัดโดยไม่มีการเว้นช่วงทราฟฟิค ในแต่ละคำสั่ง ทำให้หลังจากทำ voice 3g2100 แล้ว ue จะหา network 4g แรก ที่เจอ ซึ่งต้องขึ้น core ของโครงข่าย 2100 เดิม (SBN)เหมือนกันก่อนและเมื่อไม่มีช่วงเว้นทราฟฟิคให้ ue เข้าสู่โหมด idle ue ก็จะจับใช้แต่network เดิม อีกทั้ง sim feels ของ กสทช ยังมี imsi เป็น 520 15 Home network จึงเป็น 52015
-  sim feels 17 ของ NT ไม่สามารถใช้ data ของ 3g2100 และ 4g2100
##### 15 Dec 2022 
- ##### เช้า ต.หนองแวง อ.พระยืน จ.ขอนแก่น ปัญหา 3G - iKool
- Sim NT (sim-test), script - 3G_NBTC  Tag - Phrayaen / ไม่พบปัญหา / กสทช. ปิดเคส
- Sim Feels17, script -Auto_NBTC_SimFeels  Tag - Phraen, Phrayaen2
- Sim Feels15, script -Auto_NBTC_SimFeels52015  Tag - Phrayaen (ยืม กสทช. มา test)
- ##### บ่าย ต.โนนสวรรค์ อ.หนองเรือขอนแก่น ปัญหา 3G - iKool
- Sim NT (sim-test), script - 3G_NBTC  Tag - Nonesawan KKN / ไม่พบปัญหา / กสทช. ปิดเคส
- Sim Feels15,  Script : Auto NBTC SimFeels52015,  Tag : Nonesawan KKN
- Sim NT(sim-test), script - Netmonitor  Tag - Nonesawan KKN
##### 16 Dec 2022 ปากช่อง ปัญหา 3G - iKool
- Sim NT (sim-test), script - 3G_NBTC  Tag - Pakchong / ไม่พบปัญหา / กสทช. ปิดเคส
- Sim Feels15, script -Auto_NBTC_SimFeels52015  Tag - Pakchong_Sim NT ตั้งชื่อผิดเป็น Sim NT   พบว่าไม่ยอมจับ 2300แต่เครื่อง iPhone จับ 2300ได้ -   จึงลองอยู่กับที่ ใกล้ไซด์ 2300 โดยใช้ netmonitor 5 นาที พบว่าก็ยังไม่ยอมจับโดย แต่ iphone จับได้ (pci 17)  จึงลองอยู่กับที่ ใกล้ไซด์ 2300 โดยใช้script 4G-2300-NBTC ให้ force 2300 พบว่าสามารถจับ pci 17 2300ได้
- 

### Remark
- ##### Script 
	- 3G_NBTC
	- 3G_4G_2100_NBTC_simFeels      ใช้ sim Feels 52017 ของฝ่ายตลาดNT 
	- 4G_2300_NBTC                            เพื่อ Test ว่า sim Feels 520 15 และ 17 ใช้ 2300 ได้ไหม
	- Auto_NBTC                                  ใช้ sim หลายตัว
	- Auto_NBTC_simFeels                   ใช้ sim Feels 52017 ของฝ่ายตลาดNT 
	- Auto_NBTC_simFeels52015         ใช้ sim Feels 52015 ของ กสทช
	- Auto_NBTC_sim_nt               ใช้ sim Feels 52017 ของฝ่ายตลาดNT และวันที่16 ตั้งชื่อ tag ผิด sim

[[Task Summary]]




