# ☁️ Google Cloud Platform (GCP) Integration with CloudNation AI

## 🟢 Step 1: GCP Project Setup

1. Go to the **[GCP Console](https://console.cloud.google.com)**
2. Create a **new project** if not already available
3. 📋 **Copy the Project ID**  
   → _Use this as_ **Project ID** in CloudNation AI

---

## 🛠️ Step 2: Authenticate via Cloud Shell

1. In the **GCP Console**, click **Activate Cloud Shell** (top-right terminal icon)
2. Authorize Cloud Shell if prompted

### Run the following command:
```
gcloud auth application-default login
```

3. Type `Y` when prompted
4. Open the **authentication URL** shown in the terminal
5. Select your **Google account**
6. Complete the authentication and **copy the authentication code**
7. Paste the code back in the **Cloud Shell terminal**

---

## 📄 Retrieve Credentials

1. After successful login, a temporary **credentials file** is generated
2. Run:
```
cat <file_name>
```
Replace `<file_name>` with the actual name of the credentials file shown after login

### Extract the following values:
- `client_id`
- `client_secret`
- `refresh_token`

---

## 🚀 Final Setup in CloudNation AI

1. Go to **CloudNation AI** → `Login` → `Providers` → `Add Provider`
2. Select **GCP**
3. Enter:
   - **Project ID**
   - **Alias**
   - **Client ID**
   - **Client Secret**
   - **Refresh Token**
4. Click **Test Connection**
5. On success, click **Launch Scan**
