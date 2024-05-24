---
Type: Case ร้องเรียน
Main_Issue: ใช้ SiM ทำ IP-Phone (เสียงขาดหาย, Delay) โดย พื้นที่ NT ขาย
Trip: false
Date: 2023-08-04
Status:
  - done
tags:
  - area/BKK/ICSศิริราช
---

>[!Task Track]
>On Site Date::   ==2023-08-04==  to 2023-08-04
>CloseDate::   2023-08-07

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
- **สรุปได้ว่าปัญหาเกิดจาก Jitter สูงจาก Hop ของ VOIP ไม่ใช่ Network ของ Mobile


### LogFile

|             | data_4g2300MHz_NBTC | data_4g2100MHz_NBTC | trace_ipPhone      | Auto_DL_UL         | data_AllNetw_NBTC  |
| ----------- | ------------------- | ------------------- | ------------------ | ------------------ | ------------------ |
| ICS Counter | 440670093006638900, | 440670093006639285, | 440670093006642415 |                    |                    |
| icsauto     |                     |                     |                    | 478194041155788664 |                    |
| ics2100     |                     |                     |                    |                    | 478194041155786505 |


### Office Document Flow
>หนังสือขออนุมัติ :: -
>เอกสารเบิกเงิน:: -
>รายงานผล:: -

## Remark





[[Task Summary]]




