# Joomla Development Environment Setup

Joomla is a widely-used content management system (CMS) currently powering around 3-4% of websites on the internet.

- **CMS Definition**: A CMS allows users to create, manage, and publish digital content without needing advanced technical knowledge.
- **Main Project**: [joomla-cms GitHub Repository](https://github.com/joomla/joomla-cms)
- **Joomla Org Channel**: [Joomla Community](https://joomlacommunity.cloud.mattermost.com/main/channels)

---

## Setting Up Your Joomla Development Environment

Here are some essential resources for getting familiar with Joomla and installing a Joomla development environment:

### Quick Start Guide for Joomla 5.x as a Content Management System

---

### Tools You Need

To get started, you’ll need the **AMP stack**. An AMP stack includes:

- **Apache** (web server)
- **MySQL** (database server)
- **PHP** (scripting language)

For this tutorial, we’ll use **XAMPP** as the AMP stack.

#### 1. Install and Configure XAMPP

**XAMPP** provides an easy-to-install package for Apache, MySQL, and PHP. Here's how to set it up:

- **Download XAMPP** and install it on your computer.
- Open the XAMPP Control Panel and start the **Apache** and **MySQL** services.

#### 2. Configure MySQL with XAMPP

To set a MySQL password for better security:

1. Click on the **Shell** button in the XAMPP Control Panel to open the command line interface.
2. At the prompt, enter the following command:
   ```bash
   mysqladmin.exe -u root password secretpassword
   ```
   You can replace `secretpassword` with your own password.

3. After setting the password, you'll need to update the `phpMyAdmin` configuration file for it to work properly:

   - Open `c:\xampp\phpMyAdmin\config.inc.php` in a text editor.
   - Find line 21:
     ```php
     $cfg['Servers'][$i]['password'] = '';
     ```
   - Update it to:
     ```php
     $cfg['Servers'][$i]['password'] = 'secretpassword';
     ```
   - Save and close the file.

---

### Joomla Files

1. **Download the Latest Joomla 5.x**: [Download Joomla](https://www.joomla.org)
2. **Set Up Joomla in XAMPP**:
   - Navigate to `c:\xampp\htdocs` (the root folder for your XAMPP server, similar to the `public_html` folder on cPanel).
   - Create a folder named `joomla5` (or any name you prefer).
   - Copy the downloaded Joomla package into this folder and extract it.

---

### Create a Database in phpMyAdmin

1. Open **phpMyAdmin** by going to [http://localhost/phpMyAdmin](http://localhost/phpMyAdmin).
2. Click on the **User Accounts** tab.
3. At the bottom, click **Add user account**.
4. Enter a username (e.g., `joomla4`), which will also be your database name.
5. In the **Login Information** section, click on **Generate Password** and copy the generated password.
6. In the **Database for user account** section, check the box for **Create database with the same name and grant all privileges**.
7. Click **Go** to create the user and database.

You should now see the `joomla4` (or your chosen name) database listed in phpMyAdmin.

---

## Setting Up the Local Joomla Development Server Using XAMPP

---

### Install XAMPP

1. Install **XAMPP** to get Apache, MySQL, and PHP running on your local machine.
2. **Configure MySQL** and **PHP** to suit Joomla’s requirements.
3. Add the paths of **PHP** and **MySQL** to your environmental variables for easy access.

---

### Install Composer

1. **Composer** manages Joomla’s PHP dependencies. When installing Joomla, most dependencies are bundled in the release package.
2. Open **XAMPP Control Panel**, click on **Config** next to **Apache**, and select **PHP (php.ini)**.
3. In the `php.ini` file, uncomment the following extensions by removing the `;` before each:
   ```ini
   extension=gd
   extension=sodium
   extension=ldap
   extension=zip
   ```
4. After making changes, restart the Apache server.

---

### Steps to Set Up the Local Environment

1. **Clone the Joomla Repository**:
   Clone the official Joomla repository to your local machine.
   
2. **Checkout the Latest Release Branch**:
   Checkout the branch for the latest release (currently `4.4-dev`).

3. **Install Dependencies**:
   Run the following command from the root directory of the repository:
   ```bash
   composer install
   ```
   If you don’t have PHP-LDAP locally installed and it’s not needed for your project, you can add `--ignore-platform-reqs` to the command.

4. **Install JavaScript Dependencies**:
   Run the following command to install the necessary JavaScript dependencies:
   ```bash
   npm ci
   ```
   (Note: `npm` is the Node.js package manager, and `ci` stands for "clean install.")

---

This guide provides a quick overview of setting up a local Joomla development environment using XAMPP, Composer, and other essential tools. Once everything is set up, you can start building and managing Joomla-based projects locally!

---

