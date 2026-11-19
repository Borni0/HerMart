# HerMart
A women-focused e-commerce marketplace where women entrepreneurs sell handmade products and customers across Bangladesh can browse, order, and purchase online.

# HerMart — Local Installation Guide

HerMart is a web-based marketplace project built using PHP, MySQL, HTML, CSS, and JavaScript.

This guide explains how to clone the project from GitHub, configure the database, and run the website on a Windows PC using XAMPP.

## 1. Requirements

Before starting, make sure you have installed:

- [XAMPP](https://www.apachefriends.org/)
- [Git](https://git-scm.com/downloads)
- A web browser (Chrome, Firefox, Edge, etc.)

## 2. Clone the GitHub Repository

First, open Command Prompt, PowerShell, or Git Bash.

Navigate to the directory where you want to download the project.

Run the following command:

```bash
git clone https://github.com/Borni0/HerMart.git
```

After cloning, navigate to the project directory:

```bash
cd HerMart
```

The project files will now be available on your computer.

## 3. Copy the Project into XAMPP

1. Open the folder where you cloned the repository.
2. Locate the `DBMS` folder.
3. Copy the entire `DBMS` folder.
4. Open your XAMPP installation directory.
5. Navigate to:

```text
C:\xampp\htdocs\
```

6. Paste the `DBMS` folder inside `htdocs`.

Your directory structure should look like this:

```text
C:\xampp\htdocs\
│
└── DBMS\
    └── hMart\
        ├── index.php
        ├── assets\
        ├── includes\
        ├── customer\
        ├── seller\
        ├── admin\
        └── ...
```

**Important:** Make sure that `index.php` is directly inside the `hMart` folder.

## 4. Start XAMPP

1. Open the XAMPP Control Panel.
2. Start **Apache**.
3. Start **MySQL**.

Both services must be running to use the website and its database.

## 5. Create the MySQL Database

1. Open your browser.
2. Visit:

```text
http://localhost/phpmyadmin/
```

3. Click **New** from the left sidebar.
4. Enter the database name:

```text
hermert
```

5. Select `utf8mb4_general_ci` as the collation if available.
6. Click **Create**.

Your database is now ready.

## 6. Import the Database

The database must be imported before running the website.

1. Open the cloned HerMart project folder.
2. Locate the database `.sql` file included with the project.
3. Open phpMyAdmin:

```text
http://localhost/phpmyadmin/
```

4. Select the database named `hermert`.
5. Click the **Import** tab.
6. Click **Choose File**.
7. Select the HerMart `.sql` file from your project folder.
8. Scroll down and click **Import** or **Go**.

Wait until phpMyAdmin displays a successful import message.

**Note:** Import the provided project database SQL file, not a newly created empty database.

## 7. Configure the Database Connection

Open the following file:

```text
DBMS/hMart/includes/db.php
```

Check the database connection settings.

Make sure they match your local XAMPP configuration:

- Host: `localhost`
- Username: `root`
- Password: Leave empty if you are using the default XAMPP configuration.
- Database name: `hermert`

If necessary, update the database connection settings in `db.php` to match your configuration.

## 8. Run the HerMart Website

Make sure Apache and MySQL are running in XAMPP.

Open your browser and visit:

```text
http://localhost/DBMS/hMart/index.php
```

The HerMart homepage should now load.

You can navigate through the website and explore its available features.

## 9. Common Problems and Solutions

| Problem | Possible Solution |
|---|---|
| Apache does not start | Check whether another application is using port 80. |
| MySQL does not start | Check whether another MySQL service is using port 3306. |
| Database connection error | Check the database name, username, and password in `includes/db.php`. |
| 404 Not Found | Make sure the `DBMS/hMart` folder is inside `htdocs`. |
| XAMPP Dashboard appears instead of HerMart | Check that the correct HerMart `index.php` is inside the `hMart` folder. |
| Tables do not exist | Import the provided `.sql` database file into `hermert`. |
| CSS or images do not load | Check the asset paths and make sure the `assets` folder was copied correctly. |

## 10. Important Notes

- Apache and MySQL must be running whenever you use HerMart locally.
- The database must be created and imported before using the website.
- Do not rename important project folders unless you also update the relevant paths.
- Each team member must create and import their own local database.
- The project runs locally through XAMPP; it is not automatically hosted online.

## Project Repository

GitHub: https://github.com/Borni0/HerMart

## Local Website URL

```text
http://localhost/DBMS/hMart/index.php
```

---

**HerMart — A Web-Based Marketplace Project**
