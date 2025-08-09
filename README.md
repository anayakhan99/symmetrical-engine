Got it! Here's the updated README markdown with wrapped code blocks and flowchart, so it stays neat and easy to read on GitHub. I replaced the triple backticks with fenced code blocks using indentation and line breaks for better wrapping in the flowchart, and shortened long lines.

````markdown
# ⚡✨ EnigMano Instance Deployment ✨⚡

Welcome to **EnigMano** — your ultimate **automated multi-instance deployment** solution! 🚀  
This GitHub Actions workflow spins up secure, remote Windows environments with 🔥 speed and precision — perfect for labs, testing, or ephemeral remote desktops.

---

## 🌟 Why EnigMano?

Imagine launching **multiple chained Windows instances** effortlessly,  
each accessible over the internet via secure Ngrok tunnels.  
EnigMano automates the entire process:

- 💻 Sets up Windows RDP access with robust security  
- 🌍 Rotates through Ngrok regions for optimal connectivity  
- 🔄 Automatically triggers the next instance for continuous deployment  
- ⏳ Manages lifecycle with graceful shutdowns or reboots  
- 🛡️ Securely handles secrets and tokens with GitHub Actions  

---

## 🚀 Quick Overview

| Feature               | Description                                    |
|-----------------------|------------------------------------------------|
| **Trigger**           | Manual GitHub Workflow Dispatch (`INSTANCE`)   |
| **Runner Environment**| Windows-latest VM                              |
| **Secrets Required**  | `SECRET_SHAHZAIB` (GitHub Token), `NGROK_SHAHZAIB` (Ngrok Token) |
| **Key Script**        | `EnigMano-instance.ps1` (PowerShell)           |

---

## 🛠️ Workflow Breakdown

### 1️⃣ Deployment Parameters  
Displays your chosen instance number, repository info, and deployment metadata —  
so you’re always in control.

### 2️⃣ Secrets Validation  
Halts deployment if critical secrets are missing — no guesswork, no silent failures. 🔐

### 3️⃣ Script Download  
Fetches the latest **EnigMano PowerShell script** to your runner for execution.

### 4️⃣ Script Execution  
Runs the PowerShell script that sets up Ngrok tunnels, configures RDP, and prepares your Windows instance.

### 5️⃣ Completion & Handoff  
Outputs the remote access credentials and triggers the next instance deployment seamlessly.

---

## 🔒 Security & Access

- Ngrok tunnels protect your instance with secure TCP forwarding.  
- Windows RDP is enabled and secured with predefined credentials.  
- Secrets are injected only via GitHub Secrets — never hardcoded.  
- Access info is displayed as GitHub Action notices for quick copy-paste.  

---

## 📦 How To Use EnigMano

1. **Fork or clone** this repository.  
2. **Add GitHub Secrets:**  
   - `SECRET_SHAHZAIB` — Your GitHub Personal Access Token (repo + workflow permissions)  
   - `NGROK_SHAHZAIB` — Your Ngrok Auth Token  
3. Place the workflow YAML in `.github/workflows/enigmano.yml`.  
4. Go to **Actions > EnigMano Instance Deployment** in your repo.  
5. Click **Run workflow**, enter your desired `INSTANCE` number, and start deployment!  
6. Watch logs for your RDP tunnel URL & credentials, then connect and enjoy!  

---

## 🧩 Behind the Scenes (Flowchart)

```mermaid
flowchart TD
    A[👆 Manual Workflow Dispatch] --> B[🔐 Validate Secrets]
    B --> C[📥 Download PowerShell Script]
    C --> D[⚔️ Execute EnigMano-instance.ps1]
    D --> E[🌐 Setup Ngrok Tunnel & RDP]
    E --> F[📢 Output Access Credentials]
    F --> G[🔄 Trigger Next Instance Deployment]
    G --> H[⏰ Manage Shutdown/Reboot]
````

---

## 💡 Pro Tips

* Rotate Ngrok regions to avoid connectivity issues — built-in automatic cycling.
* Use instance chaining for continuous environment availability without manual triggering.
* Customize the PowerShell script for your specific security or setup needs.

---

## 🙌 Credits & License

Made with ❤️ by **SHAHZAIB-YT**.
Feel free to fork, improve, and share. Keep attribution intact and spread the ⚡EnigMano⚡ magic!

---

## 📬 Need Help?

Raise an issue on GitHub or reach out to the author for support and feature requests.

---

🎯 **EnigMano** — Powering seamless, secure remote Windows deployments, one instance at a time.
**#Automation #GitHubActions #PowerShell #Ngrok #RemoteDesktop #EnigMano**

---

*Ready to deploy your next instance? Just hit **Run workflow** and watch the magic happen!* ✨

```

If you want me to force-wrap the long mermaid lines or split them differently, just say so! But this is the best for GitHub's markdown rendering and natural wrapping.
```
