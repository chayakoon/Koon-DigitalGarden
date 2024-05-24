( Hybrid แปลว่า "Combination of something" ) 

![[messageImage_1715588327750.jpg]]
- _ACK_ : Aknowledge,             NACK : Negative Acknowledge


[Wiki - Hybrid automatic repeat request]([Hybrid automatic repeat request - Wikipedia](https://en.wikipedia.org/wiki/Hybrid_automatic_repeat_request))
>[!HARQ]
>Hybrid automatic repeat request (Hybrid ARQ or HARQ) is a combination of high-rate forward error-correcting coding and ARQ error-control. In standard ARQ, redundant bits are added to data to be transmitted using an error-detecting (ED) code such as a cyclic redundancy check (CRC). HARQ Process A little bit different mode of HARQ process is used depending on whether it is for FDD or TDD and whether it is for Uplink and Downlink. But I will talk only about FDD case. 
>**In FDD, we are using 8 HARQ process**
> 	i) For Downlink : Asynchronous Process 
> 		a) it can use the 8 HARQ processes in any order (Asynchronous Process).
> 		 b) UE does not know anything about HARQ process information for DL data before it gets it. So Network send these information (Process ID, RV) in PDCCH (DCI, Refer to DCI section of this site). 
> 	ii) For Uplink : Synchronous Process 
> 		a) it have to use the specific process in a specific subframe (Synchronous Process). UE has to use the same HARQ process number every 8 subframes. 
> 		b) Since UE have to use specific HARQ process ID at specific subframe, the reciever (eNode B) knows exactly which HARQ process comes when. And eNodeB can also knows about RV because UL Grant (DCI 0) from eNodeB can specify RV using MCS field. 
> 		c)it has two mode of operation : Adaptive and Non-Adaptive HARQ

