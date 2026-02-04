# Understanding Ownership
- Run ls -l in your home directory
- Identify the owner and group columns
- Check who owns your files
  <img width="585" height="47" alt="Screenshot 2026-02-05 003106" src="https://github.com/user-attachments/assets/6d85bd8c-1bc7-45ac-956c-8652326517d1" />

# Basic chown Operations
- Create file devops-file.txt
- Check current owner: ls -l devops-file.txt
- Change owner to tokyo (create user if needed)
- Change owner to berlin
- Verify the changes
  <img width="747" height="193" alt="Screenshot 2026-02-05 003145" src="https://github.com/user-attachments/assets/3685b6be-2e40-4dc8-bcbd-d629e9a61fe3" />

# Basic chgrp Operations
- Create file team-notes.txt
- Check current group: ls -l team-notes.txt
- Create group: sudo groupadd heist-team
- Change file group to heist-team
- Verify the change
  <img width="951" height="258" alt="Screenshot 2026-02-05 003302" src="https://github.com/user-attachments/assets/27f5678e-755b-4b34-b4c7-8fae2b5bdde4" />

# Recursive Ownership 
- Create directory structure:

- mkdir -p heist-project/vault
- mkdir -p heist-project/plans
- touch heist-project/vault/gold.txt
- touch heist-project/plans/strategy.conf
- Create group planners: sudo groupadd planners

- Change ownership of entire heist-project/ directory:

- Owner: professor
- Group: planners
- Verify all files and subdirectories changed
  <img width="935" height="280" alt="Screenshot 2026-02-05 003646" src="https://github.com/user-attachments/assets/ddb9ef32-cc06-4578-90ff-ac396105f604" />

# Practice Challenge
- Create users: tokyo, berlin, nairobi (if not already created)

- Create groups: vault-team, tech-team

- Create directory: bank-heist/

- Create 3 files inside:

- touch bank-heist/access-codes.txt
- touch bank-heist/blueprints.pdf
- touch bank-heist/escape-plan.txt
- Set different ownership:

- access-codes.txt → owner: tokyo, group: vault-team
- blueprints.pdf → owner: berlin, group: tech-team
- escape-plan.txt → owner: nairobi, group: vault-team
- Verify: ls -l bank-heist/
<img width="1124" height="628" alt="Screenshot 2026-02-05 003946" src="https://github.com/user-attachments/assets/5bd08c86-5a33-415e-9873-fd8b287c5edd" />




