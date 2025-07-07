# EtherCAT Slave Interface Demo Walkthrough

> Created on `07/07/2025`
> by Sebastian Villa \<<s.villa@beckhoff.com>\>
> 
> This is a write up of what I did when I set up this project.

**Using the FC1121 or CX-B110 EtherCAT Slave Interface:**

1. **On the Controllers with the EtherCAT Slave Interface, Scan for or add the slave device**

![image](https://github.com/user-attachments/assets/9ae6397e-feb4-4d24-9b79-a8f879e2f9b6)![image](https://github.com/user-attachments/assets/6e2a0b05-2504-44d0-89ae-a270ac094260)



2. **You can optionally map Synchronization variables and Device Status:**
    1. This will include new variables in the Info Data, these variables need to be monitored to determine the synchronization status.

![image](https://github.com/user-attachments/assets/ff095070-ca14-4cef-aa33-2d5820beb783)


3. **Add in the appropriate data to receive from the EtherCAT master PC and any Status data that the slave should send back.**

![image](https://github.com/user-attachments/assets/00eec05f-5da7-4c9a-ac38-f76ce76ed176)![image](https://github.com/user-attachments/assets/06e6ef04-fe4c-4911-9195-3973ba41f973)



4. **Link the new variable on the Slave Device to any variables that will use them locally.**
    1. You will need to Build, Link PLC vars, and Activate Configuration on the PLC(s) with a Slave interface.
    2. For example a simple PLC program:
  
![image](https://github.com/user-attachments/assets/a766d764-0004-4b98-b230-0931c94a3522)


5. **To configure the master side the slave is very straight forward, scan the slave and this will bring in the values that are configured for data exchange.**
    1. Alternatively, you can remake the same variables/data struct on the Master side, the names can be renamed appropriately, what is important is the data sizes and offsets.
    2. Note that the Inputs and Outputs will be switched because of the flow of data.
    3. Again you’ll need to Build, Link PLC vars, and Activate Configuration on the PLC with an EtherCAT Master interface
  
![image](https://github.com/user-attachments/assets/6d2925c9-cc25-425c-bd45-6cccac585898)

