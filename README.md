# ACTIVE DIRECTORY-LAB
# Active Directory Corporate Simulation Using Oracle VirtualBox

![Screenshot (187)](https://github.com/babsthetechguy/ACTIVE-DIRECTORY---LAB/assets/150613649/2787b1fb-be9d-4177-bb45-0b7a4944b2b4)



## Introduction/Summary

In this project, I built an Active Directory home lab by deploying Oracle Virtualbox to emulate a corporate environment with 1,000 users. The Setup comprised a Windows Server 2019 VM serving as my ‘Domain Controller’, and a Windows 10 Pro VM designed as a ‘client’ machine. To make the environment similar to a corporate structure, I implemented a custom Powershell script was used to populate Active Directory with 1,000 users, each assigned a unique name (first name and last) along with a default password. The windows 10 Pro VM (our ‘client’ machine) was then configured and joined to the domain.

The following steps involved using Active Directory to create group policies, security groups & organization units. In conclusion, Active Directory was configured to operate as a centralized management system for computers, users accounts, etc. 


## Utilized Technologies and Components:

-	Windows Server 2019
-	Windows 10 Pro
-	Oracle VirtualBox
-	Active Directory
-	Active Directory Domain Service
-	Network Address Translation (NAT)
-	Domain Name Service (DNS)
-	Dynamic Host Configuration Protocol (DHCP)
-	File and Storage Services
-	Internet Information Services (IIS)
-	PowerShell

## VirtualBox Set-up

I used VirtualBox to create both the DC “Domain Controller” and ‘Client’ machines (client machine created after setting up the Domain Controller completely and creation of 1,000 users).

![Screenshot (188)](https://github.com/babsthetechguy/ACTIVE-DIRECTORY---LAB/assets/150613649/74439548-02f8-4f59-b44a-ef439efd9c08)

![Screenshot (190)](https://github.com/babsthetechguy/ACTIVE-DIRECTORY---LAB/assets/150613649/deb003ed-9341-4d3d-b754-9e6fb5eabb94)




## Windows Server 2019 and Active Directory Configuration

Two network adapters were used to separate internal and external traffic which were renamed to be easily identified with ‘_Internet_’ for external and ‘X_Internal_X’ for internal.

![Screenshot (19)](https://github.com/babsthetechguy/ACTIVE-DIRECTORY---LAB/assets/150613649/80235403-3173-4511-bf9e-f3ae85ad731a)

![Screenshot (18)](https://github.com/babsthetechguy/ACTIVE-DIRECTORY---LAB/assets/150613649/4311c448-cac8-4577-84ff-c268ad13ae40)

![Screenshot (17)](https://github.com/babsthetechguy/ACTIVE-DIRECTORY---LAB/assets/150613649/058d6d33-1d63-49fe-a0a0-9db98c7109b2)



In addition, these roles and services within Active Directory and the DC were configured

![Screenshot 2023-12-22 at 11 16 26 PM](https://github.com/EricMcclellan1/AD-Lab/assets/147299619/680e892c-bf21-4050-8f17-806c51ebd4cf)


A custom name list was used with 1,000 fake names saved to a text doc. and also my name at the top of the list to make it even more legit ;-)


![Screenshot (21)](https://github.com/babsthetechguy/ACTIVE-DIRECTORY---LAB/assets/150613649/0649baad-ccb4-404c-96da-f5082ca16a1f)



A custom Powershell script was then executed inconjunction with the above name list to populate Active Directory, with the script parsing the names list & creating users by the first letter of the first name and the last name.

![Screenshot (11)](https://github.com/babsthetechguy/ACTIVE-DIRECTORY---LAB/assets/150613649/84d97c25-442c-4b8b-9538-9ce53e2dbbf6)

![Screenshot (15)](https://github.com/babsthetechguy/ACTIVE-DIRECTORY---LAB/assets/150613649/3160a399-203a-4d1a-ab85-895d6f18381b)


![Screenshot (22) (1)](https://github.com/babsthetechguy/ACTIVE-DIRECTORY---LAB/assets/150613649/0eca5e8b-3da5-4a42-8279-2fd911ff2b37)

![Screenshot (23) (1)](https://github.com/babsthetechguy/ACTIVE-DIRECTORY---LAB/assets/150613649/3eac68c7-ab22-405e-ba7f-c4d8a2fe2111)


## Joining Windows 10 Pro To The Domain Controller

As mentioned earlier, I utilized VirtualBox to also create the Windows 10 Pro environment, serving as a proxy for an actual ‘client’ scenario. The network adapter was configured to operate within an “internal network” ensuring that traffic flowed only through the Domain Controller (DC). To validate connectivity, I pinged the previously created DC, “mydomiainbabs.com” and received a positive read-back.

After integrating this machine with the DC, I then tried accessing it using credentials from 10 users that I previously generated, Logging into the Windows 10 VM replicated the experience of a new client/user gaining access to the corporate network on their first day of work. Each one was able to login successfully.

![WhatsApp Image 2024-01-31 at 22 43 44_9559e598](https://github.com/babsthetechguy/ACTIVE-DIRECTORY---LAB/assets/150613649/985be49b-4630-4cb4-8987-d96d624e19b0)

![WhatsApp Image 2024-01-31 at 22 48 10_06c083b6](https://github.com/babsthetechguy/ACTIVE-DIRECTORY---LAB/assets/150613649/9e0f7edd-9bd4-4f40-a32e-809d0e6ffefb)

## Conclusion

In conclusion, this project allowed me to gain valuable knowledge in setting up proper configuration of Active Directory securely, providing hands-on experience in utilizing scripts and VirtualBox. Exploring the functionality of Active Directory deepened my knowledge of the tool, more of its ins and outs on a technical level and granting me a wider knowledge base of it in a more real world corporate environment. The practical engagement enhanced my understanding and familiarity with cyber security practices within the Active Directory Management.





