# Basics
- Document the following with short descriptions and examples:
- Shebang (#!/bin/bash) — what it does and why it matters
- Tells the system which interpreter to use to run the script.
Ensures your script runs with Bash, even if the default shell is different.
- Running a script — chmod +x, ./script.sh, bash script.sh
- <img width="394" height="53" alt="Screenshot 2026-02-25 195352" src="https://github.com/user-attachments/assets/bda2ee39-4154-4669-9584-6659f6b66ce6" />
- Comments — single line (#) and inline
- <img width="515" height="51" alt="Screenshot 2026-02-25 195433" src="https://github.com/user-attachments/assets/b9099349-aad5-4fd3-b748-8d1af5809fca" />
- Variables — declaring, using, and quoting ($VAR, "$VAR", '$VAR')
- <img width="462" height="82" alt="Screenshot 2026-02-25 195521" src="https://github.com/user-attachments/assets/e1e9073c-a235-41a3-a91d-f95dca16dbe2" />
- Reading user input — read
- <img width="337" height="73" alt="Screenshot 2026-02-25 195606" src="https://github.com/user-attachments/assets/c8aad318-dd55-478a-8b63-6277859a69d7" />
- Command-line arguments — $0, $1, $#, $@, $?
- <img width="467" height="181" alt="Screenshot 2026-02-25 195636" src="https://github.com/user-attachments/assets/2b29896f-18ea-4260-9076-a2f89c8cbc48" />


# Operators and Conditionals
- Document with examples:
- String comparisons — =, !=, -z, -n
- | Operator | Description         |
| -------- | ------------------- |
| `=`      | Equal               |
| `!=`     | Not equal           |
| `-z`     | String is empty     |
| `-n`     | String is not empty |

- Integer comparisons — -eq, -ne, -lt, -gt, -le, -ge
- | Operator | Description           |
| -------- | --------------------- |
| `-eq`    | Equal                 |
| `-ne`    | Not equal             |
| `-lt`    | Less than             |
| `-gt`    | Greater than          |
| `-le`    | Less than or equal    |
| `-ge`    | Greater than or equal |

- File test operators — -f, -d, -e, -r, -w, -x, -s
- | Operator | Description                       |
| -------- | --------------------------------- |
| `-f`     | File exists and is a regular file |
| `-d`     | Directory exists                  |
| `-e`     | File or directory exists          |
| `-r`     | File is readable                  |
| `-w`     | File is writable                  |
| `-x`     | File is executable                |
| `-s`     | File exists and is not empty      |

- if, elif, else syntax
- <img width="415" height="233" alt="Screenshot 2026-02-25 200038" src="https://github.com/user-attachments/assets/90679420-6bab-481d-ace2-a2f18e5438ad" />
- Logical operators — &&, ||, !
- <img width="650" height="337" alt="Screenshot 2026-02-25 200144" src="https://github.com/user-attachments/assets/07bc8a70-26ed-4020-a357-384dbd5d019c" />
- Case statements — case ... esac
- <img width="609" height="315" alt="Screenshot 2026-02-25 200218" src="https://github.com/user-attachments/assets/5601668b-e7d5-4ef9-8bcd-440a0c5d988e" />

# Loops
- Document with examples:
- for loop — list-based and C-style
- <img width="378" height="114" alt="Screenshot 2026-02-25 200417" src="https://github.com/user-attachments/assets/f257c3b4-98c3-41c4-803d-450464cfb0f6" />
- <img width="356" height="114" alt="Screenshot 2026-02-25 200428" src="https://github.com/user-attachments/assets/b810032a-4762-45a9-b50a-a52b49cae613" />
- while loop
- <img width="498" height="169" alt="Screenshot 2026-02-25 200532" src="https://github.com/user-attachments/assets/1bfab2ba-d1aa-4651-b1b3-9b6a5c2d7c16" />
- until loop
- <img width="554" height="176" alt="Screenshot 2026-02-25 200542" src="https://github.com/user-attachments/assets/ade1340f-8032-42cc-b0be-b9cacf63e613" />
- Loop control — break, continue
- <img width="518" height="277" alt="Screenshot 2026-02-25 200632" src="https://github.com/user-attachments/assets/ebeea2e1-4c79-4bab-a4a1-bfe43878d867" />
- Looping over files — for file in *.log
- <img width="471" height="117" alt="Screenshot 2026-02-25 200711" src="https://github.com/user-attachments/assets/fd06ac3a-4189-4ca9-8506-4a3bf8b96eff" />
- Looping over command output — while read line
- <img width="448" height="115" alt="image" src="https://github.com/user-attachments/assets/4077adf5-2899-407b-bb1f-6f481ff54836" />

# Functions
Document with examples:
- Defining a function — function_name() { ... }
- <img width="440" height="104" alt="Screenshot 2026-02-25 200845" src="https://github.com/user-attachments/assets/06149b9e-1f59-43c9-b46f-2cdd0cc4de2e" />
- Calling a function
- <img width="465" height="159" alt="Screenshot 2026-02-25 200924" src="https://github.com/user-attachments/assets/8ffee43a-c9fd-40d6-aa7e-532533ae7e19" />
- Passing arguments to functions — $1, $2 inside functions
- <img width="524" height="155" alt="Screenshot 2026-02-25 200947" src="https://github.com/user-attachments/assets/e988db61-ca90-41d0-bced-e4b2e2205631" />
- Return values — return vs echo
- <img width="566" height="278" alt="Screenshot 2026-02-25 201027" src="https://github.com/user-attachments/assets/aa9e1c03-303e-4137-8eda-0f4a57626f3e" />
- <img width="380" height="146" alt="Screenshot 2026-02-25 201055" src="https://github.com/user-attachments/assets/d954bfb2-525f-408c-9757-dee7689d932e" />
- Local variables — local
- <img width="562" height="240" alt="Screenshot 2026-02-25 201120" src="https://github.com/user-attachments/assets/b542134c-6e6f-4d6a-af07-cd9c6bf84a29" />

# Text Processing Commands
Document the most useful flags/patterns for each:
- grep — search patterns, -i, -r, -c, -n, -v, -E
- | Flag | Description                       |
| ---- | --------------------------------- |
| `-i` | Case-insensitive search           |
| `-r` | Recursive search in directories   |
| `-c` | Count matching lines              |
| `-n` | Show line numbers                 |
| `-v` | Invert match (lines not matching) |
| `-E` | Extended regex patterns           |
<img width="657" height="135" alt="Screenshot 2026-02-25 201323" src="https://github.com/user-attachments/assets/ff7b8751-5483-423a-80e4-4a3c6b174bfb" />

- awk — print columns, field separator, patterns, BEGIN/END
- <img width="568" height="100" alt="Screenshot 2026-02-25 201351" src="https://github.com/user-attachments/assets/6a54295a-6a16-4792-a9bb-f36f1f4b04b7" />

- sed — substitution, delete lines, in-place edit
- | Action        | Example                           |
| ------------- | --------------------------------- |
| Substitute    | `sed 's/old/new/' file`           |
| Delete lines  | `sed '2d' file` (delete 2nd line) |
| In-place edit | `sed -i 's/foo/bar/g' file`       |

<img width="720" height="74" alt="Screenshot 2026-02-25 201424" src="https://github.com/user-attachments/assets/fe235d79-a708-438d-957e-669d59b239c7" />
- cut — extract columns by delimiter
- <img width="604" height="56" alt="Screenshot 2026-02-25 201504" src="https://github.com/user-attachments/assets/da6d066c-d011-4501-9359-ed4cc77b9877" />

- sort — alphabetical, numerical, reverse, unique
- | Option | Description   |
| ------ | ------------- |
| `-n`   | Numeric sort  |
| `-r`   | Reverse order |
| `-u`   | Unique lines  |
<img width="526" height="77" alt="Screenshot 2026-02-25 201539" src="https://github.com/user-attachments/assets/b67b80ce-b6fb-49d3-b922-53ecf0414ab6" />

- uniq — deduplicate, count
- <img width="592" height="80" alt="Screenshot 2026-02-25 201600" src="https://github.com/user-attachments/assets/5ccffe0c-337f-42e6-ad8d-64f3ef20d9f6" />

- tr — translate/delete characters
- <img width="600" height="58" alt="Screenshot 2026-02-25 201629" src="https://github.com/user-attachments/assets/6dcc1552-5af1-4b18-bce3-871294d6caa6" />

- wc — line/word/char count
- <img width="587" height="91" alt="Screenshot 2026-02-25 201656" src="https://github.com/user-attachments/assets/84f74a62-5a81-4e8f-934e-78138bbc763a" />

- head / tail — first/last N lines, follow mode
- <img width="631" height="83" alt="Screenshot 2026-02-25 201726" src="https://github.com/user-attachments/assets/6c23dbb6-ddde-4905-a971-9ece1af9f0fa" />

# Useful Patterns and One-Liners
Include at least 5 real-world one-liners you find useful. Examples:
- Find and delete files older than N days
- <img width="678" height="40" alt="Screenshot 2026-02-25 201955" src="https://github.com/user-attachments/assets/946c81ec-23b8-41fc-b7f5-9a61d323a97d" />
- Count lines in all .log files
- <img width="453" height="34" alt="image" src="https://github.com/user-attachments/assets/a91a899e-81fc-4002-a6da-b3e8fbdb8695" />
- Replace a string across multiple files
- <img width="435" height="33" alt="Screenshot 2026-02-25 202108" src="https://github.com/user-attachments/assets/39b84a53-2a8e-4abb-b545-554126ebd767" />
- Check if a service is running
- <img width="717" height="41" alt="Screenshot 2026-02-25 202134" src="https://github.com/user-attachments/assets/baa5e009-234a-4f68-ab83-f1a2952e6833" />
- Monitor disk usage with alerts
- <img width="715" height="37" alt="Screenshot 2026-02-25 202200" src="https://github.com/user-attachments/assets/6194bad1-74f8-4459-aa44-095cea7c9d78" />
- Parse CSV or JSON from command line
- <img width="346" height="39" alt="Screenshot 2026-02-25 202225" src="https://github.com/user-attachments/assets/61c7f229-2dc2-45d7-84d0-bdff855693dc" />
- Tail a log and filter for errors in real time
- <img width="586" height="34" alt="Screenshot 2026-02-25 202243" src="https://github.com/user-attachments/assets/4f780d9e-5f8c-4b22-83c5-9607114c06bc" />

# Error Handling and Debugging
Document with examples:
- Exit codes — $?, exit 0, exit 1
- <img width="489" height="194" alt="Screenshot 2026-02-25 202610" src="https://github.com/user-attachments/assets/ff5610a2-5fd3-420b-95f5-24546f7972b7" />
- <img width="532" height="98" alt="Screenshot 2026-02-25 202617" src="https://github.com/user-attachments/assets/b28e52bd-f351-4301-8c1d-740784c354ce" />
- set -e — exit on error
- <img width="493" height="139" alt="Screenshot 2026-02-25 202700" src="https://github.com/user-attachments/assets/7ca6b3f4-a165-4607-bad6-9ba338b4915f" />
- set -u — treat unset variables as error
- <img width="424" height="97" alt="Screenshot 2026-02-25 202725" src="https://github.com/user-attachments/assets/2931c971-0641-48a5-9fbe-fbd29bbbf5af" />
- <img width="490" height="42" alt="Screenshot 2026-02-25 202732" src="https://github.com/user-attachments/assets/d1013fc9-353e-438a-a486-ea7c729fed90" />
- set -o pipefail — catch errors in pipes
- <img width="502" height="140" alt="Screenshot 2026-02-25 202828" src="https://github.com/user-attachments/assets/c714db91-c9d8-4e48-9a15-fa52f9071ac6" />
- <img width="501" height="56" alt="Screenshot 2026-02-25 202835" src="https://github.com/user-attachments/assets/68609a35-bf9b-4fce-b66e-0ad51d6d3aca" />
- set -x — debug mode (trace execution)
- <img width="481" height="130" alt="Screenshot 2026-02-25 202911" src="https://github.com/user-attachments/assets/4cc28452-ba8b-4b50-99f1-d8b142a79b8e" />
- <img width="481" height="120" alt="Screenshot 2026-02-25 202920" src="https://github.com/user-attachments/assets/eb71957c-e43b-42a4-a8b3-310645d74597" />
- Trap — trap 'cleanup' EXIT
- <img width="677" height="274" alt="Screenshot 2026-02-25 202952" src="https://github.com/user-attachments/assets/4ae8ab41-8fce-4f2c-9a16-f839d0b1f208" />
- <img width="470" height="75" alt="Screenshot 2026-02-25 203002" src="https://github.com/user-attachments/assets/fbc2939c-53b4-4197-9531-bc123655d366" />

# Bonus — Quick Reference Table
| **Topic**   | **Key Syntax**             | **Example**                        |                 |
| ----------- | -------------------------- | ---------------------------------- | --------------- |
| Variable    | `VAR="value"`              | `NAME="DevOps"`                    |                 |
| Argument    | `$1, $2`                   | `./script.sh arg1 arg2`            |                 |
| If          | `if [ condition ]; then`   | `if [ -f file ]; then`             |                 |
| For loop    | `for i in list; do`        | `for i in 1 2 3; do`               |                 |
| While loop  | `while [ condition ]; do`  | `while [ $COUNT -le 5 ]; do`       |                 |
| Until loop  | `until [ condition ]; do`  | `until [ $COUNT -gt 5 ]; do`       |                 |
| Function    | `name() { ... }`           | `greet() { echo "Hi"; }`           |                 |
| Grep        | `grep pattern file`        | `grep -i "error" log.txt`          |                 |
| Awk         | `awk '{print $1}' file`    | `awk -F: '{print $1}' /etc/passwd` |                 |
| Sed         | `sed 's/old/new/g' file`   | `sed -i 's/foo/bar/g' config.txt`  |                 |
| Cut         | `cut -d',' -f1 file`       | `cut -d':' -f1 /etc/passwd`        |                 |
| Sort        | `sort [options] file`      | `sort -nr numbers.txt`             |                 |
| Uniq        | `uniq -c file`             | `sort file.txt                     | uniq -c`        |
| Tr          | `tr 'a-z' 'A-Z'`           | `echo "hello"                      | tr 'a-z' 'A-Z'` |
| Wc          | `wc -l/-w/-c file`         | `wc -l sample.log`                 |                 |
| Head / Tail | `head -n N file`           | `tail -f /var/log/syslog`          |                 |
| Exit codes  | `$?, exit 0, exit 1`       | `echo $?; exit 1`                  |                 |
| Debug / Set | `set -e -u -x -o pipefail` | `set -euxo pipefail`               |                 |
| Trap        | `trap 'function' EXIT`     | `trap cleanup EXIT`                |                 |









