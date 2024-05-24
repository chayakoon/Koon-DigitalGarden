---
Type: Case ร้องเรียน
Main_Issue: IP-Phone เสียงสนทนา ขาดหาย
Trip: "false"
Date: 2023-11-09
Status: done
tags:
---

>[!Task Track]
>On Site Date::   ==2023-11-10==  to 2023-11-10
>CloseDate::   ==2023-11-14==

>[!info]
>Location(Coordinate)::  รามคำแหง 40 https://maps.app.goo.gl/GCwZeDD6HHNMPw7p7
>


## Issue
ลูกค้านำซิมไปใช้งาน IP-Phone ในพื้นที่จำนวน 100 เลขหมาย พบปัญหาระหว่างโทร **เสียงสนทนาจะขาดหาย (ก่อนหน้านี้เคยใช้งานได้ปกติ)** เบื้องต้นทดลอง Reset แล้ว แต่ยังพบปัญหาอยู่

## Solve & Analyze
- KT ใช้ SIM สำหรับ IP Phone ที่ชั้น 1 จำนวน <10  SIM และอยู่ในชุด 30 SIM,  ชั้น 4 จำนวน >90 SIM ทั้ง 2 ชั้น มีอาการเสียงขาดหายเหมือนกัน
- Bandwidth ของ Mobile มีปัญหาหรือไม่ ? สำหรับอัตราประมาณ 100kbps ของ [VOIP Bandwidth](https://www.cisco.com/c/en/us/support/docs/voice/voice-quality/7934-bwidth-consume.html)

|         | Max Jitter | DL (Mbps) | UL (Mbps) | BLER | RSCP(RSRP) | RSRQ | SINR | CQI |
| ------- | ---------- | --------- | --------- | ---- | ---------- | ---- | ---- | --- |
| 3G 2100 |            |           |           |      |            |      |      |     |
| 4G 2100 |            |           |           |      |            |      |      |     |
| 4G 2300 |            |           |           |      |            |      |      |     |

- [**What Increases Latency?**]([VoIP Jitter and Latency: Causes and How to Troubleshoot (getvoip.com)](https://getvoip.com/blog/voip-jitter-and-latency/#latency-increase))
	- Location
	- Network hardware  - Router ที่ล้าสมัย Router จํานวนมากมีความเร็วในการประมวลผลและการสนับสนุนแบนด์วิดท์ที่ จํากัด ซึ่งอาจนําไปสู่เวลาแฝงในระหว่างกิจกรรมที่มีข้อมูลสูงเช่นการสตรีมและการโทร VoIP มองหาRouter ที่รองรับ WiFi 6 (802.11ax) ขึ้นไป
	- **Wireless networks:** 
	- **Network software and configuration:** Software Firewalls that are improperly set, quality of service settings, or NAT settings can delay the transmission of data
	- **Congestion:** อุปกรณ์จํานวนมากเกินไปที่ใช้ข้อมูลพร้อมกันบนเครือข่ายท้องถิ่นจะทําให้ความสามารถของเราเตอร์ในการส่งและรับแพ็กเก็ตข้อมูลเร็วขึ้น สิ่งนี้จะจํากัดแบนด์วิดท์และความเร็วข้อมูลที่มีอยู่ของอุปกรณ์แต่ละเครื่อง หากเครือข่ายของคุณมีผู้ใช้หลายคนที่มีส่วนร่วมในกิจกรรมที่มีข้อมูลสูง เช่น การเล่นเกม การประชุมทางวิดีโอ หรือการโทรผ่าน VoIP เครือข่ายของคุณอาจแออัดเกินไป ในการแก้ไขปัญหาคุณอาจต้องใช้เราเตอร์ที่อัปเดตหรือเราเตอร์หลายตัว
- [**What Increases Jitter?**]([VoIP Jitter and Latency: Causes and How to Troubleshoot (getvoip.com)](https://getvoip.com/blog/voip-jitter-and-latency/#increases-jitter))
	- **Network congestion:** แบนด์วิดธ์ไม่เพียงพอที่จะจัดการกับการโทร VoIP จะทําให้แพ็กเก็ตถูกทิ้งหรือจัดส่งไม่เป็นระเบียบ
	- **Wireless networks:** SINR, RSCP
	- **Outdated hardware:** 
	- **Inefficient network prioritization:** การตั้งค่าคุณภาพการบริการ (QoS) ของเราเตอร์ช่วยให้คุณสามารถจัดลําดับความสําคัญของอุปกรณ์หรือประเภทของข้อมูลบางอย่างได้ ด้วยวิธีนี้เมื่อเครือข่ายแออัดเราเตอร์จะให้ความสําคัญกับอุปกรณ์และประเภทข้อมูลที่คุณระบุ หากต้องการจัดลําดับความสําคัญของข้อมูลบางประเภท
- 

### LogFile

|                  | 3G_2100_DL_UL                                                 | 2100_DL_UL                                                 | 2300_DL_UL                                               |
| ---------------- | ------------------------------------------------------------- | ---------------------------------------------------------- | -------------------------------------------------------- |
| 3G2100_KT_Floor4 | 440670093015104177 [[(3G2100_KT_Floor4) (3G_2100_DL_UL).azm]] |                                                            |                                                          |
| 4G2100_KT_Floor4 |                                                               | 440670093015103734 [[(4G2100_KT_Floor4) (2100_DL_UL).azm]] |                                                          |
| 2300_KT_Floor4   |                                                               |                                                            | 440670093015102981 [[(2300_KT_Floor4) (2300_DL_UL).azm]] |
|                  |                                                               |                                                            |                                                          |
*กรณี Log Indoor QGISไม่สามารถเรียกใช้ตรงจาก server ได้ ต้อง Load มาไว้ที่ Local ก่อน*

### Office Document Flow
>หนังสือขออนุมัติ :: 
>เอกสารเบิกเงิน::
>รายงานผล:: [[คทป.2(205)-รายงานการตรวจสอบ(กรุงเทพธนาคม).pdf]]

## Remark
- [สาเหตุหนึ่งที่ทำให้เสียงสนทนาขาดหาย มีเสียงสะท้อน](http://www.voip4share.com/forum-f13/topic-t4806.html)
- [Jitter](https://tips.thaiware.com/1308.html)
- [How to reduce RTT](https://www.stormit.cloud/blog/what-is-round-trip-time-rtt-meaning-calculation/#reduce-rtt)
- [Acceptable Jitter and Latency for VoIP](https://getvoip.com/blog/voip-jitter-and-latency/#acceptable)
	- One-way latency on VoIP calls should not exceed 150ms
	- jitter is below 30 ms.




[[Task Summary]]




