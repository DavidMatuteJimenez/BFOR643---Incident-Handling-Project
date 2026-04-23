# Investigating Phishing Emails through CyberChef & VirusTotal

## 1. Project Overview
**Author: Rachael**

[Content here]

---

## 2. Project Relevance
**Author: Rachael**

[Content here]

---

## 3. Methodology
**Author: Team**

### 3.1 Data Sample
**Author: Rachael**

[Content here]

### 3.2 CyberChef
**Author: Komali**

CyberChef is a tool used to analyze, decode and encode data. When we looked at the email sample, it stated that the file was encoded in Base64. This encoding is used to trasmit binary data over systems that only support text and is used to hide malicious URLs/ scripts from security tools. 

After opening: https://gchq.github.io/CyberChef/, a portion of the email was pasted into the input field. The content seemed like random characters and looked like it was encoded as Base64. "From Base64" is an operation that helped decode this encoded string, so it was dragged under recipes. After clicking the button "BAKE", it decoded the encoded string to reveal a malicious link which will be discussed in detail under "RESULTS" section.

(give more details and images)


### 3.3 VirusTotal
**Author: Komali**

VirusTotal is a cloud-based malware analysis platform that scans and verifies if any files/URLs/IP Addressses are flagged as malicious. It is very useful for analysis as it scans these against 80+ antivirus engines and provides a detailed report. 

Indicators of Compromise (IOCs) such as IP Address, the link embedded into the encoded Base64 string were submitted to this tool. After scanning each IOC, there were 0 flags for any malicious content. However, it is important to use multiple tools to verify if any emails are malicious as there was email authenticaion failures when analyzing email headers.

Multiple tools must be used together to determine if an email is malicious or not. Since this is a sample, VirusTotal did not flag any of the embedded links, but in real life, VirusTotal can be used to verify if any embedded content is malicious or not. 

(give more details)



## 4. Development Environment

### VM Setup
**Author: David**

## To Run This Project (Step-By-Step Guide)

### 4.2 Download and Install UTM

**Step 1:** Visit [https://mac.getutm.app/](https://mac.getutm.app/)

**Step 2:** Click the download button for macOS

**Step 3:** Open the downloaded `.dmg` file

**Step 4:** Drag UTM to your Applications folder

**Step 5:** Open Applications folder and launch UTM

**Step 6:** Grant any necessary permissions when prompted

---

### 4.3 Deploy Kali Linux on UTM

**Step 7:** Follow Kali Linux's official UTM installation guide:
[https://www.kali.org/docs/virtualization/install-utm-guest-vm/](https://www.kali.org/docs/virtualization/install-utm-guest-vm/)

This guide will walk you through:
* Downloading the Kali Linux ARM64 image for UTM
* Creating a new virtual machine in UTM
* Allocating CPU, RAM, and storage resources
* Importing the Kali Linux image

---

### 4.4 Setup and Configure Kali Linux

**Step 8:** Follow Kali Linux's installation and setup guide:
[https://www.kali.org/docs/installation/hard-disk-install/](https://www.kali.org/docs/installation/hard-disk-install/)

This guide will walk you through:
* Initial Kali Linux boot and configuration
* Partitioning and disk setup
* User account creation
* System updates and package configuration
* Desktop environment setup

---

### 4.5 Login to Kali Linux

**Step 9:** At the Kali Linux login screen, enter:
* **Username:** `kali`
* **Password:** `kali`

**Step 10:** Press Enter to login

---

### 4.6 Use CyberChef and VirusTotal

**Step 11:** Open a web browser in Kali Linux

**Step 12:** Visit CyberChef at [https://cyberchef.io/](https://cyberchef.io/)

**Step 13:** Use CyberChef for your analysis tasks

**Step 14:** Visit VirusTotal at [https://www.virustotal.com/](https://www.virustotal.com/)

**Step 15:** Use VirusTotal for your scanning and analysis tasks

---

## 5. Results

### 5.1 CyberChef
**Author: Komali**
The portion of the email has content encoded in Base64 which converts data into 64 ASCII characters. Base64 encoding itself is not malicious but it is commonly used to embedded malicious scripts/URLs into the final string to bypass security tools.

Using CyberChef, the Base64 string was analyzed and decoded. The encoded string was pasted into the input field and "From Base64" operation was applied to the recipes. After hitting the button "BAKE", it decoded the string and revealed the malicious URL:

` <a href="https://blog1seguimentmydomaine2bra.me/">Clique aqui</a></font> `

This URL does not seem to be related to Bradesco Bank (the bank it is claiming to be) and the anchor text of "Clique aqui" (Click here) , seems to be very generic and suspicious.

<img width="1435" height="790" alt="Screenshot 2026-04-22 at 9 58 34 PM" src="https://github.com/user-attachments/assets/26c8943a-889e-4a0a-8802-3d894c2bc896" />

### 5.2 VirusTotal
**Author: David**

[Content here]

---

## 6. Documentation

[Content here]

---

### ✒️ Authors
- Rachael
- David
- Komali
