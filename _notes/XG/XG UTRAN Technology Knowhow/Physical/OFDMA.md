
[[LTE Resource]]


- [LTE FRAME STRUCTURE & RB (RESOURCE BLOCK)](https://www.youtube.com/watch?v=k6GHl_btjcE) 
	- [00:09:31](https://www.youtube.com/watch?v=k6GHl_btjcE&t=512#t=08:31.83) format
	- [00:14:15](https://www.youtube.com/watch?v=k6GHl_btjcE&t=855#t=14:15.31) spacial subframe
	- ![[LTE-Frame-1.png|1000]]        [[LTE-Frame-2.png]]      [[LTE-Frame-3.png]] 
	- [[LTE เรียงสรุป.pdf]]
- [What is a Cyclic Prefix in OFDM?](https://www.youtube.com/watch?v=AJg57AEBtNw)
- [LTE Basics Part I - OFDMA and LTE Frame structures](https://www.youtube.com/watch?v=pArdrXM5qLM) รูปชัดเจน
- [[CBRS LTE Technology for the Enterprise.jpg]]     [CBRS](https://www.arubanetworks.com/assets/wp/WP_CBRS-The-Radio.pdf)
- [LTE Physical Layer](https://www.youtube.com/watch?v=E7GnlmxGhXc&t=13s)
- [4G LTE Frame Structure - Part of 4G Course (Link in description)](https://www.youtube.com/watch?v=yuheccefqyU)
- [LTE Basics Part I - OFDMA and LTE Frame structures](https://www.youtube.com/watch?v=pArdrXM5qLM)
- [How eNodeB decides resource elements for Control and Data region in LTE ? (CQI)](https://www.youtube.com/watch?v=JMsHuWpzOb0&t=174s)
- [LTE Tutorial: Understanding the LTE Resource Grid  **PSS, SSS, BCH, PDSCH, PDCCH, PHICH, and PCFICH.** Understand the role of each channel](https://www.youtube.com/watch?v=tGGfsIjG910) <-- สำคัญมาก
- [2.1 LTE Physical Resources Block (youtube.com)](https://www.youtube.com/watch?v=aXt9HWwjPME))

- $15\space kHz * 12\space subCarrier = 180\space kHz$
- $\frac{20\space MHz}{180\space kHz}=111\space PRB(\approx 100\space PRB)$

- ![[PRB RB RE Structure.png|400]]
- [Transmission Time Interval (TTI) - LTE 4G Vs 5GNR](https://pdfcoffee.com/transmission-time-interval-tti-lte-4g-vs-5gnr-pdf-free.html)
	- What is meant by TTI ?
		- TTI is LTE's smallest(minimum) unit of time in which Base Station is capable of scheduling any user for uplink or downlink transmission
		- One TTI duration corresponds to a number of consecutive symbols in the time domain in one transmission direction
		- During Each TTI Base Station will assign resources and inform user where to look for its downlink data through PDCCH channel
	- TTI in LTE 4G: 
		- TTI in LTE is 1ms 
		- minimum scheduling time for Uplink or Downlink transmission is one subframe 
		- TTI is made up of two slots หรือพูดได้ว่า 1 TTI = 1 SubFrame (14 OFDM Symbols)
		- Transmission Time Interval (TTI) - LTE 4G vs 5GNR
	- TTI in 5GNR: Here in 5G it is completely different from 4G, 
		- a new concept Mini Slot has introduced 
		- Minimum TTI in 5GNR is Mini Slot i.e., minimum scheduling time for Uplink or Downlink transmission A standard slot has 14 OFDM symbols A mini-slot is shorter in duration than a standard slot and located anywhere within the slot
		- Mini Slot is made up of 2 , 4 or 7 OFDM Symbols regardless of numerology
		- Since URLLC is one of three primary 5G use cases and is achieved partially through Mini-slots which is non-slot based scheduling
		- Low latency is achieved through Mini-slots\
- [Wifi OFDM 802.11a,OFDMA 802.11ax ](https://www.youtube.com/watch?v=gjdHpZWxujA)
	- [[OFDM 802.11a.png]]    [[OFDMA 802.11ax.png]]
- [[RadioAccessEvo.png]]
- [LTE: MIMO and OFDM](https://www.youtube.com/watch?v=tM1Ih5KD0GI&list=WL&index=28&t=11s)
- 