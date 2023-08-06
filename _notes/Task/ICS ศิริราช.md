
---
Type: Case ร้องเรียน
Main_Issue: 
Trip: False
Date: 2023-08-04
Status:  in progress
Tags: area/BKK/ICSศิริราช
---

>[!Task Track]
>On Site Date::   ==2023-08-04==  to 2023-08-04
>CloseDate::   ==YYYY-MM-DD==

>[!info]
>Location(Coordinate)::  https://goo.gl/maps/kBGGFuqgYZk9Qc4x7

## Issue
- ใช้  SiM ทำ IP-Phone โดย พื้นที่  NT ขาย
- ลูกค้าแจ้งว่า เสียงขาดหาย, Delay 
- 


## Solve & Analyze

>[!VOIP Quality Test]
>[How to Measure VoIP Quality & MOS Score (Mean Opinion Score)](https://obkio.com/blog/measuring-voip-quality-with-mos-score-mean-opinion-score/)
>
  
|        | RSRP | RSRQ | SINR | ping |
| ------ | ---- | ---- | ---- | ---- |
| 4G2300 | good | good | good | Fail |
| 4G2100 | good | good | good | Fail |
| 3G2100 |      |      |      |      | 

- Ping จาก AZQ -> IP Phone  = Fail
- Ping จาก AZQ -> NBTC Server = 30 ms (Avg)
- ทางพื้นที่ ping จากระบบ (SoftSwitch) มี Jitter สูง และ Latency สูง


### LogFile

|                  | Script 1 | Script 2 | Script 3 | Script 4 | Script 5 |
| ---------------- | -------- | -------- | -------- | -------- | -------- |
| Log Name (Tag) 1 |          |          |          |          |          |
| Log Name (Tag) 2 |          |          |          |          |          |
| Log Name (Tag) 3 |          |          |          |          |          |


### Office Document Flow
>หนังสือขออนุมัติ :: 
>เอกสารเบิกเงิน::
>รายงานผล::

## Remark





[[Task Summary]]




