# Task 1: Your First Script
- Create a file hello.sh
- Add the shebang line #!/bin/bash at the top
- Print Hello, DevOps! using echo
- Make it executable and run it
<img width="1464" height="744" alt="Screenshot 2026-02-17 010644" src="https://github.com/user-attachments/assets/a66080b4-9838-434b-bc5b-dba4216cd093" />
 <img width="614" height="76" alt="Screenshot 2026-02-17 010715" src="https://github.com/user-attachments/assets/4271acd5-1f6e-4ece-a51f-08de60af0379" />
 <img width="1045" height="740" alt="Screenshot 2026-02-17 010808" src="https://github.com/user-attachments/assets/ae76c2a1-0269-4336-82bd-9909f8d54acc" />

# What happens if you remove the shebang line?
nothing the script will be interpreted in the default shell like we have bash,sh,ksh,fish,etc... so when we used the shebang it clearly says that in which 
environment the script should be executed 

# Variables
Create variables.sh with:
- A variable for your NAME
- A variable for your ROLE (e.g., "DevOps Engineer")
- Print: Hello, I am <NAME> and I am a <ROLE>

<img width="813" height="729" alt="Screenshot 2026-02-17 011259" src="https://github.com/user-attachments/assets/d2a6218a-3ffd-458d-8a66-8fcf610750ad" />
<img width="897" height="686" alt="Screenshot 2026-02-17 011331" src="https://github.com/user-attachments/assets/3f90e9ed-b7c1-4afb-95e5-e3de2f7e1f85" />
<img width="1233" height="737" alt="Screenshot 2026-02-17 011447" src="https://github.com/user-attachments/assets/f175c6cb-8b61-4af4-adf4-bb3e9f09fa4e" />
<img width="1243" height="751" alt="Screenshot 2026-02-17 011748" src="https://github.com/user-attachments/assets/a956ffa2-605f-41a5-8ddc-9a524efdb59c" />
Try using single quotes vs double quotes — what's the difference?
no worries 

# Task 3: User Input with read
- Create greet.sh that:
- Asks the user for their name using read
- Asks for their favourite tool
<img width="913" height="748" alt="Screenshot 2026-02-17 012503" src="https://github.com/user-attachments/assets/12213721-1faf-4dfd-901b-5ac4039d6ac3" />
<img width="1334" height="327" alt="Screenshot 2026-02-17 012535" src="https://github.com/user-attachments/assets/30958c0b-5631-4238-a6fc-e3a3b265ebd5" />

# Task 4: If-Else Conditions
Create check_number.sh that:
Takes a number using read
Prints whether it is positive, negative, or zero
<img width="913" height="748" alt="Screenshot 2026-02-17 012503" src="https://github.com/user-attachments/assets/b0c37312-5a80-4688-83f9-5f3cdaa4037b" />
<img width="1334" height="327" alt="Screenshot 2026-02-17 012535" src="https://github.com/user-attachments/assets/8e9ca504-e1cd-434c-a761-06a77c0ff843" />

# Create file_check.sh that:
Asks for a filename
Checks if the file exists using -f
Prints appropriate message
<img width="1240" height="456" alt="Screenshot 2026-02-17 013602" src="https://github.com/user-attachments/assets/2deea24d-e511-41fc-8818-2a76d9679e04" />
<img width="1236" height="753" alt="Screenshot 2026-02-17 020419" src="https://github.com/user-attachments/assets/b2c984fa-d836-4751-91c1-be2d10c6602f" />

# ask 5: Combine It All
Create server_check.sh that:

Stores a service name in a variable (e.g., nginx, sshd)
Asks the user: "Do you want to check the status? (y/n)"
If y — runs systemctl status <service> and prints whether it's active or not
If n — prints "Skipped."

<img width="1051" height="749" alt="Screenshot 2026-02-17 014600" src="https://github.com/user-attachments/assets/bda8af17-ed45-4529-ba03-0c23d52afe88" />
<img width="1656" height="975" alt="Screenshot 2026-02-17 014622" src="https://github.com/user-attachments/assets/bd2cdbfb-0584-41bc-a832-58939bb89332" />
<img width="1919" height="759" alt="Screenshot 2026-02-17 014641" src="https://github.com/user-attachments/assets/7aa1b1aa-b885-40cc-a629-d837584f499b" />




















