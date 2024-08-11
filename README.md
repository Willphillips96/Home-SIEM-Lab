# Home-SIEM-Lab

## Objective

(THIS LAB IS IN PROGRESS) The objective of this project is to successfully set up and configure the Elastic Stack SIEM in a home lab environment. This involves configuring Elastic Agents for log collection and forwarding data to the SIEM, ensuring effective security event monitoring and analysis.

### Skills Learned
[Bullet Points - Remove this afterwards]

- Advanced understanding of SIEM concepts and practical application.
- Proficiency in analyzing and interpreting network logs.
- Ability to generate and recognize attack signatures and patterns.
- Enhanced knowledge of network protocols and security vulnerabilities.
- Development of critical thinking and problem-solving skills in cybersecurity.

### Tools Used
[Bullet Points - Remove this afterwards]

- Security Information and Event Management (SIEM) system for log ingestion and analysis.
- Network analysis tools (such as Wireshark) for capturing and examining network traffic.
- Telemetry generation tools to create realistic network traffic and attack scenarios.

## Steps
1. Created an Elastic account.

2. Downloaded the Kali Linux Image and successfully logged in. I am utilizing virtual box.

3.Set up an agent by going to Add integrations

<img width="546" alt="image" src="https://github.com/user-attachments/assets/df61cd5b-06c1-48d7-8391-19123f3a466e">

4. Added Elastic Defend.

   <img width="913" alt="image" src="https://github.com/user-attachments/assets/93d5972f-a838-45b9-8392-6c97cdfa1fea">

5. Utilized the command below to download the Elastic Defende agent onto the Kali Linux VM.

   <img width="530" alt="image" src="https://github.com/user-attachments/assets/f45786a8-dafe-428a-b048-49caa47a89f5">

6. Ran nmap on the local host. This can ultimately can detect open ports and creates several security events.

<img width="530" alt="image" src="https://github.com/user-attachments/assets/11d5cf70-d276-42a0-bae4-162e0c72360c">

7. Withthin Elastic I navigated to the logs.









*Ref 1: Network Diagram*
