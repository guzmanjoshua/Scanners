# How To Install and Scan in Greenbone Security Assistant with Azure

### Introduction

This Greenbone lab is a comprehensive guide on how to set up and utilize the Greenbone Security Assistant (GSA) for vulnerability scanning. The guide covers various steps, including creating and configuring an OpenVAS VM, accessing the VM through Windows PowerShell, performing the installation, logging into the GSA dashboard, creating assets and targets, and initiating scan tasks. Each step is accompanied by relevant screenshots and instructions to ensure a smooth scanning process. It is important to note that scanning from the public internet is considered malicious and should be avoided.

## Section 1: Creating the OpenVAS VM

OpenVAS VM: **STEP 1**

- Go to Marketplace.
- In the search bar in Marketplace, type ‘OpenVas’.
- Once ‘OpenVas secured and supported by HOSSTED’ pops up, click on create.

<img src="Greenbone Folder Pics/OV 1.png">

OpenVAS VM: **STEP 2**

- Once the OpenVas VM is created, open it up.
- Make sure the VM is running.
- You want to locate the public IP address and copy it.

![a OV 2.1.png](How%20To%20Install%20and%20Scan%20in%20Greenbone%20Security%20Assi%205a55124c91eb456a89e92c5c4b4a5330/a_OV_2.1.png)

## Section 2: Installation and Open

Install OpenVAS: **STEP 1**

- Open up Windows Powershell.
- Enter ‘ssh analyst@your_OpenVasVM_PublicIP’ and press enter.
- If done correctly you will be prompted to enter the same password you created when creating the OpenVasVM.

![a OV 3.png](How%20To%20Install%20and%20Scan%20in%20Greenbone%20Security%20Assi%205a55124c91eb456a89e92c5c4b4a5330/a_OV_3.png)

Install OpenVAS: **STEP 2**

- If done corrected, you should get an output similar to the picture above.
- Do not do anything yet since it is running an installation, this might take some time.

![OV 1.png](How%20To%20Install%20and%20Scan%20in%20Greenbone%20Security%20Assi%205a55124c91eb456a89e92c5c4b4a5330/OV_1.png)

Install OpenVAS: **STEP 3**

- Once the installation is finish, you should get an output similar to the picture above.
- Open any web browser and copy the blue link and paste it in the web browser URL.

![a OV 4.png](How%20To%20Install%20and%20Scan%20in%20Greenbone%20Security%20Assi%205a55124c91eb456a89e92c5c4b4a5330/a_OV_4.png)

Install OpenVAS: **STEP 4**

- Once you reached this page, copy and paste the Username and Password from Windows PowerShell into the Greenbone sign in page.

![a OV 5 light.png](How%20To%20Install%20and%20Scan%20in%20Greenbone%20Security%20Assi%205a55124c91eb456a89e92c5c4b4a5330/a_OV_5_light.png)

## Section 3: Creating Host

GSA Host: **STEP 1**

- Once logged in you will see the dashboard.
- Once here click on Assets.

![a OV 6.1.png](How%20To%20Install%20and%20Scan%20in%20Greenbone%20Security%20Assi%205a55124c91eb456a89e92c5c4b4a5330/a_OV_6.1.png)

GSA Host: **STEP 2**

- In Assets, click on the page with the star under the Dashboards button to create a New Host.

![a OV 7.png](How%20To%20Install%20and%20Scan%20in%20Greenbone%20Security%20Assi%205a55124c91eb456a89e92c5c4b4a5330/a_OV_7.png)

GSA Host: **STEP 3**

- For the IP Address, enter the private IP address of your desire VM.
- For the Comment, enter the name of your VM.
- When finish press Save.

![a OV 8.png](How%20To%20Install%20and%20Scan%20in%20Greenbone%20Security%20Assi%205a55124c91eb456a89e92c5c4b4a5330/a_OV_8.png)

## Section 4: Creating Target

GSA Target: **STEP 1**

- Press the same page with the star under actions of the Hosts you created to create a new target.

![a OV 9.png](How%20To%20Install%20and%20Scan%20in%20Greenbone%20Security%20Assi%205a55124c91eb456a89e92c5c4b4a5330/a_OV_9.png)

GSA Target: **STEP 2**

- Name the target and save.

![a OV 10.png](How%20To%20Install%20and%20Scan%20in%20Greenbone%20Security%20Assi%205a55124c91eb456a89e92c5c4b4a5330/a_OV_10.png)

## Section 5: Creating Task

GSA Task: **STEP 1**

- Click on Scans.
- Click on the page with the star.
- Click on New Task.

![a OV 11.png](How%20To%20Install%20and%20Scan%20in%20Greenbone%20Security%20Assi%205a55124c91eb456a89e92c5c4b4a5330/a_OV_11.png)

GSA Task: **STEP 2**

- Name the new scan task.
- For Scan Targets select the target you made for the dedicated VM.
- When finish press Save.

![a OV 12.png](How%20To%20Install%20and%20Scan%20in%20Greenbone%20Security%20Assi%205a55124c91eb456a89e92c5c4b4a5330/a_OV_12.png)

## Section 6: Run Scan and View Results

GSA Scan: **STEP 1**

- Click on the start button to start the scan. (I already started the scan, so it is greyed out for me)
- BE AWARE, to have a successful scan make sure the machine is turned on.
- Wait until the scan is completed to look at the report.

![a OV 13.png](How%20To%20Install%20and%20Scan%20in%20Greenbone%20Security%20Assi%205a55124c91eb456a89e92c5c4b4a5330/a_OV_13.png)

GSA Scan: **STEP 2**

- To check the report, click on either the Status button or the Reports button.

![a OV 14.1.png](How%20To%20Install%20and%20Scan%20in%20Greenbone%20Security%20Assi%205a55124c91eb456a89e92c5c4b4a5330/a_OV_14.1.png)

GSA Scan: **STEP 3**

- The report shows various of information about the machine however, this is an unauthenticated scan. So, we are not getting the full picture of our machines.

![a OV 15.png](How%20To%20Install%20and%20Scan%20in%20Greenbone%20Security%20Assi%205a55124c91eb456a89e92c5c4b4a5330/a_OV_15.png)

## Section 7: Authenticated Scan

GSA Authenticated Scan: **STEP 1**

- Click on Configuration.
- Click on Credentials.

![a OV 17.1.png](How%20To%20Install%20and%20Scan%20in%20Greenbone%20Security%20Assi%205a55124c91eb456a89e92c5c4b4a5330/a_OV_17.1.png)

GSA Authenticated Scan: **STEP 2**

- Click the page with the star.

![a OV 16.png](How%20To%20Install%20and%20Scan%20in%20Greenbone%20Security%20Assi%205a55124c91eb456a89e92c5c4b4a5330/a_OV_16.png)

GSA Authenticated Scan: **STEP 3**

- Add ‘Credential’ for name so we understand what it is.
- Have the type set to Username + Password.
- Have the Username and Password the same as your admin credentials.
- Click on save when finish.
- Repeat the steps 4 - 6 to create a new scan.

![a OV 18.png](How%20To%20Install%20and%20Scan%20in%20Greenbone%20Security%20Assi%205a55124c91eb456a89e92c5c4b4a5330/a_OV_18.png)

Unfortunately, I had trouble scanning my VMs during this time potentially due to interference from the February 13, 2024, Windows patches: [Microsoft February 2024 Patch Tuesday fixes 2 zero-days, 73 flaws (bleepingcomputer.com)](https://www.bleepingcomputer.com/news/microsoft/microsoft-february-2024-patch-tuesday-fixes-2-zero-days-73-flaws/)

### Conclusion

In conclusion, this comprehensive guide provides an in-depth overview of how to set up and utilize the Greenbone Security Assistant (GSA) for vulnerability scanning. It walks through various steps, from creating and configuring an OpenVAS VM to initiating scan tasks. However, it should be noted that due to potential system updates and patches, as experienced during the writing of this guide, there may be instances where scanning may not go as smoothly as expected. Overall, this guide provides a solid foundation for anyone looking to delve into vulnerability scanning using GSA.
