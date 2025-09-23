 ## 🐧 Linux Users & Groups
````markdown


In Linux, **users** and **groups** are the foundation of security and access control.  
They decide **who** can access files, run programs, or manage the system.

---
````
## 👤 Users in Linux

A **user** represents an account on the system.  
Every user has a **UID (User ID)** and certain **privileges**.

### 🔑 Types of Users

1. **Root User (Superuser)**  
   - **Username**: `root`  
   - **UID**: `0`  
   - **Role**: The most powerful account with full system control.  
   - **Powers**: Can edit/delete any file, install software, manage users.

2. **Normal Users**  
   - Created for everyday use.  
   - **UID**: Usually starts from `1000` onwards.  
   - **Role**: Can manage files inside their home folder.  
   - **Limitations**: Cannot change system files unless given permission.

3. **System Users**  
   - **UID**: Typically below `1000`.  
   - **Role**: Special accounts used by system services (e.g., `mysql`, `www-data`).  
   - **Login**: Usually no direct login, just for running background tasks.

---

## 👥 Groups in Linux

A **group** is a collection of users.  
Permissions can be assigned to groups, making it easier to manage shared access.

### 🔑 Types of Groups

1. **Primary Group**  
   - Each user has one primary group (created by default).  
   - Example: User `bob` will have group `bob`.

2. **Secondary Groups**  
   - A user can join multiple groups for extra permissions.  
   - Example: `bob` can also be part of `developers`.

3. **System Groups**  
   - Special groups for services (e.g., `mysql`, `www-data`).  
   - Used by daemons or system tasks.

---

## 🛠️ Managing Users & Groups

### ➕ Create a User
```bash
sudo adduser alice
````

Creates user **alice** and also a primary group with the same name.

### ➕ Create a Group

```bash
sudo groupadd developers
```

Makes a new group called **developers**.

### 👤 Add User to a Group

```bash
sudo usermod -aG developers alice
```

Adds **alice** to the **developers** group.

### 🔄 Change Primary Group

```bash
sudo usermod -g admin bob
```

Changes **bob’s** primary group to **admin**.
---
![alt text](IMAGES/LAB_3/3RD/1.png)![alt text](IMAGES/LAB_3/3RD/1b.png)
---

## 📋 Viewing Users & Groups

### List All Users

```bash
cat /etc/passwd
```

### List All Groups

```bash
cat /etc/group
```

### Check a User’s Details

```bash
id alice
```

Shows **UID**, **GID**, and all groups **alice** belongs to.
---
![alt text](IMAGES/LAB_3/3RD/2.png)![alt text](IMAGES/LAB_3/3RD/2b.png)![alt text](IMAGES/LAB_3/3RD/2c.png)![alt text](IMAGES/LAB_3/3RD/2d.png)![alt text](IMAGES/LAB_3/3RD/2e.png)
---


## 🔒 File Permissions & Groups

Each file/directory has **3 levels of permission**:

* **Owner (User)**
* **Group**
* **Others**

Example:

```
-rwxr-xr--
```

* `rwx` → owner can read/write/execute
* `r-x` → group can read/execute
* `r--` → others can only read

### Change File’s Group

```bash
sudo chown :developers file.txt
```

Now `file.txt` belongs to the **developers** group.
---
![alt text](IMAGES/LAB_3/3RD/3.png)
---

## ⭐ Special Groups

* **`sudo` (or `wheel`)** → lets users run commands as root.
* **`www-data`** → used by web servers.
* **`staff`** → common on macOS/Linux for shared access.

---

## ❌ Deleting Users & Groups

### Delete a User (with home directory)

```bash
sudo deluser --remove-home alice
```

### Delete a Group

```bash
sudo delgroup developers
```
---
![alt text](IMAGES/LAB_3/3RD/4.png)
---

