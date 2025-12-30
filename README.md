[README.md](https://github.com/user-attachments/files/24379503/README.md)
#  Nexus Skill Hub

Welcome to the official community library for **Project Nexus**. This repository is the central heart for extending Nexus with Local AI, JavaScript, and Python automations.

##  How to Install Skills
1. Open **Nexus** on your Mac.
2. Select **"Explore Skills..."** from the Menu Bar.
3. Find a tool you like and click **"Add"**. It will be ready to use instantly!

---

##  How to Contribute (Submit your own Skill)
We welcome all contributions! To keep our community safe, every submission is manually reviewed.

1. **Create:** Build your automation in the Nexus App using the **Design Editor**.
2. **Export:** Use the **"Publish to Hub"** button in the editor. This saves a `.nexus` file to your Downloads.
3. **Fork:** Fork this repository on GitHub.
4. **Upload:** Add your `.nexus` file to the `skills/` folder.
5. **Register:** Add your skill's metadata to `catalog.json` (see the format below).
6. **Pull Request:** Submit a Pull Request. We will review your code and merge it if it passes security checks.

---

##  Security & Quality Guidelines
To be accepted, your Skill **must** follow these rules:

### 1. Privacy First
*   **No Data Siphoning:** Do not send clipboard data to personal servers.
*   **Local LLM Priority:** Use `nex.llm.generate` for text tasks. Only use external APIs (OpenAI/Gemini) if absolutely necessary (e.g., specialized data lookup).
*   **No Hardcoded Secrets:** Never put API keys in the code. Use `env.YOUR_KEY` so users can provide their own keys securely.

### 2. Sandbox & Safety
*   **No Dangerous OS Calls:** In Python, avoid `os.system` or `subprocess` that modifies system files.
*   **Domain Allowlist:** If your script uses `nativeFetch`, you must list the domains in the "Permissions" field.

### 3. Polish & Utility
*   **Clear Purpose:** One Skill = One Problem. Make it atomic.
*   **SF Symbols:** Use [Apple SF Symbols](https://developer.apple.com/sf-symbols/) for your icon (e.g., `sparkles`, `doc.text.fill`).
*   **English First:** Descriptions and names should be in English to serve the global community.

---

##  Catalog Format
Add your entry to `catalog.json` like this:

```json
{
  "id": "author-tool-name",
  "name": "Cool Tool Name",
  "description": "What it does in 1 sentence.",
  "author": "YourGitHubUser",
  "category": "Office | Dev | Social | Data | Utility",
  "icon": "sf-symbol-name",
  "downloadURL": "https://raw.githubusercontent.com/bananamats94/Nexus-Skills-Hub/main/skills/your_file.nexus",
  "isPro": false
}
```

---

##  License & Disclaimer
By contributing, you agree that your code is provided under the MIT License. Project Nexus is not responsible for third-party scripts. Use at your own risk.
