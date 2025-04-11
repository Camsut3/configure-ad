
<p align="center">
<img src="https://i.imgur.com/Bp7tRX1.png" height="40%" width="60%" alt="Microsoft Azure Logo"/>
</p>
<h1>Creating a Virtual Machine (VM) in Microsoft Azure</h1>
Join me on this project as I set up a virtual machine in Azure and view the network topology using Network Watcher.<br />


<h2>Requirements</h2>

- Computer with internet connection
- Microsoft Azure account
  - Credit card (required for free Azure credits)

<h2>High-Level Steps</h2>

- Select “Virtual machines” and select to Create an “Azure virtual machine”
- Fill in the required fields on the “Basics” page
- Click “Review + create”
- Click “Create” if the VM has passed validation
- View newly created VM in Network Watcher
- Delete Resource Groups to minimize charges to free Azure credits

<h2>Synopsis</h2>

<p>
<img src="https://i.imgur.com/zkr3A9P.png" height="70%" width="70%"/>
</p>
<p>
To initiate the creation of the virtual machine, I searched for “virtual machine” in the Azure homepage search bar and selected “Virtual machines.” I then clicked “Create” in the top left corner (the blue “Create” button in the center also works) and chose “Azure virtual machine.”
</p>
<br />

<p>
<img src="https://i.imgur.com/bwTogp0.png" height="50%" width="50%"/>
</p>
<p>
<img src="https://i.imgur.com/3h91vqh.png" height="50%" width="50%"/>
</p>
<p>
The first page you encounter is the "Basics" page, where I filled in all the required fields. For the Resource group, I created a new one by selecting "Create new" and chose a region appropriate for my location. The region you select can influence the available options for the "Size" field, so you might need to adjust this a bit. Don’t forget to check the box under Licensing! Once I completed this page, I clicked "Review + create."
</p>
<br />

<p>
<img src="https://i.imgur.com/ksIytig.png" height="50%" width="50%"/>
</p>
<p>
Before the VM could be created, it needed to pass validation. Once the confirmation message at the top indicated that everything was correctly set up, I clicked "Create."
</p>
<br />

<p>
<img src="https://i.imgur.com/3iB9u1P.png" height="70%" width="70%"/>
</p>
<p>
Setting up the VM in Azure took some time, but once it was complete, I reviewed the configuration. I noted the locations of the public and private IP addresses, knowing this information would be essential for future labs.
</p>
<br />

<p>
<img src="https://i.imgur.com/J9BB8fA.png" height="70%" width="70%"/>
</p>
<p>
I used Network Watcher in Azure to explore the different components of my new VM. When you create a VM, it involves more than just the virtual machine itself. Azure also sets up a virtual network (VM-Lab-vnet), a subnet (default), a virtual NIC (vm-1960), a Network Security Group (VM-1-nsg), and a public IP address (VM-1-ip).
</p>
<br />

<p>
💡 That's how I set up a virtual machine in Azure! If you follow these steps, remember to delete any Resource Groups created to minimize charges to your free Azure credits. 💡
</p>
<br />
