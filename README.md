# 🧹 AutoDup_Cleaner (Automation System)

A Python-based **automation utility** that scans directories, detects duplicate files using **hashing (MD5)**, deletes redundant copies, generates detailed logs, and **emails reports automatically** at scheduled intervals.

This project is suitable for:

* System automation
* File management utilities
* Academic / final-year projects
* Resume & GitHub portfolio

---

## 📌 Key Features

* 🔍 **Duplicate Detection using MD5 Hashing**
* 🗂️ **Recursive Directory Scanning**
* 🗑️ **Automatic Duplicate File Deletion** (keeps one original copy)
* 📝 **Timestamped Log File Generation**
* 📧 **Email Notification with Log Attachment**
* ⏱️ **Task Scheduling (Runs Automatically at Fixed Intervals)**
* 💻 **Command-Line Interface (CLI)**

---

## 🛠️ Technologies Used

* **Language:** Python 3.x
* **Libraries & Modules:**

  * `hashlib` – checksum generation
  * `os` – file & directory operations
  * `time` – execution time & timestamps
  * `sys` – command-line arguments
  * `schedule` – job scheduling
  * `smtplib` – email service
  * `email.message` – email formatting

---

## 📂 Project Structure

```
Smart-Duplicate-File-Cleaner/
│
├── AutoDupCleaner.py           # Main application script
├── DuplicateLog_*.log          # Auto-generated log files
├── README.md                   # Project documentation
```

---

## ⚙️ How the Application Works

1. User provides a directory path as a command-line argument
2. Application scans all files recursively
3. MD5 checksum is calculated for every file
4. Files with identical checksums are marked as duplicates
5. One file is preserved, remaining duplicates are deleted
6. A detailed log file is generated
7. Log file is emailed automatically
8. Process repeats based on the scheduled interval

---

## ▶️ How to Run the Project

### 1️⃣ Install Required Package

```bash
pip install schedule
```

---

### 2️⃣ Run the Script

```bash
python AutoDupCleaner.py <DirectoryPath>
```

**Example:**

```bash
python AutoDupCleaner.py D:/TestFolder
```

---

### 3️⃣ Set Schedule Time

After execution, enter the schedule interval (in minutes):

```
Enter the schedule time in minutes to run the application: 10
```

➡️ The script will now run **every 10 minutes automatically**.

---

## 🧾 Command-Line Options

| Flag  | Description                 |
| ----- | --------------------------- |
| `--h` | Displays help information   |
| `--u` | Displays usage instructions |

---

## 📧 Email Configuration

The script sends log reports via **Gmail SMTP**.

### 🔐 Requirements

* Gmail account
* App Password enabled (Google Security Settings)

### ⚠️ Security Note

For production use, **do NOT hardcode credentials**. Use environment variables instead.

---

## 📝 Sample Log File Content

```
------------------------------------------------------------
This is a log file created by duplicate file remover.
This log file contains the list of duplicate files deleted.
------------------------------------------------------------
Deleted File : D:/TestFolder/sample1_copy.txt
Deleted File : D:/TestFolder/sample2_copy.txt
Total Deleted File : 2
------------------------------------------------------------
Total time taken by Application : 0.42 sec
------------------------------------------------------------
```

---

## 📈 Performance

* Uses **buffered reading (1024 bytes)** for efficiency
* Works well with large directories
* Time complexity depends on number of files

---

## 🚀 Future Enhancements

* ✅ SHA-256 hashing for better integrity
* ✅ Dry-run mode (no deletion)
* ✅ GUI using Tkinter
* ✅ Database-based logging
* ✅ Cloud storage support
* ✅ Linux Cron Job integration

---

## 👨‍💻 Author

**Shubham Dalvi**
B.Sc. Computer Science
Aspiring Python Automation & Machine Learning 

---

## ⭐ Acknowledgement

This project is inspired by real-world system maintenance and automation requirements and developed for learning, academic, and practical use.

---

## 📜 License

This project is open-source and free to use for educational purposes.

---

### 🌟 If you like this project, don't forget to **star ⭐ the repository** on GitHub!
