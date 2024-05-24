
- [Basic Procedure](https://www.sharetechnote.com/html/BasicProcedures_LTE.html)
	- **Overall LTE Sequenc**
		1. UE is Off
		2. Power On UE
		3. < Frequency Search >
		4. < Cell Search > : Normally a UE would find multiple cells in this process
		5. MIB decoding
		6. SIB deconding
		7. < Cell Selection >
		8. < Initial RACH Process >
		9. < Registration/Authentication/Attach>
		10. < Default EPS Bearer Setup>
		11. Now UE is in IDLE Mode
		12. <(If the current cell become weak or UE moves to another cell regisn) Cell Reselection>
		13. <(When Paging message comes or User make a call) RACH Process>
		14. < Setup Dedicated EPS Bearer >
		15. Receive data
		16. Transmit data
		17. (If UE power is percieved too weak by the network) Network send TPC command to increase UE Tx Power
		18. (If UE power is percieved too strong by the network) Network send TPC command to decrease UE Tx Power
		19. (If UE moves to another cell region) Network and UE perform Handover procedure >
		20. User stop call and UE gets into IDLE mode

- [[4G RACH]]

