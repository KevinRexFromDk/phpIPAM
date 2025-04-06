# 📦 phpIPAM Auto Install Script
This repository contains an automated installation script for setting up phpIPAM on an Ubuntu server. The script installs and configures the necessary prerequisites, including Apache2, MariaDB, and PHP for a smooth phpIPAM installation.

# 🔧 Features
 - Installs necessary Apache2, MariaDB, and PHP dependencies 🔧
 - Configures MariaDB for phpIPAM database setup 🗄️
 - Prompts for Database Name, Database User, and Password settings with default values 📝
 - Automatically clones the phpIPAM repository and configures it 📂
 - Handles installation errors and stops gracefully if anything fails 🚨

# 📥 Fetch the Install Script
To download the latest version of the **phpipam-autoinstall.sh** script, run the following command:

```bash
wget https://raw.githubusercontent.com/KevinRexFromDk/phpIPAM/refs/heads/main/phpIPAM-autoinstall.sh
```

# ⚙️ Change Execute Permissions
Once the script is downloaded, you'll need to make it executable. Use the following command:

```bash
sudo chmod +x phpipam-autoinstall.sh
```

# 🚀 Running the Script
After changing the script's permissions, you can run it with the following command:

```bash
sudo ./phpipam-autoinstall.sh
```
The script will prompt you to enter the following details during the installation process:
 1. Database Name (default: phpipam)
 2. Database User (default: phpipamadmin)
 3. Database User Password (must match when confirming)

If you leave any input blank, the default values will be used.

# 🛠️ Script Behavior
 - The script installs all necessary dependencies: **Apache2**, **MariaDB**, **PHP** 🏗️
 - It configures the MariaDB database and creates a user for phpIPAM 🗄️
 - It clones the phpIPAM repository into the web root and sets up the configuration file 🖥️
 - If any step fails, the script stops and prints an error message ⚠️
 - After a successful installation, a "completed successfully" message will be displayed 🎉

# 🔧 Customization
You can customize the installation by entering the following parameters when prompted:

Database Name 💬

Database User 🔐

Database Password 🔑

If you leave the input blank, the script will use the default values.

Example of Input Prompt
bash
Kopiér
Rediger
Enter database name (default 'phpipam'): phpipam
Enter database user (default 'phpipamadmin'): phpipamadmin
Enter password for user 'phpipamadmin': [Hidden]
Confirm password: [Hidden]
# 📝 Post-Installation
Once the script completes, you can finish the phpIPAM configuration by following these steps:

Navigate to http://<your-server-ip>/phpipam

Click the "New phpIPAM installation" button

Click "Automatic database installation"

Insert the following details:

MySQL Username: phpipamadmin

MySQL Password: [Hidden]

MySQL Location: 127.0.0.1

MySQL DB Name: phpipam

Click "Show advanced options" and uncheck "Create new database" and "Set permissions to tables"

Click "Install phpIPAM database"

Log in with the username admin and the password you set earlier

Enjoy using phpIPAM!
