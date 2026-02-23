# Task 1: For Loop
Create for_loop.sh that:
Loops through a list of 5 fruits and prints each one
<img width="1175" height="755" alt="Screenshot 2026-02-17 021607" src="https://github.com/user-attachments/assets/6fac9b50-f710-4c1e-bf1c-04babaad0507" />
<img width="1178" height="625" alt="Screenshot 2026-02-17 021634" src="https://github.com/user-attachments/assets/5fc4fa36-75ad-4522-aebf-1354d0da93f1" />


Create count.sh that:
Prints numbers 1 to 10 using a for loop
<img width="769" height="751" alt="Screenshot 2026-02-17 022431" src="https://github.com/user-attachments/assets/98f92eda-29dc-4b6d-9a70-cf5be9e94811" />
<img width="666" height="573" alt="Screenshot 2026-02-17 022441" src="https://github.com/user-attachments/assets/34f4b2af-463a-48c4-8fc7-81a65d47c9c7" />

# Task 2: While Loop
Create countdown.sh that:
Takes a number from the user
Counts down to 0 using a while loop
Prints "Done!" at the end

<img width="1091" height="744" alt="Screenshot 2026-02-17 024801" src="https://github.com/user-attachments/assets/4990c40b-c2b6-4a3d-be5b-6bb05faad71f" />
<img width="1051" height="695" alt="Screenshot 2026-02-17 024823" src="https://github.com/user-attachments/assets/88b19c14-4eea-454e-8fd2-7b841cae2167" />

# Task 3: Command-Line Arguments
Create greet.sh that:

Accepts a name as $1
Prints Hello, <name>!
If no argument is passed, prints "Usage: ./greet.sh "
<img width="653" height="514" alt="Screenshot 2026-02-17 030009" src="https://github.com/user-attachments/assets/9fbc77ec-968c-4572-9416-f1bb002ee1d5" />
<img width="1635" height="895" alt="Screenshot 2026-02-17 030030" src="https://github.com/user-attachments/assets/9e676b2a-febb-4140-bac1-2f5afb6e8e98" />

Create args_demo.sh that:

- Prints total number of arguments
- Prints all arguments 
- Prints the script name 
<img width="881" height="457" alt="Screenshot 2026-02-17 030619" src="https://github.com/user-attachments/assets/60354898-e516-4b68-9b46-f02b73237f47" />
<img width="731" height="552" alt="Screenshot 2026-02-17 030603" src="https://github.com/user-attachments/assets/b384f11c-f776-40bc-aa67-d0bbf8e1addb" />

Install Packages via Script
- Create install_packages.sh that:
- Defines a list of packages: nginx, curl, wget
- Loops through the list
- Checks if each package is installed (use dpkg -s or rpm -q)
- Installs it if missing, skips if already present
- Prints status for each package
  <img width="1012" height="487" alt="Screenshot 2026-02-23 130337" src="https://github.com/user-attachments/assets/c7b9515a-91a5-46a4-b729-22edae5477a4" />
  <img width="1898" height="958" alt="Screenshot 2026-02-23 130355" src="https://github.com/user-attachments/assets/083d6d49-5c8c-458b-bd9d-4c893ca8f252" />
  <img width="1798" height="221" alt="Screenshot 2026-02-23 130409" src="https://github.com/user-attachments/assets/7508957e-1e11-4383-9194-c45474a93a7f" />

Error Handling
- Create safe_script.sh that:
- Uses set -e at the top (exit on error)
- Tries to create a directory /tmp/devops-test
- Tries to navigate into it
- Creates a file inside
- Uses || operator to print an error if any step fails
<img width="1326" height="518" alt="Screenshot 2026-02-23 132355" src="https://github.com/user-attachments/assets/4bd3aa73-f167-45ab-8702-c862b12ffdca" />
<img width="1281" height="377" alt="Screenshot 2026-02-23 132415" src="https://github.com/user-attachments/assets/0f460339-b32f-4473-8765-99c47178e1be" />


Modify your install_packages.sh to check if the script is being run as root — exit with a message if not.










