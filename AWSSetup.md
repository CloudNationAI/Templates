
# ☁️ Amazon Web Services (AWS) Integration with CloudNation AI

CloudNation AI supports two methods to connect your AWS account:

---

## 🔐 Option 1: Using Access Credentials

### 🟢 Step 1: Gather Credentials

1. Log in to your **AWS Console**
2. Navigate to your **IAM dashboard**
3. Create a **new user** (or use an existing one) with **programmatic access**
4. Attach the necessary **permissions policies** (e.g., `SecurityAudit`)
5. After creation, download the **Access Key ID** and **Secret Access Key**
6. Copy your **AWS Account ID** from the **My Account** section

---

### 🚀 Step 2: Setup in CloudNation AI

1. Go to **CloudNation AI** → `Providers` → `Add Provider`
2. Select **AWS**
3. Enter:
   - **Account ID**
   - **Alias**
   - Select **Secrets** as the connection method
   - Enter **Access Key**
   - Enter **Secret Key**
4. Click **Next** → **Test Connection** → **Launch Scan**

---

## 🛡️ Option 2: Using IAM Role via CloudFormation

### 🟢 Step 1: Prepare IAM Role

1. Log in to your **AWS Console**
2. 📋 Copy your **Account ID**
3. Navigate to **CloudFormation** → **Stacks** → **Create Stack**
4. Select **"With new resources (standard)"**
5. Choose **Upload a template file**

📥 **Download the IAM template from:**  
[CloudNation AI IAM Template](https://github.com/CloudNationAI/Templates/blob/main/cloudnation-prowler-role.yml)

6. Upload the downloaded `.yml` file
7. Enter a **stack name** (e.g., `cloudnationai-role`)

### 🔧 Parameters:
- Do **NOT** change the Account ID
- Set **External ID** as:  
  `6ee03c25-dbe4-40a9-ba7d-f44837cd81e0`

8. Click **Next** → **Next** → **Create Stack**

⏳ Wait for the stack to complete creation

---

### 📄 Step 2: Get IAM Role ARN

1. Once the stack is created, go to the **Outputs** tab
2. 📋 **Copy the ARN** shown there

---

### 🚀 Step 3: Setup in CloudNation AI

1. Go to **CloudNation AI** → `Providers` → `Add Provider`
2. Select **AWS**
3. Enter:
   - **Account ID**
   - **Alias**
   - Select **IAM** as the connection method
   - Choose **AWS SDK Default** as the auth method in dropdown
   - Paste the **IAM Role ARN**
4. Click **Next** → **Test Connection** → **Launch Scan**
