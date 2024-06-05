# Active Directory Project
The goal of this project was to set up an environment using Oracle VM VirtualBox with the utilization of Active Directory and other tools to configure a domain controller and clients to sucessfully communicate through the network.

Identification of external internet NIC and internal NIC, manual configuration of internal NIC IP address for the internal network. (The internal NIC was easily identified as it was initially ssigned an APIPA address) 
![image](https://github.com/kimSim/AD/assets/10665087/7068d945-4f68-41fd-9672-4f3e104c9215)


Utilizing Server Manager, installed Active Directory, created a domain and a dedicated domain adminstrative account. Through "Active Directory Users and Conmputers" this account was added to an organization unit categorized as Admins, then given privelages as a domain adminstrator to allow it to make elevated changes and configurations.
![image](https://github.com/kimSim/AD/assets/10665087/a83b1e08-3f7c-4367-a231-8167633f85ab)


Installation and configuration of RAS and NAT to allow future Windows 10 client to still be able to access the internet through the domain controller even though it is in a private virtual network environment. Configured the NAT connection to the external internet connection.
![image](https://github.com/kimSim/AD/assets/10665087/2e33caa5-35b0-421d-ab2d-ef792aef027e)


Installed and configured DHCP to allow clients to sucessfully connect to the external network via assigned IP address. Set up IP scope range between 172.16.0.100-200 and verified lease duration. In this case the domain controller was used as the DNS server due to the environment given. 

![image](https://github.com/kimSim/AD/assets/10665087/ab8aec21-bfe1-4428-9a62-ee668f1fbe56)


Utilized PowerShell to get data from predetermined names via txt file in order to create 1,000 users and configure them with names, usernames, passwords, etc. Verified all users have been successfuly created in the domain users directory. 
![image](https://github.com/kimSim/AD/assets/10665087/af5b18cb-9b1c-403d-b792-25bc2e981d8b)


Using VirtualBox, created a new Windows 10 client that is connected to the domain. Configured the virtual client with neccessary CPU core and RAM usage. Verified client is sucessfully connected to the domain controller which then is able to sucessfully communicate to the external network. Verification was done by the ping and ipconfig commands in cmd.  
![image](https://github.com/kimSim/AD/assets/10665087/d8854481-b099-4ea9-8015-313b53745cc3)

