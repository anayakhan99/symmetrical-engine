```markdown
# ⚡ EnigMano Instance Deployment

Welcome to **EnigMano** — a tactical, multi-instance deployment system designed for secure, automated Windows environment provisioning via GitHub Actions. 🚀

---

## 🚀 Overview

This repository hosts a powerful GitHub Actions workflow that deploys an *EnigMano instance* on a Windows runner.  
Each instance launches a PowerShell script that sets up remote access, configures secure tunnels with Ngrok, and automates chained deployments — all while maintaining stealthy, precise operation cycles.  

---

## 🎯 Features

- **Instance-specific deployment:** Deploy multiple EnigMano instances by specifying an `INSTANCE` number.
- **Secure tunnels:** Automatically establishes Ngrok TCP tunnels for remote access.
- **Automated chaining:** Each instance triggers the next, ensuring continuous operation.
- **Robust secret validation:** Requires GitHub secrets for authentication and Ngrok tokens.
- **Self-hosted or hosted runners:** Supports both environments with proper termination logic.
- **Detailed logging:** Outputs informative, colorful logs and status notices.
- **Customizable:** Easily adjust parameters like instance number and runtime.

---

## ⚙️ How It Works

1. **Trigger workflow:** Manually trigger deployment via GitHub Actions `workflow_dispatch` with an input for `INSTANCE`.
2. **Validate secrets:** Checks presence of essential secrets (`SECRET_SHAHZAIB` and `NGROK_SHAHZAIB`).
3. **Download script:** Fetches the latest `EnigMano-instance.ps1` from a central repository.
4. **Run PowerShell script:** Executes the script to:
   - Set up RDP access
   - Initialize Ngrok tunnel
   - Create secure user accounts
   - Spin up visual signatures
   - Monitor uptime and handle graceful handoffs
5. **Chain next instance:** Automatically triggers deployment of the next instance.
6. **Shutdown:** Gracefully terminates or reboots based on environment.

---

## 🔑 Prerequisites

- GitHub repository with Actions enabled.
- Two GitHub Secrets configured in your repo:
  - `SECRET_SHAHZAIB` — Personal Access Token or API secret.
  - `NGROK_SHAHZAIB` — Ngrok authentication token.
- Windows runner (self-hosted or GitHub-hosted `windows-latest`).

---

## 📥 Usage

1. Go to the **Actions** tab in your GitHub repo.
2. Select the **EnigMano Instance Deployment** workflow.
3. Click **Run workflow**.
4. Enter the instance number (e.g., `1`, `2`, `3`...).
5. Hit **Run** and watch the magic unfold! ✨

---

## 🛠️ Environment Variables

| Variable        | Description                                      |
|-----------------|------------------------------------------------|
| `INSTANCE_ID`   | The numeric identifier of the current instance.|
| `SECRET_SHAHZAIB` | Your GitHub secret token for authentication.   |
| `NGROK_SHAHZAIB` | Your Ngrok auth token to create tunnels.        |
| `REPO`          | The repository name triggering the workflow.   |
| `WORKFLOW_FILE` | The workflow file name (`enigmano.yml`).        |
| `DEPLOYMENT_ID` | The unique deployment run ID from GitHub.      |

---

## ⚠️ Important Notes

- Ensure your secrets are properly configured or the workflow will abort.
- The PowerShell script downloads dynamically; always verify the source for security.
- Ngrok tunnels expose TCP ports — protect your credentials carefully.
- This system is designed for automated chaining and may consume resources; monitor usage.

---

## 💡 Troubleshooting

- **Missing secrets?** Add them under your repo’s *Settings → Secrets and variables*.
- **Download failures?** Confirm access to the raw script URL.
- **Tunnel issues?** Verify Ngrok token and network availability.
- **Unexpected shutdowns?** Review logs for errors and runner environment compatibility.

---

## 🙌 Credits & Acknowledgements

Developed and powered by **SHAHZAIB-YT** — keeping deployments precise, secure, and unstoppable. 🔋  
Inspired by tactical automation and seamless multi-instance workflows.

---

## 📜 License

MIT License © 2025 SHAHZAIB-YT

---

Thank you for deploying EnigMano!  
Run safe, stay stealthy, and power on! ⚡

---

*For more info, check the [`enigmano.yml`](./enigmano.yml) workflow and the [`EnigMano-instance.ps1`](./EnigMano-instance.ps1) script.*

---
```
