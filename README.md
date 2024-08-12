# Nessus Vulnerability Scanning and Remediation Lab

## Objective

The objective of this project is to successfully configure and scan for vulnerabilities as well as remediate them via Nessus in home lab environment.

### Skills Learned


- Configured and conducted vulnerability scans utilizing Nessus to identify and assess security weaknesses in a virtual environment.
- Disabled the firewall to intentionally expose the VM, demonstrating its visibility and risk factors during a vulnerability scan.
- Performing routine scans can elimanate a large amount of risk.
- Enhanced knowledge of security vulnerabilities and successfully remediating them.
- proficiency in using Nessus to scan for vulnerabilities.

### Tools Used


- Nessus
- VMware 
- Windows 10

## Steps
1. Downloaded VMware workstation pro.

   <img width="367" alt="image" src="https://github.com/user-attachments/assets/efb1f332-f96e-4b9f-a1bf-82fb805fa3a5">

2. Then I downloaded the Windows 10 ISO file.

3. Next I installed Nessus.

4. While waiting for Nessus to install, I navigated to the Windows VM workstation 17 player and configured and installed the Windows virtual machine.

   <img width="541" alt="image" src="https://github.com/user-attachments/assets/fd5dd287-4e84-4e33-a4d9-3296df54f214">

   <img width="511" alt="image" src="https://github.com/user-attachments/assets/13466cbd-ccc9-4d30-b1aa-e471968a2f1e">


5. Once the VM was booted up I ran the ipconfig command to find the IP address. I tried to ping it from my local machine and it was unreachable.

6. Next I disabled the firewall on the VM.

   <img width="508" alt="image" src="https://github.com/user-attachments/assets/aabca124-6669-4aef-97c4-b755a8405cb5">

7. Ran the ping command again and was successfully able to ping the VM.

8. Navigated to Nessus and created a new scan.

   <img width="1619" alt="image" src="https://github.com/user-attachments/assets/5fbb0ff8-4b93-4d02-9043-c169e23f7057">

9. Selected Basic Network Scan

    <img width="1076" alt="image" src="https://github.com/user-attachments/assets/674dfac9-4296-4fdb-917e-e0a77726c118">

10. Configured a scan of the VM.

    <img width="1495" alt="image" src="https://github.com/user-attachments/assets/3ca2666d-11ae-4d17-9f2a-d26621b19828">

11. Once the configuration was complete I launched the scan.

    <img width="1580" alt="image" src="https://github.com/user-attachments/assets/c1e9e1ca-75ce-46b1-a2da-bc8345cd5088">

12. The findings for the scan is in the screenshots below.

    <img width="1550" alt="image" src="https://github.com/user-attachments/assets/6d6fe8f2-4f1c-47ef-9667-bb68bc73b59e">

    <img width="1544" alt="image" src="https://github.com/user-attachments/assets/281f2b85-e3a8-4985-9df1-9ac34acaad8d">

    <img width="1565" alt="image" src="https://github.com/user-attachments/assets/06b45180-7017-45b1-8252-8a5771b71d34">

13. As an example, this log generated because Nessus was not able to authenticate to the VM as there were no credentials used.

    <img width="1565" alt="image" src="https://github.com/user-attachments/assets/e5c18fd5-855c-412e-a920-53bfe5074d2b">

14. Next I set up the virtual machine to accept authenticated scans as well as provide login credentials to Nessus and compare the results of the first scan after the adjustments.

15. I enabled remote registry.

    <img width="510" alt="image" src="https://github.com/user-attachments/assets/a5f52161-0d64-46bd-9fba-b38e18a1470e">

16. Navigated to User Account control settings and changed it to never notify.

    <img width="510" alt="image" src="https://github.com/user-attachments/assets/eb347ae6-8ae6-4760-b3b4-8b91a2dc8f22">

17. Navigated to Registry Editor to add a key to allow the remote account to connect in to and add a key to further disable user account control for the remote account. *This was based off of guidance from Nessus.

    <img width="510" alt="image" src="https://github.com/user-attachments/assets/63f1d8f0-5a6c-4042-805d-5d0b51e774bd">

18. Next I restarted the VM.

19. I navigated back to Nessus and went back into the previous scan and configured it further by adding the Windows VM login credentials.

    <img width="1451" alt="image" src="https://github.com/user-attachments/assets/87245dac-98f4-4d81-9f84-69cb2a3daef6">

20. Ran the scan and the screenshot below shows the results.

    <img width="1527" alt="image" src="https://github.com/user-attachments/assets/c823d88f-ead3-41cb-b648-3bb4f2f638d3">

21. As seen in the screenshot a credentialed scan revealed that there were several critical vulnerabilities.

22. As an example, I noticed that there were several critical vulnerabilities. More than likely after updating Windows or Edge this would be remediated.

    
<img width="1631" alt="image" src="https://github.com/user-attachments/assets/2b4c93b5-0175-4088-a831-f91f64df8cb6">

23. Below in the screenshot is a breakdown on one of the critical vulnerabilities, which states that Edge needs to be updated.

    <img width="1157" alt="image" src="https://github.com/user-attachments/assets/a8050afb-dd87-47e5-a0f6-0a2b3b627d7f">

24. Within the remediations tab it gives a high level overview on how to remediate the vulnerabilities.

    <img width="1738" alt="image" src="https://github.com/user-attachments/assets/104ee96c-c837-4f8a-a8d8-1de8023b0959">

25. A fix for most of these vulnerabilities would be having routine windows automated patching within the organization to avoid having these vulnerabilities occur.

26. Next I am going to install a depricated version of Firefox and run another scan to see the results.

<img width="462" alt="image" src="https://github.com/user-attachments/assets/4b497366-8698-477c-b9c8-afadd20d3d4d">

27. I Performed another scan after the depricated Firefox download, below are the results of the next scan.

    <img width="1760" alt="image" src="https://github.com/user-attachments/assets/d219af4e-da48-467c-8b4f-c7d051cee39e">

    <img width="1690" alt="image" src="https://github.com/user-attachments/assets/8d31556e-8c46-43f4-8193-ce78f4e6234c">

28. Next my goal is to remediate as many vulnerabilities as possible. To start with I will uninstall Firefox completely and run windows updates. Normally in an enterprise setting updating the application would be the solution.

    <img width="508" alt="image" src="https://github.com/user-attachments/assets/3384051e-98f5-4901-ac46-cc3c391c4a42">

    <img width="509" alt="image" src="https://github.com/user-attachments/assets/b4efec65-df72-4413-8fe8-168d8e76e329">



   Reflecting on the previous scans:

Scan 1: A non-credentialed scan revealed zero critical vulnerabilities.


<img width="709" alt="image" src="https://github.com/user-attachments/assets/e28946a9-3316-4a4d-a3f7-b657ba78b286">


Scan 2: A credentialed scan resulted in a significant increase in critical vulnerabilities detected.


<img width="706" alt="image" src="https://github.com/user-attachments/assets/1ff234dd-1da0-4a82-9c66-89f080207ec3">


Scan 3: After installing a deprecated version of Firefox, the number of critical vulnerabilities surged dramatically.


<img width="707" alt="image" src="https://github.com/user-attachments/assets/9c1b089f-5e6f-4043-b1e0-e51dd6c849d6">


Scan 4: After uninstalling Firefox, running Windows updates, and updating applications in the Microsoft Store. I was able to remediate a large amount of the vulnerabilities, this is the final credentialed scan.









## Lessons Learned

- There's a large difference between doing a credentialed scan and a non credentialed scan. More risks are exposed with credentialed scans.
- Regularly updating applications and Windows significantly reduces the number of vulnerabilities detected during scans.



    


    

    



    






   










