# Mimikatz Rule Detection Project

<div style="text-align: center;">
  <img src="https://github.com/user-attachments/assets/c7b40fae-567f-43b1-8706-1e0031590b5a" alt="SIEM Project Overview" style="border: 2px solid #000; border-radius: 5px;">
</div>



## Objective

The Mimikatz Rule Detection Project was designed to simulate a real-world cyber attack scenario, focusing on detecting and responding to the use of the Mimikatz tool on a Windows machine. The primary goal was to establish a robust detection mechanism using LimaCharlie EDR and automate incident response actions with Tines. This project provided hands-on experience in detecting sophisticated attacks and automating responses in a controlled environment.

### Skills Learned

- Advanced understanding of Endpoint Detection and Response (EDR) systems.
- Proficiency in detecting and analyzing hacker tools like Mimikatz.
- Automation of incident response actions using playbooks.
- Integration of SIEM, Slack, and email notifications for streamlined communication.
- Development of decision-making processes for isolating compromised machines.

### Tools Used

- **LimaCharlie EDR**: For real-time detection and monitoring of the Mimikatz tool.
- **Tines**: To automate the incident response process, including notifications and machine isolation.
- **Slack**: For immediate alerting and communication with the security team.
- **Email**: To send detailed reports on the detected incidents.
- **APIs**: To facilitate integration between LimaCharlie, Tines, Slack, and the email system.

## Steps

1. **EDR Installation**
   - A Windows machine was set up with LimaCharlie EDR installed to monitor and detect suspicious activities, focusing on detecting the execution of the Mimikatz tool.
  
2. **Detection Rule Creation**
   - A custom detection rule was created in LimaCharlie to identify the execution of Mimikatz. This rule was designed to capture and log the tool's activity for further analysis.
  
3. **Alert Generation and Playbook Execution**
   - Upon detecting Mimikatz, Tines was triggered to execute a predefined playbook, which performed the following actions:
     - Sent an alert to Slack with the machine and detection details.
     - Dispatched an email containing the detection report.
     - Prompted the security analyst to decide whether to isolate the compromised machine.

## Screenshots



### 4. Analyst Decision: Isolation Process

*Ref 4: Isolation Prompt*  
The security analyst was prompted within Tines to either isolate the machine or leave it as is. Screenshots below demonstrate both decision paths:

- **No Isolation**: If the analyst chose not to isolate the machine, a Slack alert was sent indicating that the machine remained online.
  
  ![No Isolation Alert](https://imgur.com/link-to-your-screenshot)

- **Isolation**: If the analyst chose to isolate the machine, Tines automated the isolation process and sent a follow-up Slack alert confirming the action.
  
  ![Isolation Alert](https://imgur.com/link-to-your-screenshot)

![Screenshot 2024-08-15 230555](https://github.com/user-attachments/assets/447be739-caf7-4b0b-87a7-3e19c1704ee2)
![Screenshot 2024-08-15 230955](https://github.com/user-attachments/assets/c4c656db-84f5-40b1-9875-15fb7021a251)
![Screenshot 2024-08-15 224101](https://github.com/user-attachments/assets/8d0aac3b-78e0-4db8-bfd7-5d6787809c17)


![Screenshot 2024-08-15 231313](https://github.com/user-attachments/assets/acbdcd15-7233-45a8-a955-47110cd33707)


![Screenshot 2024-08-15 234155](https://github.com/user-attachments/assets/69884420-10f2-4074-84a1-aeb6197ca273)

![Screenshot 2024-08-15 234101](https://github.com/user-attachments/assets/4f8502c4-133d-4fc3-a35b-486ff18f592a)




  
