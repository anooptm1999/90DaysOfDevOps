# Log Rotation Script
- Create log_rotate.sh that:
- Takes a log directory as an argument (e.g., /var/log/myapp)
- Compresses .log files older than 7 days using gzip
- Deletes .gz files older than 30 days
- Prints how many files were compressed and deleted
- Exits with an error if the directory doesn't exist
<img width="1614" height="839" alt="Screenshot 2026-02-24 131228" src="https://github.com/user-attachments/assets/b3ca04c0-73a2-4874-a75e-c6415c1d9690" />
<img width="1102" height="600" alt="Screenshot 2026-02-24 131255" src="https://github.com/user-attachments/assets/af1de1d7-a138-4073-b7d9-9ed03025fd99" />


# Server Backup Script
- Create backup.sh that:
- Takes a source directory and backup destination as arguments
- Creates a timestamped .tar.gz archive (e.g., backup-2026-02-08.tar.gz)
- Verifies the archive was created successfully
- Prints archive name and size
- Deletes backups older than 14 days from the destination
- Handles errors — exit if source doesn't exist

<img width="756" height="638" alt="Screenshot 2026-02-25 191149" src="https://github.com/user-attachments/assets/bc7e3dee-7a07-41dd-9a37-0d6077576b1b" />
<img width="753" height="380" alt="Screenshot 2026-02-25 191206" src="https://github.com/user-attachments/assets/219b9fe5-7ccc-4d7e-87f1-005423388433" />
<img width="745" height="183" alt="Screenshot 2026-02-25 191252" src="https://github.com/user-attachments/assets/d23401ad-5f03-4525-9a0a-81fdc5f06474" />
<img width="740" height="66" alt="Screenshot 2026-02-25 191304" src="https://github.com/user-attachments/assets/65c38bd2-037f-430c-b292-55be16acfbf2" />


# Crontab
- Read: crontab -l — what's currently scheduled?
- Understand cron syntax:
* * * * *  command
│ │ │ │ │
│ │ │ │ └── Day of week (0-7)
│ │ │ └──── Month (1-12)
│ │ └────── Day of month (1-31)
│ └──────── Hour (0-23)
└────────── Minute (0-59)
- Write cron entries (in your markdown, don't apply if unsure) for:
- Run log_rotate.sh every day at 2 AM
- Run backup.sh every Sunday at 3 AM
- Run a health check script every 5 minutes

<img width="642" height="53" alt="Screenshot 2026-02-25 191610" src="https://github.com/user-attachments/assets/67e8346e-36ea-48e6-93e3-09e751d2f529" />
<img width="379" height="37" alt="Screenshot 2026-02-25 191620" src="https://github.com/user-attachments/assets/a1a88388-3b1a-4037-8a10-a5621dcdc812" />
<img width="753" height="523" alt="Screenshot 2026-02-25 191642" src="https://github.com/user-attachments/assets/ab9d5da5-db41-4177-a975-8957a0d1c9df" />
<img width="676" height="94" alt="Screenshot 2026-02-25 191658" src="https://github.com/user-attachments/assets/5d84addf-50d7-4fa5-bfd7-7657c15e2b2a" />

# Combine — Scheduled Maintenance Script
- Create maintenance.sh that:
- Calls your log rotation function
- Calls your backup function
- Logs all output to /var/log/maintenance.log with timestamps
- Write the cron entry to run it daily at 1 AM

<img width="748" height="416" alt="Screenshot 2026-02-25 192004" src="https://github.com/user-attachments/assets/eb7f4d61-5a73-4647-8fc8-6a7b304c8dad" />
<img width="634" height="84" alt="Screenshot 2026-02-25 192015" src="https://github.com/user-attachments/assets/b4d487e4-74e4-476a-b38e-e3620d72c2e3" />
<img width="620" height="262" alt="Screenshot 2026-02-25 192025" src="https://github.com/user-attachments/assets/ed796954-f791-4a58-aaa6-3b9413081e17" />
- <img width="366" height="34" alt="Screenshot 2026-02-25 192034" src="https://github.com/user-attachments/assets/12bc12af-39fd-4c58-b2b6-1e696a085b94" />
- <img width="443" height="58" alt="Screenshot 2026-02-25 192048" src="https://github.com/user-attachments/assets/d6200837-4ac9-4e66-9d4e-9cf7408d1976" />
- <img width="462" height="59" alt="Screenshot 2026-02-25 192057" src="https://github.com/user-attachments/assets/1d1bc23e-03cb-4993-ab7f-9d24362c5fa7" />







