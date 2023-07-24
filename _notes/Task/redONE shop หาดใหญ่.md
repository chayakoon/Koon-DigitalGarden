

---
Type: Case ร้องเรียน
Main_Issue: Data Throughput ไม่สามารถให้บริการ
Date: 2022-11-16
Trip: true
Status: done
Tags: redONE, MVNO, area/SKA/หาดใหญ่
---

>[!Task Track]
>On Site Date::   2022-11-24  to 2022-11-25
>CloseDate::   2022-12-13

>[!info]
>Location(Coordinate)::  [Redone AG Hatyai](https://goo.gl/maps/d17VzVtweV6TqLPo7)


## Issue
- Shop redOne หาดใหญ่ จับ 4G2300 ไม่ยอมจับ 4G2100  
- redOne อยากให้จับ 4G2100 
- Repeater 4G2100 ? กสทช. ตรวจพบ



## Information

- หนังสือ redOne --> [[1381(redONE).pdf]]  

**LogFile**

|                           | Auto_Red One       | 4G21002300_Red one | 4G2100_Red one     | 4G2300_Red one     | 3G2100_Red one     |
| ------------------------- | ------------------ | ------------------ | ------------------ | ------------------ | ------------------ |
| Hatyai shop Route         | 478194041133922488 | 478194217227581507 | 478194217227584798 |                    | 440670092984776764 |
| Hatyai shop route 2       | 478194041133924790 | 478194217227583943 |                    |                    | 440670092984779180 |
| Hatyai shop Front         | 478194041133927545 | 478194217227586664 | 478194217227587616 |                    | 440670092984781964 |
| Hatyai shop inside        | 478194041133929451 | 478194217227588630 | 478194217227589514 |                    | 440670092984783846 |
| Hatyai shop inside done 1 | 478194041134002382 |                    |                    | 478194217227661548 |                    |
| Hatyai shop inside done 2 |                    |                    | 478194217227663508 | 478194041134004375 |                    |

## Solve & Action
##### ภายใน Shop
- ใน shop RSRP ของโครงข่าย 4G-2300MHz (PCI 431,201,176) และ 4G-2100MHz(PCI 58) มีค่าใกล้เคียงกัน เครื่องลูกข่ายของลูกค้าที่เป็น Auto Network จึงเข้าใช้งาน 4G2300MHz ตาม Priority ที่กำหนดไว้ รวมถึงคุณภาพสัญญาณของ 3G มีค่าอยู่ในระดับพอใช้งานได้ จึงเกิดการสลับใช้งาน Network 4G-2300MHz  กับ 3G-2100 MHz อยู่บ่อยครั้ง 
- 4G2300 - SINR 2,  ทำ MOD QPSK-16QAM ( LTE3.9 ไม่ขึ้น  LTE+ Advance )  Throughput ตำ่สุด
- 4G2100 - SINR 8,  ทำ MOD 16-256QAM 
- 3G2100 - Throughput ดีกว่า 4G2300
- หลัง DTN ปรับแก้โครงข่าย ( PCI 178 ) ยังคงให้ Throughput ตำ่กว่า 3G4G-2100 แต่แก้ปัญหา Swing ไป 3G ได้

##### ภายนอก Shop
- ทดสอบ**_ภายนอก_**อาคาร โดยทำการ drive test  บนถนนรอบอาคารศูนย์บริการ red One ในรัศมี 1 km โดยประมาณ พบว่า site ทำงานได้ตามมาตรฐาน LTE แต่สัญญาณไม่สามารถให้คุณภาพที่ดีตรงจุดที่ตั้งของ ศูนย์บริการ red One และมีค่า SINR บริเวณหน้าอาคารศูนย์บริการ red One ต่ากว่าบริเวณอื่นๆ ที่รับสัญญาณจาก Cell เดียวกัน



[[Task Summary]]





## Report
- [[redOne Route สิ่งที่ส่งมาด้วย.pptx]]
- [[คทป.2(212)-รายงานผลฯRedOne(สงขลา).pdf]]
- [[353538111338267-24_11_2022-12_42_21 (Hatyai shop route 2).azm]]
- [[353538111338267-24_11_2022-12_21_02 (Hatyai shop route) 1.azm]]
- [[Cell 4G2300 ตำบลหาดใหญ่.txt]]
- [[Cell 4G2100 ตำบลหาดใหญ่.txt]]