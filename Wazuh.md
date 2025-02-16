### Installing ELK Stack on Ubuntu Server

This guide explains how to install the Wazuh server on **Ubuntu Server** step-by-step.

---

#### Prerequisites
1. **Ubuntu Server**: Ensure your server is updated.
2. **Minimum Requirements**:
   - **CPU**: 2 cores.
   - **RAM**: 4 GB (8 GB recommended).
   - **Storage**: 50 GB free space.
3. **Privileges**: You need root or sudo access.

---

### Step 1: Update and Prepare Ubuntu
Run the following commands to update your server:
```bash
sudo apt update && sudo apt upgrade -y
sudo apt install wget curl apt-transport-https software-properties-common -y
```

---

### Step 2: Installing Wazuh
1. Download and run the Wazuh installation assistant.
   ```bash
   curl -sO https://packages.wazuh.com/4.9/wazuh-install.sh && sudo bash ./wazuh-install.sh -a
   ```

   Once the assistant finishes the installation, the output shows the access credentials and a message that confirms that the installation was successful.
   ```bash
    INFO: --- Summary ---
    INFO: You can access the web interface https://<wazuh-dashboard-ip>
    User: admin
    Password: <ADMIN_PASSWORD>
    INFO: Installation finished.
   ```

2. You can access the wazuh page by typing your ubuntu ip in the browser and then logging in using the credentials you have just been given.

  - **Username**: admin
  - **Password**: <ADMIN_PASSWORD>
---

### Congratulations! You've just installed wazuh
