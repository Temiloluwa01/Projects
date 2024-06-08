# Created an externally accessible static website using Azure Virtual Machine via Azure portal

This project involved creating an externally accessible virtual machine on Azure. The virtual machine was accessible via its public IP, placed in a subnet in a virtual network, and had a network security group attached that allows HTTP access. It also had an Apache web server installed that served the static html file. 

If you'd like to do it below is a step-by-step guide on how to accomplish this:

## Demo

Sign in to the Azure Portal: Go to portal.azure.com and log in with your Azure account, after signing in create a virtual machine. 

## **Step 1: Create an Azure Virtual Machine (VM)**

- Navigate to **"Virtual Machines"** and click **"Create"**.
- Select a **"Resource Group"** or create a new one. In my case i already had a resource group. 
- Provide a **"VM Name"**, select the **region**, and choose an appropriate image (e.g., Ubuntu, Windows Server).
- Choose a size for the **VM**.
- Configure the Administrator account (username, password, or SSH key). I used choose a username and password for my admin credentials.

 ![annotely_image (13)](https://github.com/Temiloluwa01/Projects/assets/116880220/15eefbc7-aa2c-46c1-ab76-8560cda2f549)

- Configure **inbound ports** to be able to access your VM. Since i creating a linux machine I choose port 22 to br able to connect to my machine.
![annotely_image (14)](https://github.com/Temiloluwa01/Projects/assets/116880220/fb4576b6-72e5-41ad-a871-40967ee1834d)

- In the **"Networking" tab**, ensure that the VM has a public IP address.
![annotely_image (15)](https://github.com/Temiloluwa01/Projects/assets/116880220/166b7a20-326a-4042-80e8-9fa1d24323e2)

- Complete the creation process by reviewing and creating the VM.



## **Step 2: connect to the VM and install a Web Server**

- Connect to the VM by using SSH. 
````
SSH VMname@vmipaddress
````
- Update the VM dependencies and Install an Apache Web Server
````
Sudo apt update -y
sudo apt upgrade -y
sudo apt install apache2 -y
`````
- Open a browser and navigate to the public IP of your VM to ensure the web server is running. You will notice that the web server isnt runnnig, now thats because of the web server cannot connect to the internet. 
![Screenshot 2024-06-08 041141](https://github.com/Temiloluwa01/Projects/assets/116880220/dda4d7ac-3a74-47cc-abc8-1b2e5446ab3a)

To rectify that, 


## **Step 3: Create a Network Security Group(NSG)**
- Navigate to nsg on the Azure portal. You will see an NSG that was created alongsides the VM, click into it and create an inbound rule that allows web traffic.
  
![annotely_image (16)](https://github.com/Temiloluwa01/Projects/assets/116880220/c2e31459-b142-4f4c-b317-d77b84783f86)

- Create an inbound security rule thats allows HTTP traffic to the VM so that the web server can be accessible on the internet.
  
![annotely_image (17)](https://github.com/Temiloluwa01/Projects/assets/116880220/cf19ce5a-2250-4823-8d33-da4283165cd6)

- Now verify the Web Server again. Open a browser and navigate to the public IP of your VM to ensure the web server is running. You will see that the the web server is now working.

![Screenshot 2024-06-05 021824](https://github.com/Temiloluwa01/Projects/assets/116880220/6afd7053-7c73-48b2-a08a-7231c7a52a63)








