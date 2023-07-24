---
Type: Special Assignment
Main_Issue: ตรวจสอบ Cell ที่ NOC พบว่าไม่มีทราฟฟิค จำนวน 40,000 cell
Date: 2023-06-12
Status: in progress
Tags:
---

## Issue 
- MNOC พบ Cell 4G2300 ที่ไม่มีทราฟฟิค จำนวน 40,000 cell
- ตรวจสอบว่า cell เหล่านี้ ไม่ได้ Assigned ให้ NTใช้หรือไม่ (Attach Reject) หรือ Cell Priority จาก SIB 3 อยู่ใน Priority ต่ำ จนทำให้ UE ไม่มีความจำเป็นต้องใช้



## Information

- กรุงเทพปริมณฑล นำร่อง10 site แรก  [[seq x cell info สุ่ม bkk10site.xlsx]]
- [Map กรุงเทพปริมณฑล นำร่อง 10 site แรก ](https://www.google.com/maps/d/u/0/edit?mid=1E-aq1XrlyfXmpGhv7Ee8XVDKyfEfHb0&usp=sharing)


### Solve & Analyze

- ควรขอข้อมูลจาก DTN ในส่วนของ cell priority (SIB3)[[MIB SIB]] ของ sector ที่มีปัญหา แล้วตัด priority ตำ่สุดออกไป **เพื่อดูเฉพาะ priority สูง (5,6) ที่ไม่มีทราฟฟิคก่อน** 



|          BKK            | PCI | EARFCN | Result                                             |
| -------------------- | --- | ------ | -------------------------------------------------- |
| THE_CHALLENGER       | 460 | 39050  | ไม่พบ Cell                                          |
| UDOMSUKRICE_COM      | 110 | 39050  | Force Cell manual เข้าไม่ได้, แต่พบ 110 ของความถี่อื่น |
| CHANGWATTANA42       | 122 | 39248  | Force Cell ด้วย script ใช้งานได้, ไม่ Force พบ cell0 แต่ไม่เป็น primary cell |
| PHRAPIN7(TALAD THAI) | 369 | 38852  | Force Cell ด้วย script ใช้งานได้, ไม่ Force พบ cell0 แต่ไม่เป็น primary cell |
| BuengThongLang       | 21  | 39248  | Force Cell ด้วย script ใช้งานได้, ไม่ Force พบ cell0 แต่ไม่เป็น primary cell | 

| South     | PCI | EARFCN | Force to used cell | DL/UL | RSRQ | System   |
| --------- | --- | ------ | ------------------ | ----- | ---- | -------- |
| SKA0499   | 259 | 39248  | difficult          | -     | -    | abnormal |
| SKA0091   | 276 | 38852  | difficult          | Low   | bad  | abnormal |
| JANAM     | 207 | 550    | difficult          | Low   | bad  | abnormal |
| YMWNM     |     |        |                    |       | bad  |          |
| MAYOM     | 205 | 550    | ok                 | pass  | ok   | normal   |
| BSKMM     | 54  | 550    | ok                 | pass  | ok   | normal   |
| BLHNS     | 106 | 550    | can not Force      | Fail  | -    | abnormal |
| KHSTM     | 346 | 550    | ok                 | pass  | ok   | normal   |
| BURGM     | 137 | 550    | ok                 | pass  | ok   | normal   |
| BJBTG     | 285 | 550    | ok                 | pass  | ok   | normal   |
| AIYWM     | 80  | 550    | can not Force      | Fail  | -    | abnormal |
| CTBTM     | 46  | 550    | ok                 | pass  | ok   | normal   |
| KPKNM     | 229 | 550    | ok                 | pass  | ok   | normal   |
| BMLNE     | 74  | 550    | ok                 | pass  | ok   | normal   |
| BPYUM     | 152 | 550    | ok                 | pass  | ok   | normal   |
| SEDYK     | 305 | 550    | ok                 | pass  | ok   | normal   |
| BNWOM     | 285 | 550    | difficult          | Low   | bad  | abnormal |
| BSWNS     | 60  | 550    | ok                 | pass  | ok   | normal   |
| MSCSM     | 486 | 550    | Not Found PCI-486  | N/A   | N/A  | N/A      |
| TTOGM     | 338 | 550    | ok                 | pass  | ok   | normal   |
| SCHFD     | 273 | 550    | ok                 |       | bad  | normal   |
| BARGM     | 199 | 550    | ok                 | pass  | ok   | normal   |
| MTTPA     | 92  | 550    | ok                 |       | ok   | normal   |
| RNGFF     | 48  | 550    | ok                 |       | ok   | normal   |
| KNHGM     | 99  | 550    | ok                 |       | ok   | normal   |
| **HNCGM** | 271 | 550    | ok                 | pass  | ok   | normal   |
| DMMVG     | 46  | 550    | ok                 | pass  | ok   | normal   |
|           |     |        |                    |       |      |          |
|           |     |        |                    |       |      |          |
|           |     |        |                    |       |      |          |
|           |     |        |                    |       |      |          |

### LogFile

|                      | cell 0 force traffic | cell 0 notForce idle | cell 0 notForce Traffic |
| -------------------- | -------------------- | -------------------- | ----------------------- |
| THE_CHALLENGER       |                      | 440670093002658519   |                         |
| UDOMSUKRICE_COM      |                      |                      |                         |
| CHANGWATTANA42       | 440670093002831913   | 440670093002833647   |                         |
| PHRAPIN7(TALAD THAI) | 478239112538617161   |                      |                         |
| BuengThongLang       | 440670093002840275   |                      | 440670093002841217      |
|                      |                      |                      |                         |

- [Cell 0 - AZQ **Template** Report](https://docs.google.com/spreadsheets/d/1Y471JjhJx226q9Xld4N2thOxDWCGuf_WkKYtg4UKOec/edit?usp=sharing)
