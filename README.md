# Vulnerability Scanning and Remediation with Nessus

## Objective

(THIS LAB IS IN PROGRESS) The objective of this project is to successfully configure and scan for vulnerabilities as well as remediate them via Nessus in home lab environment.

### Skills Learned
[Bullet Points - Remove this afterwards]

- Configured and conducted vulnerability scans using Nessus to identify and assess security weaknesses in a virtual environment.
- Proficiency in analyzing and interpreting network logs.
- Ability to generate and recognize attack signatures and patterns.
- Enhanced knowledge of network protocols and security vulnerabilities.
- Development of critical thinking and problem-solving skills in cybersecurity.

### Tools Used
[Bullet Points - Remove this afterwards]

- Nessus
- VMware 
- Telemetry generation tools to create realistic network traffic and attack scenarios.

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







    


    

    



    






   









*Ref 1: Network Diagram*
