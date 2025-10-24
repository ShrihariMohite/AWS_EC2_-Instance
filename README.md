# ☁ Task 2: Launch a Virtual Machine (VM) Instance (AWS EC2)

## 🎯 Objective
To understand how cloud virtual machines work by creating, configuring, and connecting to a cloud-based server instance using the **AWS EC2 Free Tier**.  
This task introduces the concept of **Infrastructure-as-a-Service (IaaS)** — the foundational layer of cloud computing.

---

## 🧰 Tools Used
- **Platform:** AWS (Amazon Web Services)
- **Service:** EC2 (Elastic Compute Cloud)
- **Operating System:** Linux
- **Instance Type:** t2.micro
- **Region:** Asia Pacific (Mumbai) – `ap-south-1`

---

## 🧭 Step-by-Step Implementation

### **Step 1 — AWS Account Setup**
1. Go to [https://aws.amazon.com/](https://aws.amazon.com/).
2. Create a new AWS account and activate the **Free Tier**.
3. Log in to the **AWS Management Console** and select the nearest region (e.g., `ap-south-1`).

---

### **Step 2 — Launch an EC2 Instance**
1. Navigate to **EC2 → Instances → Launch Instance**.
2. Configure the following:
   - **Name:** `my-first-vm`
   - **AMI (Image):** Ubuntu Server 22.04 LTS
   - **Instance Type:** `t2.micro` (Free Tier)
3. **Create a Key Pair:**
   - Type: RSA  
   - File format: `.pem`
   - Download and store the key securely.
4. **Network Settings:**
   - ✅ Allow SSH (port 22)
   - ✅ Allow HTTP (port 80)
   - ✅ Allow HTTPS (port 443)
5. **Storage:** Default (8 GB gp2)
6. Click **Launch Instance**.

---

### **Step 3 — Verify Instance**
- Go to **EC2 → Instances**.
- Check that the instance state is **Running**.
- Note the **Public IPv4 address**.
  
---

### **Step 4 — Connect to the Instance**
#### **Option 1: AWS Console (Browser SSH)**
1. Select the instance.
2. Click **Connect → EC2 Instance Connect → Connect**.
3. Run the following commands:
   ```bash
   uname -a
   whoami
   ls
