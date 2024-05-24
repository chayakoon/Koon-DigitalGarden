- Link
	- [LTE Drive Test Parameters](https://telecom-knowledge.blogspot.com/2016/09/lte-drive-test-parameters.html)
	- [Mobile Signal Strength Recommendations](https://wiki.teltonika-networks.com/view/Mobile_Signal_Strength_Recommendations)
	- [LTE RSSI, RSRP and RSRQ Measurement](https://www.cablefree.net/wirelesstechnology/4glte/rsrp-rsrq-measurement-lte/)
	- [**4G/LTE - PHY Measurement**](https://www.sharetechnote.com/html/Handbook_LTE_RSRP_EPRE_TotalPower.html)
	- [LTE Radio Primer Part 7: DL Cell Reference Signals, RSRP & RSRQ](https://www.youtube.com/watch?v=XAtQq7zHvQ0)
- [RSSI and SNR](https://www.youtube.com/watch?v=veIo02JhPn4) ความสัมพันธ์ของ RSSI และ SINR ที่มีต่อผลกระทบต่อความสามารถในการเขื่อมต่อโครงข่าย - [00:02:54](https://www.youtube.com/watch?v=veIo02JhPn4&t=174#t=02:54.32)  ถ้า RSSI - Noise > 20 จะถือว่าใช้งานได้
- [SINR and CQI calculation](https://comtech.vsb.cz/qualmob/sinr_lte.html)
- [CQI](https://www.sharetechnote.com/html/Handbook_LTE_CQI.html)     [LTE CQI Vs PMI Vs RI-Difference Between LTE CQI,PMI,RI](https://www.rfwireless-world.com/Terminology/LTE-CQI-vs-PMI-vs-RI.html)
- [[CQI, MCS, Modulation.png]]    [[SINR CQI MCS.jpg]]
- PRB Modulation and Coding Scheme (MCS)
- [[Modulation vs Coverage.png]]


| Signal quality: | **RSRP (dBm)**   | **RSRQ (dB)**   | **SINR/CINR (dB)** | RSSI (dBm) |     |
| --------------- | ---------------- | --------------- | ------------------ | ---------- | --- |
| **very good**   | >= -80           | >= -10          | >= 20              | >-65       |     |
| **good**        | from -80 to -90  | from -10 to -15 | from 13 to 20      | -65 to -75 |     |
| **bad**         | from -90 to -100 | from -15 to -20 | from 0 to 13       | -75 to -85 |     |
| **very bad**    | <= -100          | < -20           | <= 0               | <-85       |     |

>[!info]  RSSI  - **Reference Symbol Signal Intentity**  (wideband Power)
>The RSSI-Recieve Signal Strenght Indicator is Recieve **Signal** Power in milliWatt and is measure in dBm
> _Is Serving cell power includede Interference & Noise_
>The 'staircase' signal quality icon correlates as follows with the RSSI value (dBm) -- <font color="#ff0000">รูปแสดงสัญญาณบนโทรศัพท์มือถือ คือค่า RSSI</font>
  ** RSSI = WidebandPower = *Noise + ServingCellPower +  Interference Power* **
>So, without noise and interference, we have that 100% DL PRB activity:
>$$
  RSSI(dBm)=12*N*RSRP
>$$
>- **RSRP is the received power of 1 RE (3GPP definition)** average of power levels received across all Reference Signal symbols within the considered measurement frequency bandwidth
>- **RSSI** is measured over the entire bandwidth
>- **N: number of RBs across the RSSI** is measured and depends on the BW

>[!SINR]  SINR - Signal to Interference Noise Ratio
>**Signal** to interference Noise Ratio
>$$
>SINR(dB)=\frac{P}{I+N}
>$$
>[[Interference Cause.jpg]]
> [Diffraction interference patterns with phasor diagrams](https://www.youtube.com/watch?v=NazBRcMDOOo&list=WL&index=23&t=240s)
> [RTWP (Received Total Wideband Power)/ Uplink Interference in KPI Optimization](https://www.youtube.com/watch?v=UzgipEDcdiM)
> 

>[!RSRP]   RSRP - Recieved Signal Recieved Power
>In other words RSRP (Reference Signal Receive Power) is the average power of Resource Elements (RE) that carry cell specific Reference Signals (RS) over the entire bandwidth, so RSRP is only measured in the symbols carrying RS.
>- RSRP is the average received power of a single RS resource element.
>- UE measures the power of multiple resource elements used to transfer the reference signal but then takes an average of them rather than summing them.
>- Reporting range -44…-140 dBm
>$$
>RSRP(dBm) = RSSI - 10\log (N*12)
>$$
>- **N = Number of PRBs (Physical Resource Blocks**)


>[!RSRQ] RSRQ - Recieved Signal Recieved Quality 
>	[RSRQ value might be used for some scenarios such as **cell selection, cell reselection and handover.**](https://telecompedia.net/rsrq/)
>$$
>RSRQ(dB)=\frac{RSRP}{\left( \frac{RSSI}{N} \right)}=\frac{N*RSRP}{RSSI}
>$$
>- **N = Number of PRBs (Physical Resource Blocks**)
>- ![X](https://telecommunications4dummies.com/wp-content/uploads/2021/07/image.png)
>- **RSSI = noise + serving cell power + interference power during RS symbol**
>- **So we have that RSRQ depends on serving cell power and the number of Tx antennas**


- ![[lte-singal_QLTY_1.png]]
- ![[LTE-singal_QLTY_2.png]]
- [LoRa/LoRaWAN tutorial 10: **RSSI and SNR**](https://www.youtube.com/watch?v=RpTw1fGhI68)
	- ![[Screen Shot 2567-05-19 at 06.21.20.png|]]