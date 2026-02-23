# Basic Functions
- Create functions.sh with:
- A function greet that takes a name as argument and prints Hello, <name>!
- A function add that takes two numbers and prints their sum
- Call both functions from the script
<img width="904" height="627" alt="Screenshot 2026-02-23 135632" src="https://github.com/user-attachments/assets/73cd6dc5-def2-4586-9aba-b896ac5f3985" />
<img width="918" height="322" alt="Screenshot 2026-02-23 135644" src="https://github.com/user-attachments/assets/3342cb68-6260-4b90-aba7-86dfcea79d20" />

# Functions with Return Values
- Create disk_check.sh with:
- A function check_disk that checks disk usage of / using df -h
- A function check_memory that checks free memory using free -h
- A main section that calls both and prints the results
<img width="1125" height="745" alt="Screenshot 2026-02-23 141625" src="https://github.com/user-attachments/assets/409aeb63-ffc0-42c4-9050-f7af2f4ced77" />
<img width="1333" height="411" alt="Screenshot 2026-02-23 141611" src="https://github.com/user-attachments/assets/6c8f8c50-edf9-4a15-8a0b-c97e33737518" />

# Strict Mode — set -euo pipefail
- Create strict_demo.sh with set -euo pipefail at the top
- Try using an undefined variable — what happens with set -u?
- Try a command that fails — what happens with set -e?
- Try a piped command where one part fails — what happens with set -o pipefail?
- Document: What does each flag do?
- set -e → cat: abc.txt: No such file or directory
- set -u → ubound variable
- set -o pipefail → cat: abc.txt: No such file or directory
Pipeline done

<img width="1336" height="678" alt="Screenshot 2026-02-23 143709" src="https://github.com/user-attachments/assets/c79dc14a-a7ce-4f8b-bf1f-9d353ad6ba69" />
<img width="1204" height="667" alt="Screenshot 2026-02-23 143651" src="https://github.com/user-attachments/assets/abf1f8fd-345a-41f0-8562-9a9c6d5039e2" />

# Local Variables
- Create local_demo.sh with:
- A function that uses local keyword for variables
- Show that local variables don't leak outside the function
- Compare with a function that uses regular variables


# Build a Script — System Info Reporter
- Create system_info.sh that uses functions for everything:
- A function to print hostname and OS info
- A function to print uptime
- A function to print disk usage (top 5 by size)
- A function to print memory usage
- A function to print top 5 CPU-consuming processes
- A main function that calls all of the above with section headers
- Use set -euo pipefail at the top





