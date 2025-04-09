# 🔗 Steps to Connect Microsoft Azure Account with CloudNation AI

## 🟢 Step 0: Prerequisites
Ensure you have:
- An **active Azure account**
- An **active Subscription ID**

📌 **Copy the Subscription ID** from the Azure Portal **Home Screen**.

---

## 🛠️ Step 1: App Registration

1. Go to **Azure Portal Home**
2. Use the **search bar** and search for:  
   `Microsoft Entra ID`
3. Navigate to **App Registrations** → Click **+ New registration**

### Fill in the App Registration Form:
- **Name**: `Cloudnationai`
- Click on **Register**

---

### On the Results Page:
- 📋 **Copy** `Directory (tenant) ID` → _use this as_ **Tenant ID**
- 📋 **Copy** `Application (client) ID` → _use this as_ **Client ID**

---

### Add Client Secret:
1. Go to **Client credentials** → **Certificates & secrets**
2. Click **+ New client secret**
3. **Description**: `cloudnationai`
4. Click **Add**

⚠️ Once created:
- 📋 **Copy the `Value`** → _use this as_ **Client Secret**

---

## 🚀 Final Setup in CloudNation AI

1. Navigate to **CloudNation AI** → `Providers` → `Add Provider`
2. Enter:
   - **Subscription ID**
   - **Alias**
   - **Client ID**
   - **Client Secret**
   - **Tenant ID**
3. Click **Test Connection**
4. Click **Launch Scan**
