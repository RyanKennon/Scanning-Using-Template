<p align="center">
  <img width="560" height="448" alt="image" src="https://github.com/user-attachments/assets/3b1cab95-b678-4542-9897-9239f2f81b24" />
</p>

# Scanning-Using-Template

### Overview Here

---

## Environments and Technologies Used

- Microsoft Azure
- Azure Virtual Network
- Tenable (Security Scanner)

---

## Lab Objectives

---

## Step-by-Step Walkthrough

### Lab Environment

- **Platform:** Microsoft Azure
- **Client Machine:** Windows 11 Pro

### Capture 1

---

### 1) Create Vulnerabilities

1. Log into the **Virtual Machine** and disable **Windows Firewalls**
2. Open the **Computer Management** settings and create a **user** named **Administrator** then add to the **Administrators** group
3. Add the **Guest** user to the **Administrator** group as well

### Capture 2

---

### 2) Create Scan Template

1. Log into **Tenable** and select **Create Scan Template** for an **Advanced Network Scan**
2. In the **Basic** tab make the following changes
   - Turn on **Start the Remote Registry service during the scan**
   - Turn on **Enable administrative shares during the scan**
   - Turn on **Start the Server service during the scan**
  
### Capture 3

3. In the **Discovery** tab make the following changes:
   - Turn on **Ping the remote host**
   - Turn on **Use fast network discovery**
   - Turn on the **TCP** Network Port Scanner
  
### Capture 4
### Capture 5

4. In the **Assessments** tab make the following changes:
   - Turn on **Perform thorough tests**
   - Turn off **Only use credentials provided by the user**
  
## Capture 6
## Capture 7

5. On the **Report** tab add the credentials for the **Virtual Machine**
6. On the **Compliance** tab add the **DISA Microsoft Windows 11 STIG**

## Capture 8

7. On the **Plugins** tab enable the following plugins:
   - **General**
   - **Settings**
   - **Windows**
   - **Windows: Microsoft Bulletins**
   - **Windows: User Management**
   - Click **Policy Compliance** and enable **Windows Compliance Checks**
  
## Capture 9

8. Save the Template

---

### 3) Scan Using Template

1. Create **User Defined** scan using the recently created template
2. Make the following changes to scan then launch scan:
   - **Scanner:** Local Scan Engine
   - **Targets:** `<Windows 11 VM private IP address>`
3. Once the scan is complete check the **vulnerabilities log**

## Capture 10

4. Select the vulnerability and find the **description** and **solution**

## Capture 11

---

