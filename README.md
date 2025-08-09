````markdown
# ⚡ EnigMano Instance Deployment

Welcome to **EnigMano** — a powerful, automated multi-instance deployment workflow designed to launch and manage remote Windows environments seamlessly using GitHub Actions and PowerShell.

---

## 🚀 Overview

This GitHub Actions workflow automates the deployment of individual **EnigMano instances** — each running a specialized PowerShell script that:

- Establishes secure remote desktop access via Ngrok tunnels.
- Rotates through multiple geographic Ngrok regions for robust connectivity.
- Sets up environment and security configurations.
- Automatically triggers the next instance for continuous, chained deployments.
- Handles graceful shutdown or reboot depending on the environment.

Each instance is uniquely identified and controlled through the `INSTANCE` input parameter, allowing flexible multi-instance scaling.

---

## ⚙️ Workflow Details

- **Trigger:** Manual dispatch (`workflow_dispatch`) with an input parameter `INSTANCE` (default: `1`).
- **Runner:** Runs on a fresh `windows-latest` environment.
- **Secrets Required:**
  - `SECRET_SHAHZAIB` — GitHub API token with repo and workflow permissions.
  - `NGROK_SHAHZAIB` — Ngrok authentication token for tunnel creation.

### Main Steps:

1. **Parameter Logging:** Displays deployment metadata such as instance number and workflow details.
2. **Secrets Validation:** Ensures all necessary secrets are provided before proceeding.
3. **Script Download:** Fetches the core `EnigMano-instance.ps1` PowerShell script from a remote source.
4. **Instance Execution:** Runs the PowerShell script with elevated execution policy.
5. **Completion Status:** Reports successful execution and instance completion.

---

## 🔐 Security & Access

- The PowerShell script configures Windows Remote Desktop Protocol (RDP) securely.
- A randomly rotated Ngrok TCP tunnel exposes RDP over the internet with region fallback.
- Credentials and tunnel URLs are securely injected via GitHub Secrets.
- Instance credentials are displayed in the workflow logs as actionable notices for quick access.

---

## 🎯 Use Cases

- Automated multi-instance deployment for remote access labs or ephemeral environments.
- Rapid setup of disposable Windows environments accessible remotely.
- Chained instance triggering for continuous deployment or scale testing.

---

## 🛠️ Prerequisites

- A GitHub repository to host this workflow.
- GitHub Secrets configured with:
  - `SECRET_SHAHZAIB`: Personal Access Token with repo and workflow dispatch scopes.
  - `NGROK_SHAHZAIB`: Ngrok authentication token.
- Basic familiarity with GitHub Actions and PowerShell scripting.
- Ngrok account for secure tunneling.

---

## 🧩 How to Use

1. Fork or clone this repository.
2. Add the workflow YAML (`enigmano.yml`) into `.github/workflows/`.
3. Add the required secrets in your GitHub repository settings.
4. Manually trigger the workflow via GitHub Actions UI:
   - Select the `INSTANCE` number to deploy.
5. Monitor the workflow logs for:
   - Tunnel URL and RDP credentials.
   - Deployment status and progress.
6. Use the exposed RDP address to connect to your EnigMano instance.

---

## ⚡ Architecture & Flow

```mermaid
flowchart TD
    A[GitHub Workflow Dispatch] --> B[Validate Secrets]
    B --> C[Download EnigMano-instance.ps1]
    C --> D[Run PowerShell Script]
    D --> E[Setup Ngrok Tunnel & RDP]
    E --> F[Display Access Info]
    F --> G[Trigger Next Instance Workflow]
    G --> H[Shutdown or Reboot]
````

---

## 📜 License & Credits

**EnigMano** is created and maintained by **SHAHZAIB-YT**.
Feel free to fork, improve, and customize. Please keep attribution in place.

---

## 📫 Support

For questions, feature requests, or contributions, open an issue or contact the author on GitHub.

---

*Deploy your own remote Windows instance network with EnigMano and stay in control — effortlessly.*
\#EnigMano #RemoteAccess #GitHubActions #PowerShell #Ngrok #Automation

```
```
