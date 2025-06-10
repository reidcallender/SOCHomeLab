<h1>SOC Home Lab</h1>



<h2>Description</h2>
The purpose of this lab was to create a basic home SOC in the cloud using azure. I created a virtual machine and opened it to the internet to entice attackers. I forwarded the logs from the VM to a central repository and integrated microsoft sentinel to analyze and map the attack data.
<br />


<h2>Languages and Utilities Used</h2>

- KQL 
- Azure Sentinel
- Log analytics workspace
- Azure VM
- Json
  

<h2>Environments Used </h2>

- <b>Windows 11 Pro (VM)</b> 

<h2>Lab Walk-through:</h2>


Created a resource group and added a virtual network. <br/>

![Image](https://github.com/user-attachments/assets/98ded820-1d44-47de-8674-4a217b861e20)
<br />
<br />
Created a virtual machine. <br />
<br />
![Image](https://github.com/user-attachments/assets/08c4ee2c-7f86-43bb-8719-f1b87f8839a2)
<br />
<br />
Created a new inbound rule in the network security group which allows any inbound traffic. <br />
<br />
![Image](https://github.com/user-attachments/assets/bc752db1-3de5-482a-96f0-427258c9bb4a)
<br />
<br />
Connected to the VM using RDP to turn off Windows firewall. <br />
<br />
![Image](https://github.com/user-attachments/assets/6a370436-8af2-41bc-a38a-636ec4acb7f3)
<br />
<br />
Created a log analytics workspace to forward logs from the VM. <br />
<br />
![Image](https://github.com/user-attachments/assets/46886adf-bd2c-4fbf-a6c7-9ca9e08d4dd7)
<br />
<br />
Created a Sentinel instance and linked it with log analytic workspace. <br />
<br />
![Image](https://github.com/user-attachments/assets/98526ea1-c775-4ca0-8f1a-3d6fc024ca5b)
<br />  
<br />
Connected the log repository with the VM and created a data collection rule. <br />
<br />
![Image](https://github.com/user-attachments/assets/d68b270c-68be-42a5-afa6-9fd7853d09aa)
<br />  
<br />
Viewed the event logs in log analytics workspace and filtered them using KQL to to show events with failed login attempts. <br />
<br />
![Image](https://github.com/user-attachments/assets/28b16642-8a9a-45e6-bd48-8ccf1935de48)
<br />  
<br />
Imported a spreadsheet into watchlist which will resolve IP addresses to phyical locations which will be used on the map. <br />
<br />
![Image](https://github.com/user-attachments/assets/860c9f1d-faff-46c4-b75f-d7f7f2348c60)
<br />  
<br />
Created a workbook in sentinel and added a json file obtained from Josh Madakor which will generate the attack map. https://drive.google.com/file/d/1ErlVEK5cQjpGyOcu4T02xYy7F31dWuir/view?pli=1 <br />
<br />
![Image](https://github.com/user-attachments/assets/77f5197a-bee2-4982-9073-abf3987b49f7)
<br />  
<br />
The final results of the lab! We can see three different brute force attacks which ocntinued up until I deleted the VM. <br />
<br />
![Image](https://github.com/user-attachments/assets/9193058f-47be-4a45-b7fa-de1b2da60b52)
<br />  
<br />
A separate implementation that I did of this lab. This time I recorded one brute force attack and a few single login attempts. <br />
<br />
![Image](https://github.com/user-attachments/assets/ffc3ffc2-0110-4d7f-97c8-4080888f49cf)
