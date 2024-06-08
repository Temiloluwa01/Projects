# Created an externally accessible static website using Azure Virtual Machine via ARM template 

This project involved creating an externally accessible virtual machine on Azure. The virtual machine was accessible via its public IP, placed in a subnet in a virtual network, and had a network security group attached that allows HTTP access. It also had an Apache web server installed that served the static html file. 

If you'd like to do it below is a step-by-step guide on how to accomplish this:

## Demo

Sign in to the Azure Portal: Go to portal.azure.com and log in with your Azure account, after signing in create a template. 

## **Step 1: Create an Azure Template**

- Navigate to **"Template"** and click **"Create"**. 
- Provide a **"Template name"**, and add a description for the template if you want to add one.
  
![annotely_image (18)](https://github.com/Temiloluwa01/Projects/assets/116880220/aacd2023-e261-4313-a390-b8211645b040)

- After creating the template click on it, then click on **Deploy**

![annotely_image (19)](https://github.com/Temiloluwa01/Projects/assets/116880220/8af547e8-a2ff-475a-bd7c-5ec9f799fecc)

- When you click on deploy, you will be redirected to a custom deployment page. On this page, you will see that there are a bunch of ways to automate the deployment of a virtual machine. You can choose from the options dispalyed the one that best suits you.7
  
- If you have a custom template ready like me you can choose the **Build your own template in the editor option**

![annotely_image (20)](https://github.com/Temiloluwa01/Projects/assets/116880220/5e39870f-81bc-462f-b1f4-40d38dba1a40)

- Click on **load file** to upload your custom template then click **Save**.

![annotely_image (21)](https://github.com/Temiloluwa01/Projects/assets/116880220/8c2dc598-393a-47fe-859d-894c578f4056)

- After you click on **Save** you will be redirected to another tab where you will complete the automation by inputtig the required information.
  After inputting the information required click on **purchase** to purchase the service. 

![annotely_image (22)](https://github.com/Temiloluwa01/Projects/assets/116880220/4701bbe1-3252-43c7-9917-9ed421a943f1)


## Note: The credentials asked for depends on the paramters used in the template. 




