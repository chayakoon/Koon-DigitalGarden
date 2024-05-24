>[!LTE Tracking Area Update vs. UMTS Location/Routing Area Update ] 
>In UMTS, **location area and routing area udpates** are only done when the mobile is in idle state, i.e. no physical link is established on the high speed shared-, dedicated- or forward access channel. This makes sense as in these states the RNC in the access network is aware of the location anyway and can report location changes to the core network when necessary. Only once the mobile goes to idle state and the mobile makes the decision to go to another cell on its own without reporting back, routing and location area updates come into play if the new cell is outside the current area.
>   Remark : _RUA is PS Domain equivalent of  LAU_
>In LTE, the corresponding procedure is called a **tracking area update**. The first difference to the LAU and RAU of UMTS is that the mobile can have a list of several valid tracking areas and an update only has to be made if the new cell is in a tracking area that is not part of that list. So far so good. TS 23.401 chapter 5.3.3.0 says, however, that a tracking area update is made in **both idle and connected state**. Quite a surprise to me so I wondered why an update is necessary in the connected state!?
>The answer to that question can be found in the message sequence charts for handovers. For example: during an X2 handover, which is directly negotiated between two base stations, the Mobility Management Entity (MME) in core network is only informed of the handover after it has taken place. Also, there's no direct communication between the MME and the mobile device during the handover procedure. That means that in case the new cell is in a new tracking area, the mobile has to update its tracking area list as that information was not contained in the handover messaging.
>From a logical point of view that also makes sense. Traking areas are administered by the core network (by the Non Access Stratum) while handovers are performed by the access network. Also, the signaling does not interrupt the user data transfer so there are no side effects of performing this procedure in connected mode and while transferring data.

- LAU (3G) จะทำ เมื่อ 
	- UE อยู่ใน idle state
	- UE เข้าสู่ LA ใหม่
	- เมื่อเวลาผ่านไปช่วงเวลาหนึ่ง หลังจาก  UE อยู่ใน idle Mode
	- เปิดเครื่องใหม่
- TAU (4G) จะทำ เมื่อ
	- UE อยู่ทั้ง idle และ connected state
	- 


## Location Area Update Reject Cause 
(GMM Cause Information Element)  [Protocol Control](https://rfmw.em.keysight.com/rfcomms/refdocs/gsm/gprsla_protocol_stack_conf.html#BABBJAAC)

| Cause Value (decimal) | Cause Value (bits) | Cause                                   |
| --------------------- | ------------------ | --------------------------------------- |
| 2                     | 00000010           | IMSI Unknown                            |
| 3                     | 00000011           | Illegal MS                              |
| 4                     | 00000100           | IMSI UKNOWN IN VLR                      |
| 5                     | 00000101           | IMEI NOT ACCEPTED                       |
| 6                     | 00000110           | Illegal ME                              |
| 7                     | 00000111           | GPRS Services Not Allowed               |
| 8                     | 00001000           | GPRS/Non-GPRS Services Not Allowed      |
| 9                     | 00001001           | MS Identity Cannot Be Derived           |
| 10                    | 00001010           | Implicitly Detached                     |
| 11                    | 00001011           | PLMN Not Allowed                        |
| 12                    | 00001100           | Location Area Not Allowed               |
| 13                    | 00001101           | Roaming Not Allowed In This LA          |
| 16                    | 00010000           | MSC Temporarily Not Reachable           |
| 17                    | 00010001           | Network Failure                         |
| 22                    | 00010110           | Congestion                              |
| 32                    | 00100000           | Service Option Not Supported            |
| 33                    | 00100001           | Requested Service Option Not Subscribed |
| 34                    | 00100010           | Service Option Temporarily Out of Order |
| 48                    | 00110000           | Retry Upon Entry Into A New Cell        |
| 95                    | 01011111           | Semantically Incorrect Message          |
| 96                    | 01100000           | Invalid Mandatory Information           |
| 97                    | 01100001           | Message Type Nonexistent                |
| 98                    | 01100010           | Msg Type Incompatible With Prot State   |
| 99                    | 01100011           | Information Element Nonexistent         |
| 100                   | 01100100           | Conditional IE Error                    |
| 101                   | 01100101           | Msg Incompatible With Protocol State    |
| 111                   | 01101111           | Protocol Error, Unspecified             |





