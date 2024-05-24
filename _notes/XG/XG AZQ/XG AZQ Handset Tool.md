##### Sony Experia
- [คู่มือเครื่อง Sony Experia]([userguide_TH_J8110-J8170-J9110_2_Android10.pdf (sonymobile.com)](https://www-support-downloads.sonymobile.com/j8110/userguide_TH_J8110-J8170-J9110_2_Android10.pdf))
- [วิธีการติดตั้ง Firmware และ Azenqos - Sony Xperia 1 ll](https://www.youtube.com/watch?v=xdqedURM7ys)

##### ติดตั้ง App มือถือ Azq
- [Link](https://apk.azenqos.com)
- User : AZQ     PWD : AZQ

#####  DT Tool Manual
- [AZQ User Guide (TH).pdf](https://drive.google.com/file/d/1aqn7KVkNhRbke8TtzSGwcu-vGcsh3yym/view?usp=sharing)

##### Facebook account AZQ

| No. | User                            | PWD     | facebook App Name |
| --- | ------------------------------- | ------- | ----------------- |
| 1   | efqrausbti_1595564972@tfbnw.net | tot1234 | APITest           |
| 2   | rlxwsnnzcf_1595564969@tfbnw.net | tot1234 | APITest           |
| 3   | elfqumiesw_1595564966@tfbnw.net | tot1234 | APITest           |
| 4   | hidtblmasj_1595564974@tfbnw.net | tot1234 | APITest           | 




##### DT Tools Azq File
- File ที่  upload แล้ว จะอยู่ใน **โฟลเดอร์  Diag_Log**
- File ที่  Deleat  แล้ว จะอยู่ใน **โฟลเดอร์  AZQ_TRASH**


##### MOS
- MOS - Mean Opinion Score (คะแนนความคิดเห็นเฉลี่ย)
- [AZQ User Guid หัวข้อ  Doing POLQA MOS voice quality tests](https://docs.google.com/document/d/18GZAgcs3jRFdWqfvAqmQicvYlXRk6D0WktqWmd5iwwo/edit#heading=h.2qy8f5fdd8g2)
- [POLQA MOS Guide](https://docs.google.com/presentation/d/1tMG_bjvZ9ZfVxuJS4ubrwigBSdHvFnbtIOs_huyI9ag/edit?usp=sharing](https://docs.google.com/presentation/d/1tMG_bjvZ9ZfVxuJS4ubrwigBSdHvFnbtIOs_huyI9ag/edit?usp=sharing)


![[MOS_Log_Diagram.png]]


- wait หลังคำสั่ง MOS  ฝั่ง B ควรมากกว่า ฝั่ง A  ( เช่น A=3, B=5 )
- Duration ควรมี  60sec ( ถ้า 3 Loop ก็ใช้ Loop ละ 13 sec )

![[MOS_Script_Config.png]]


##### ใส่ Cell File ในเครื่องมือวัด AZQ
- [การใส่ cell file ในเครื่องมือวัด](https://drive.google.com/file/d/13AbJKLz0cyKm2HilizFtqlAen9HQrynu/view?usp=sharing) ใช้ .txt,  .csv
- [[AZQ_3G_Cell_Pattern.xlsx]]
- [[AZQ_4G_Cell_Pattern.xlsx]]


##### Script Command 
- **HTTP DL**  5M, 1G   **HTTP UL** ไฟล์สุงสุด 1GB, ตั้งเท่าไรก็ได้ เครื่องจะ gen ให้
- [**Notes and variables in script**](https://docs.google.com/document/d/18GZAgcs3jRFdWqfvAqmQicvYlXRk6D0WktqWmd5iwwo/edit#heading=h.k9bek9g4bra3)
- 
##### อ่าน Script AZQ (Network Mode, Band)

| Network Mode     | =   | 
| ---------------- | --- |
| WCDMA            | 0   |
| LTE              | 6   |
| LTE_WCDMA_GSM    | 4   |
| NR_LTE_WCDMA_GSM | 5   |



| Band Lock        | LTE,WCDMA Bands = | 
| ---------------- | ----------------- |
| LTE B1           | 1                 |
| LTEB 40          | 549755813888      |
| LTE B1,B40       | 549755813889      |
| WCDMA B2100      | 4194304           |
| WCDMA B850       | 67108864          |
| WCDMA B2100,B850 | 71303168          |










##### Parameter ในเครื่องมือวัด
- [[Tab LTE RADIO 4G2100.jpg]]  
- 