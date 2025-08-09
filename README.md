# ⚡ EnigMano Instance Deployment — Your Tactical Multi-Instance Commander

![GitHub Workflow](https://img.shields.io/badge/GitHub-Workflow-blue?style=for-the-badge&logo=github&logoColor=white)  
![Windows](https://img.shields.io/badge/Runner-Windows-lime?style=for-the-badge&logo=windows&logoColor=white)  
![PowerShell](https://img.shields.io/badge/Script-PowerShell-178600?style=for-the-badge&logo=powershell&logoColor=white)

---

## 🔥 What Is This?

This GitHub Actions workflow automates deploying **EnigMano** instances — Windows fortress environments orchestrated with stealth and precision.  
Trigger it manually, input your **instance number**, and let the silent hand execute the mission.

---

## 🚀 Features & Highlights

- Manual trigger with instance input for multi-instance management  
- PowerShell deployment on Windows runners (`windows-latest`)  
- Validates required secrets (`SECRET_SHAHZAIB` & `NGROK_SHAHZAIB`)  
- Downloads and executes the latest `EnigMano-instance.ps1` script  
- Clear, step-by-step logging for easy tracking  
- Final status report on completion  

---

## 🛠️ How It Works

1. **Trigger the workflow** with an instance number (e.g., 1, 2, 3).  
2. **Sets up environment variables** including secrets and repo info.  
3. **Logs deployment parameters** like instance ID and workflow info.  
4. **Validates required secrets**, aborting if missing.  
5. **Downloads the deployment script** from a trusted source.  
6. **Runs the PowerShell script** to deploy your EnigMano instance.  
7. **Logs final status** with success or failure information.  

---

## 🎯 Usage

- Fork this repository, and enable Actions. 
- Open your repo's **Actions** tab  
- Select **⚡ EnigMano Instance Deployment** workflow  
- Click **Run workflow**  
- Enter the **INSTANCE** number (default: 1)  
- Confirm & watch your fortress deploy ⚔️  

---

## 🔐 Prerequisites

- Runner: **windows-latest** (Windows environment)  
- GitHub secrets configured:  
  - `SECRET_SHAHZAIB` (your secret token)  
  - `NGROK_SHAHZAIB` (your Ngrok auth token)  

---

## ⚠️ Notes & Tips

- Keep your secrets **safe and confidential** 🔒
- Use in **secure/private environments only**  

---

## 🙌 Credits

Built & maintained by **SHAHZAIB-YT** — powering your fortress with tactical precision. 🔋

---

Ready to deploy your EnigMano fortress? Command the silent hand now! ⚡🛡️
