<p align="center">
  <img width="560" height="448" alt="image" src="https://github.com/user-attachments/assets/3b1cab95-b678-4542-9897-9239f2f81b24" />
</p>

# Vulnerability Management: Custom Scan Template Development & Execution

This project successfully demonstrated the creation and use of a customized vulnerability scan template within a controlled environment. A reusable scan template was configured and executed to assess the system. The scan successfully detected the injected vulnerabilities and generated structured reporting based on the defined template settings. This project reinforced the importance of standardized scanning procedures, repeatability in vulnerability assessments, and understanding how scan configurations influence detection accuracy and reporting outcomes.

---

## Environments and Technologies Used

- Microsoft Azure
- Azure Virtual Network
- Tenable (Security Scanner)

---

## Lab Objectives
 
- Configure and customize a vulnerability scan template  
- Define scan policies, scope, and assessment settings  
- Execute a vulnerability scan using the custom template  
- Analyze scan results

---

## Step-by-Step Walkthrough

### Lab Environment

- **Platform:** Microsoft Azure
- **Client Machine:** Windows 11 Pro

<p align="center">
  <img width="1252" height="404" alt="Capture1" src="https://github.com/user-attachments/assets/ab8be9f3-bd9c-477f-97dd-43cf3a60257d" />
</p>

---

### 1) Create Scan Template

1. Log into the **Virtual Machine** and disable **Windows Firewalls**
2. Log into **Tenable** and select **Create Scan Template** for an **Advanced Network Scan**
3. In the **Basic** tab make the following changes
   - Turn on **Start the Remote Registry service during the scan**
   - Turn on **Enable administrative shares during the scan**
   - Turn on **Start the Server service during the scan**
  
<p align="center">
  <img width="1340" height="171" alt="Capture3" src="https://github.com/user-attachments/assets/bb8cfdcc-edba-41dc-983b-a36d6b55ba4b" />
</p>

4. In the **Discovery** tab make the following changes:
   - Turn on **Ping the remote host**
   - Turn on **Use fast network discovery**
   - Turn on the **TCP** Network Port Scanner
  
<p align="center">
  <img width="603" height="200" alt="Capture4" src="https://github.com/user-attachments/assets/5e1abbce-5645-4f11-a936-9159dde3793d" />
</p>

<p align="center">
  <img width="598" height="107" alt="Capture5" src="https://github.com/user-attachments/assets/cb6a4bba-aaf6-4661-a179-5edb7be60368" />
</p>

5. In the **Assessments** tab make the following changes:
   - Turn on **Perform thorough tests**
   - Turn off **Only use credentials provided by the user**
  
<p align="center">
  <img width="586" height="93" alt="Capture6" src="https://github.com/user-attachments/assets/89c092d2-ba21-4dc3-bfeb-033e6452a7f4" />
</p>

<p align="center">
  <img width="576" height="97" alt="Capture7" src="https://github.com/user-attachments/assets/ddf077d8-23be-4702-b6c5-cc4a81c7ec1e" />
</p>

6. On the **Report** tab add the credentials for the **Virtual Machine**
7. On the **Compliance** tab add the **DISA Microsoft Windows 11 STIG**

<p align="center">
  <img width="611" height="600" alt="Untitled Diagram drawio" src="https://github.com/user-attachments/assets/a614bf86-b875-40ad-9a06-05f1023d1257" />
</p>

8. On the **Plugins** tab enable the following plugins:
   - **General**
   - **Settings**
   - **Windows**
   - **Windows: Microsoft Bulletins**
   - **Windows: User Management**
   - Click **Policy Compliance** and enable **Windows Compliance Checks**
  
<p align="center">
  <img width="1515" height="241" alt="Capture9" src="https://github.com/user-attachments/assets/45486979-2689-4230-9c6b-b1fc6efc7ee1" />
</p>

9. Save the Template

---

### 2) Scan Using Template

1. Create **User Defined** scan using the recently created template
2. Make the following changes to scan then launch scan:
   - **Scanner:** Local Scan Engine
   - **Targets:** `<Windows 11 VM private IP address>`
3. Once the scan is complete check the **vulnerability log**

<p align="center">
  <img width="1353" height="439" alt="Capture10" src="https://github.com/user-attachments/assets/8e3543b4-ba44-4fd8-bc39-fb6df019357f" />
</p>

4. Select the vulnerability and find the **description** and **solution**

<p align="center">
  <img width="1387" height="280" alt="Capture11" src="https://github.com/user-attachments/assets/996a8699-fd29-447b-b3af-a40e528d4961" />
</p>

---

## Outcome 
  
- Built and configured a reusable vulnerability scan template  
- Executed a standardized scan using the custom configuration  
- Demonstrated consistency and repeatability in vulnerability assessments

---

## Skills Demonstrated

- Vulnerability Management  
- Scan Template Configuration  
- Security Assessment  
- Risk Identification  
- Security Testing Methodology  
- Scan Policy Customization     
- Standardized Security Procedures  
