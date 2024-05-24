
>**<u>การเปลี่ยน Cell ของ UE</u>
> <font color="#ff0000">Hand Over</font> :** เมื่อ UE อยู่ในสถานะ **<font color="#ff0000">Connected Mode</font>** การย้ายข้าม cell เรียกว่า Hand Over ซึ่งใน Site ต้นทางต้องมีการระบุ neighbor cell ของ site ปลายทางเอาไว้
> **<font color="#00b050">Cell Re-Selection</font> :**  เมื่อ UE อยู่ในสถานะ **<font color="#00b050">Idle Mode</font>** การย้ายข้าม cell เรียกว่า Cell Reselection

> **<u>UE-State</u>** --> [[LTE Mobility Management (MM)]]
> <font color="#00b050">**Idle Mode**</font> คือ สถานะของ UE ไม่มีการใช้ Traffic หรือ Services ใดๆ โดยขั้นตอนการติดต่อของ UE กับ Network คือ การหาความถี่ที่ตัวเองรู้จัก และรับ PLMN ที่สําคัญตามลําดับ Priority เพื่อเข้าอยู่ใน Network เท่านั้น ( ไม่ได้มีการทํา RRC Connection ?)
> <font color="#ff0000">**Connected Mode**</font> คือ สถานะของ UE มีการใช้ Traffic และใน Layer-3 จะพบว่ามีการทํา RRC Connectionและ (E)RAB
> 
>> ทั้ง 2 สถานะ มีผลต่อการทํา Signaling Layer-3 ในการย้ายข้าม Cell ของ UE

- [LTE Cell Camping and Selection Procedure](https://www.techplayon.com/lte-cell-camping-and-selection-procedure/)
- [BasicProcedure_LTE_Cell_Selection](https://www.sharetechnote.com/html/BasicProcedure_LTE_Cell_Selection.html)
- [ Multi Carrier Cell Re-selection in LTE](https://www.techplayon.com/multi-carrier-cell-re-selection-in-lte/)
	>Cell Re selection is a procedure used to change the cell after the UE is camped on a cell and stays in the Idle mode.This procedure is used to let the UE get camped on a cell which has the best radio conditions among all the other cells on which the UE is allowed to camp on.	
	>Cell reselection is done by first checking the :
>		1. PRIORITY
>		2. RADIO LINK QUALITY
>		3. CELL ACCESSIBILITY
- [**LTE Quick Reference**](https://www.sharetechnote.com/html/Handbook_LTE_Cell_Reselection_old1.html)
- 