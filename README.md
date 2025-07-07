# EtherCAT Slave Interface Demo ReadMe

> Created on `07/07/2025`
> by Sebastian Villa

### Used Software
TwinCAT Project is using TwinCAT 3.1.**4026**.16

### Used Hardware
3x CX5140 with EtherCAT Slave Optional interfaces

### Variable Declaration for Master\Slave Controller(s)
```format?
iMasterCounter 	AT %Q\I* //integer 		input of Slave from output of Master
lrMasterTemp 	AT %Q\I* //lreal		input of Slave from output of Master
bTrigger 		AT %Q\I* //bool 		input of Slave from output of Master

iSlaveCounter1 	AT %I\Q* //integer		output of Slave to input of Master
lrSlaveTemp1 	AT %I\Q* //lreal		output of Slave to input of Master
bFlag1 			AT %I\Q* //bool			output of Slave to input of Master
iSlaveCounter2 	AT %I\Q* //integer		output of Slave to input of Master
lrSlaveTemp2 	AT %I\Q* //lreal		output of Slave to input of Master
bFlag2 			AT %I\Q* //bool			output of Slave to input of Master
```

---
Aditional Info
- [This Github Repo](https://github.com/sebvc/EtherCAT-Slave-Interface-Demo)
- [Infosys Documentation for EtherCAT Slave Optional Interface (CXxxxx-B110)](https://infosys.beckhoff.com/content/1033/b110_ethercat_optioninterface/1893271819.html?id=1772418640633806881)
- [My Walkthrough](https://github.com/sebvc/EC-Slave-Bridge-Demo/blob/main/Walkthrough.md)

### Code Disclaimer
*All sample code provided by Beckhoff Automation LLC are for illustrative purposes only and are provided “as is” and without any warranties, express or implied. Actual implementations in applications will vary significantly. Beckhoff Automation LLC shall have no liability for, and does not waive any rights in relation to, any code samples that it provides or the use of such code samples for any purpose.*
