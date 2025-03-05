# 🚫 Internet Blocking HOSTS List

This repository contains a **HOSTS** file designed to block internet connections to specific domains. It can be used with ad blockers, DNS-based filtering systems, or manually applied to your system's HOSTS file to prevent access to unwanted sites.

## 📌 Features
- Blocks internet by blocking a wide range of domains
- Compatible with popular ad blockers such as [AdGuard](https://adguard.com/), [Pi-hole](https://pi-hole.net/), and [uBlock Origin](https://ublockorigin.com/).

## 📂 Installation & Usage
### 🖥️ Manual Installation
1. **Download the latest HOSTS file**
   ```sh
   wget https://raw.githubusercontent.com/anttitane/hosts-list-to-block-internet/main/hosts -O /etc/hosts
   ```

2. **Apply the changes:**
   - **Windows:** Copy the `hosts` file to `C:\Windows\System32\drivers\etc\hosts`.
   - **Mac/Linux:** Move the file to `/etc/hosts`.
   - Flush the DNS cache:
     ```sh
     ipconfig /flushdns  # Windows
     sudo dscacheutil -flushcache  # macOS
     sudo systemctl restart nscd  # Linux
     ```

### 🛠️ Using with Ad Blockers
- **Pi-hole:** Add the raw URL to the Pi-hole block list.
- **AdGuard:** Import the HOSTS file into AdGuard Home.
- **uBlock Origin:** Add the raw URL in the "Filter Lists" section.

## 🔄 Updating the List
To keep your blocklist updated, you can set up a cron job or scheduled task to automatically download the latest version:
```sh
wget -qO /etc/hosts https://raw.githubusercontent.com/YOUR_GITHUB_USERNAME/YOUR_REPO_NAME/main/hosts
```

## 🤝 Contributing
Have domains to add or remove? Feel free to submit a pull request or open an issue.

---

⭐ **Star this repository** if you find it useful!

