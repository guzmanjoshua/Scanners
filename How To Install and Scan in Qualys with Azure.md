# How To Install and Scan in Qualys with Azure

### **Introduction**

This article provides a guide on how to install and scan in Qualys with Azure. It covers the steps required to set up and connect the Qualys virtual scanner appliance in Azure, as well as perform scans using Qualys for vulnerability management. The article includes instructions, screenshots, and explanations to help users navigate through the process effectively.

### **About Qualys**

Qualys is a leading provider of cloud-based security and compliance solutions. It offers a wide range of products and services designed to help organizations identify and mitigate vulnerabilities in their IT infrastructure. Qualys provides comprehensive scanning capabilities, allowing users to assess the security posture of their systems, networks, web applications, and more. With its intuitive interface and powerful features, Qualys simplifies the vulnerability management process and helps organizations prioritize and address security risks effectively.

By leveraging Qualys in conjunction with Azure, organizations can enhance their security posture and gain valuable insights into potential vulnerabilities. The integration of Qualys with Azure allows users to leverage the scalability and flexibility of the cloud while benefiting from Qualys' robust scanning and reporting capabilities. With Qualys, organizations can proactively identify and remediate vulnerabilities, ensuring the protection of their critical assets and data.

Whether you are new to Qualys or looking to integrate it with Azure, this article will guide you through the process of installing and scanning in Qualys, empowering you to strengthen your security measures and protect your infrastructure.

# Section 1 - Getting Qualys Personalization Code

- Log into Qualys.
- When logged into Qualys, make sure you are in the Vulnerability Management dashboard, you can check in the top left of the screen.
- Click on the Scans tab.
- Click on the Appliances sub-tab.

<img src="Qualys Folder Pics/Q 1.png">

Qualys Code: **STEP 1**
</br>

- Click on the New button.
- Click on Scanner Appliance.

<img src="Qualys Folder Pics/Q 2.png">

Qualys Code: **STEP 2**

- When you reach this page with your Personalization Code, DO NOT close or go to the next page since you need this code.
- Open up Azure on a new tab.

![Q 11.png](How%20To%20Install%20and%20Scan%20in%20Qualys%20with%20Azure%209dbf9714de4b4a249419d3506cd96302/Q_11.png)

Qualys Code: **STEP 3**

# Section 2 - Creating and Connecting the Qualys VM in Azure to Qualys

- In Azure go to the Marketplace.
- In the Marketplace search bar type in ‘qualys virtual scanner appliance’.
- Once ‘Qualys Virtual Scanner Appliance’ appears press Create.
- When creating the VM you will see a text box named Perscode.
- Get the Personalization Code from Qualys and put it in the Azure Perscode text box and continue creating the VM.
- When finished, head back into Qualys.

![Q 9.png](How%20To%20Install%20and%20Scan%20in%20Qualys%20with%20Azure%209dbf9714de4b4a249419d3506cd96302/Q_9.png)

Qualys VM: **STEP 1**

- On the Personalization Code page, scroll down and press next until you have reached the same page you see above.
- Click on the Start Wizard button.

![Q 12.png](How%20To%20Install%20and%20Scan%20in%20Qualys%20with%20Azure%209dbf9714de4b4a249419d3506cd96302/Q_12.png)

Qualys VM: **STEP 2**

- Name the Virtual Scanner.
- For the Virtualization Platform, we want to choose Microsoft Azure which you can select with the dropdown arrow.
- When finish click next.

![Q 13.png](How%20To%20Install%20and%20Scan%20in%20Qualys%20with%20Azure%209dbf9714de4b4a249419d3506cd96302/Q_13.png)

Qualys VM: **STEP 3**

- When you reach this page you see above, double check that you finish creating the Qualys VM in Azure and the Perscode is inserted.
- This is the last chance to finish the VM.
- When finish scroll down and click next.

![Q 14.png](How%20To%20Install%20and%20Scan%20in%20Qualys%20with%20Azure%209dbf9714de4b4a249419d3506cd96302/Q_14.png)

Qualys VM: **STEP 4**

- When you reach this page you see above, you can safely click done even if it's not finish.
- You can check the status at the Appliances sub-tab.
- Once finish move on to the next step.

![Q 15.png](How%20To%20Install%20and%20Scan%20in%20Qualys%20with%20Azure%209dbf9714de4b4a249419d3506cd96302/Q_15.png)

Qualys VM: **STEP 5**

# Section 3 - Scanning in Qualys

- Click on the Scans sub-tab.
- Click on the New drop-down button.
- Click on the Scan button.

![Q 3.png](How%20To%20Install%20and%20Scan%20in%20Qualys%20with%20Azure%209dbf9714de4b4a249419d3506cd96302/Q_3.png)

Qualys Scan: **STEP 1**

- Name the Scan on the title text box.
- On Scanner Appliance select the Virtual Scanner you created and named in the previous steps.
- For the IPv4 Addresses, type the machine(s) private address you want to scan.
- BE AWARE, to have a successful scan make sure the machine is turned on.
- When finished click Launch.

![Q 4.png](How%20To%20Install%20and%20Scan%20in%20Qualys%20with%20Azure%209dbf9714de4b4a249419d3506cd96302/Q_4.png)

Qualys Scan: **STEP 2**

- If this is your first time adding the private IP address(es), this page you see above will pop up.
- Click on Add.

![Q 5.png](How%20To%20Install%20and%20Scan%20in%20Qualys%20with%20Azure%209dbf9714de4b4a249419d3506cd96302/Q_5.png)

Qualys Scan: **STEP 3**

- This page you see above will pop up.
- The Status shows the progress of the Scan.
- The three main statuses are Queue, Running, and Finish.
- You can safely close this page and head back to the Scans subpage.

![Q 6.png](How%20To%20Install%20and%20Scan%20in%20Qualys%20with%20Azure%209dbf9714de4b4a249419d3506cd96302/Q_6.png)

Qualys Scan: **STEP 4**

- In this page you can see the Status Icons on the left side.
- The Status of the scans is on the right side.
- On the bottom of the screen the View Summary will bring you back to the Scan Status page, which is the page we were before this.
- The View Results will appear when the Scan is finish.
- When the scan is finish, click on the machine scan and click on View Results.

![Q 7.1.png](How%20To%20Install%20and%20Scan%20in%20Qualys%20with%20Azure%209dbf9714de4b4a249419d3506cd96302/Q_7.1.png)

Qualys Scan: **STEP 5**

- In my scan of my Windows VM, I have a summary of 45 vulnerabilities with an average security risk of 3.0.
- I have 6 vulnerabilities that have a severity level of 2 and 6 other vulnerabilities that have a severity level of 3.
- The Windows OS was detected but with a vague version, with 5 services detected.
- The 12 vulnerabilities and the 33 other information gathered can be viewed in more detailed by pressing the drop-down buttons that is located in the Detailed Results section.
- While we got the scan to work this is an unauthenticated scan, so we are not grabbing the full picture of our machine.

![Q 8.png](How%20To%20Install%20and%20Scan%20in%20Qualys%20with%20Azure%209dbf9714de4b4a249419d3506cd96302/Q_8.png)

![Screenshot 2024-02-14 174310.png](How%20To%20Install%20and%20Scan%20in%20Qualys%20with%20Azure%209dbf9714de4b4a249419d3506cd96302/Screenshot_2024-02-14_174310.png)

Qualys Scan: **STEP 6**

# Section 4 - Authenticated Scans with Qualys

- Go to the Authentication sub-tab.
- Click on the new drop-down button.
- Click on the Operating System drop-down button.
- Click on the appropriate OS, for my case I am choosing the Windows OS.

![Q 16.1.png](How%20To%20Install%20and%20Scan%20in%20Qualys%20with%20Azure%209dbf9714de4b4a249419d3506cd96302/Q_16.1.png)

Qualys Authentication Scan: **STEP 1**

- The default title will be the OS you chose.
- In Login Credentials select Local for Windows Authentication.
- Select Basic authentication for Login and enter in the Username and Password from your Windows admin credentials.
- Select both NTLMv2 and NTLMv1.
- Select IPs from the left list when finish.

![Q 17.png](How%20To%20Install%20and%20Scan%20in%20Qualys%20with%20Azure%209dbf9714de4b4a249419d3506cd96302/Q_17.png)

Qualys Authentication Scan: **STEP 2**

- Type the private IPs from your VM that matches your OS.
- Select the Save button when finish.

![Screenshot 2024-02-14 172617.png](How%20To%20Install%20and%20Scan%20in%20Qualys%20with%20Azure%209dbf9714de4b4a249419d3506cd96302/Screenshot_2024-02-14_172617.png)

Qualys Authentication Scan: **STEP 3**

- Repeat the same scanning steps for the authenticated VM.
- The only difference is to name the title with “Authenticated” to distinguish from the unauthenticated scan.
- For example, I will name my scan to “Authenticated Azure WindowsVM”.
- When done press Launch.
- As the same as the previous steps, when the scan is done click on View Results.

![Q 3.png](How%20To%20Install%20and%20Scan%20in%20Qualys%20with%20Azure%209dbf9714de4b4a249419d3506cd96302/Q_3.png)

![Q 4.png](How%20To%20Install%20and%20Scan%20in%20Qualys%20with%20Azure%209dbf9714de4b4a249419d3506cd96302/Q_4.png)

Qualys Authentication Scan: **STEP 4**

- In my scan of my Authenticated Windows VM, I have a summary of 310 vulnerabilities with an average security risk of 5.0.
- I have 9 vulnerabilities that have a severity level of 2, 34 vulnerabilities that have a severity level of 3, 45 vulnerabilities that have a severity level of 4, and 13 vulnerabilities that have a severity level of 5.
- The Windows OS was detected with the specific version, with 15 services detected.
- The scan detected 101 vulnerabilities, 4 potential vulnerabilities, and 205 information gathered.

![Screenshot 2024-02-14 174411.png](How%20To%20Install%20and%20Scan%20in%20Qualys%20with%20Azure%209dbf9714de4b4a249419d3506cd96302/Screenshot_2024-02-14_174411.png)

![Screenshot 2024-02-14 174442.png](How%20To%20Install%20and%20Scan%20in%20Qualys%20with%20Azure%209dbf9714de4b4a249419d3506cd96302/Screenshot_2024-02-14_174442.png)

Qualys Authentication Scan: **STEP 5**

### **Conclusion: Authenticated vs. Unauthenticated Scans**

Authenticated and unauthenticated scans serve different purposes in vulnerability management. Unauthenticated scans provide a high-level overview of remotely exploitable vulnerabilities, while authenticated scans offer deeper insights by accessing the internal system configuration with specific user credentials. Both types of scans are valuable and should be conducted to gain a comprehensive understanding of security risks. By combining the results, vulnerabilities can be prioritized and addressed more effectively, improving overall security.

In conclusion, this article provides a comprehensive guide on installing and scanning with Qualys in Azure. It covers the steps to set up the Qualys virtual scanner appliance, perform scans, and highlights the importance of authenticated and unauthenticated scans in vulnerability management.
