# Input and Validation
- Your script should:
- Accept the path to a log file as a command-line argument
- Exit with a clear error message if no argument is provided
- Exit with a clear error message if the file doesn't exist
<img width="757" height="383" alt="Screenshot 2026-02-25 193033" src="https://github.com/user-attachments/assets/2405855f-63de-4021-be07-cef1f0d8da82" />
<img width="577" height="77" alt="Screenshot 2026-02-25 193055" src="https://github.com/user-attachments/assets/ab11d9fb-b1e8-419b-b838-28bd4cd1585a" />
<img width="482" height="75" alt="Screenshot 2026-02-25 193112" src="https://github.com/user-attachments/assets/109bd387-c428-43d8-8116-2577a5765d8d" />
<img width="570" height="57" alt="Screenshot 2026-02-25 193120" src="https://github.com/user-attachments/assets/f8590d60-9a7d-47a2-95e6-0b35cee91dac" />
<img width="597" height="79" alt="Screenshot 2026-02-25 193125" src="https://github.com/user-attachments/assets/310c06af-6fc5-4ba3-815f-a9646b176bdc" />

# Error Count
- Count the total number of lines containing the keyword ERROR or Failed
- Print the total error count to the console
<img width="715" height="417" alt="Screenshot 2026-02-25 193323" src="https://github.com/user-attachments/assets/e8f36ef3-88dc-46a8-b770-7f6d63569d5a" />
<img width="549" height="73" alt="Screenshot 2026-02-25 193334" src="https://github.com/user-attachments/assets/d4baf76f-89a3-41d0-b2c4-863fab2e76af" />
<img width="618" height="56" alt="Screenshot 2026-02-25 193343" src="https://github.com/user-attachments/assets/0b8fb638-02f0-4811-bbed-f1684044ba6b" />
<img width="564" height="162" alt="Screenshot 2026-02-25 193353" src="https://github.com/user-attachments/assets/f888ca26-2f63-432f-a7a4-ad29d711355c" />
<img width="538" height="59" alt="Screenshot 2026-02-25 193401" src="https://github.com/user-attachments/assets/edbe43d3-61dd-4456-9571-7f60d1823472" />

# Critical Events
- Search for lines containing the keyword CRITICAL
- Print those lines along with their line number
Example output:

--- Critical Events ---
Line 84: 2025-07-29 10:15:23 CRITICAL Disk space below threshold
Line 217: 2025-07-29 14:32:01 CRITICAL Database connection lost

<img width="735" height="409" alt="Screenshot 2026-02-25 193635" src="https://github.com/user-attachments/assets/0761dcb7-df71-45ca-ac59-3fd5bd87a678" />
<img width="616" height="88" alt="Screenshot 2026-02-25 193645" src="https://github.com/user-attachments/assets/2911d3e7-9f58-48a2-91c5-53ccc50a4c95" />
<img width="488" height="73" alt="Screenshot 2026-02-25 193656" src="https://github.com/user-attachments/assets/a5e16047-0e36-4416-9a22-a160cbf1f125" />
<img width="629" height="68" alt="Screenshot 2026-02-25 193704" src="https://github.com/user-attachments/assets/c10a9cda-26b2-43ff-810b-ecc28f413a90" />
<img width="667" height="162" alt="Screenshot 2026-02-25 193715" src="https://github.com/user-attachments/assets/468baecf-e06c-47a0-9800-d67ff6a8a817" />
<img width="535" height="98" alt="Screenshot 2026-02-25 193732" src="https://github.com/user-attachments/assets/e1aa8d60-9750-4540-b7c9-0e3b590ce01d" />

# Top Error Messages
- Extract all lines containing ERROR
- Identify the top 5 most common error messages
- Display them with their occurrence count, sorted in descending order
<img width="775" height="431" alt="Screenshot 2026-02-25 193924" src="https://github.com/user-attachments/assets/bc8f0124-8cef-45af-ad08-91557452ae1a" />
<img width="585" height="95" alt="Screenshot 2026-02-25 193933" src="https://github.com/user-attachments/assets/ebc1e188-0b0a-4cfb-b996-379fbb0b7564" />
<img width="474" height="82" alt="Screenshot 2026-02-25 193939" src="https://github.com/user-attachments/assets/ba492b3c-a110-4179-857b-1b9d510540d3" />
<img width="638" height="61" alt="Screenshot 2026-02-25 193947" src="https://github.com/user-attachments/assets/3ed5c079-165f-4f88-9bfd-a4217b85ec65" />
<img width="709" height="276" alt="Screenshot 2026-02-25 193957" src="https://github.com/user-attachments/assets/103a5daa-fa2b-4381-a712-68ed56340418" />
<img width="628" height="163" alt="Screenshot 2026-02-25 194012" src="https://github.com/user-attachments/assets/3ba5825b-0c97-4ac0-a607-308e63f30296" />

# Summary Report
- Generate a summary report to a text file named log_report_<date>.txt (e.g., log_report_2026-02-11.txt). The report should include:
- Date of analysis
- Log file name
- Total lines processed
- Total error count
- Top 5 error messages with their occurrence count
- List of critical events with line numbers
<img width="756" height="684" alt="Screenshot 2026-02-25 194343" src="https://github.com/user-attachments/assets/68e4321b-b54f-4f05-8a09-e4dc987032db" />
<img width="609" height="311" alt="Screenshot 2026-02-25 194358" src="https://github.com/user-attachments/assets/5f8eddb3-4820-43ec-82e2-c00c608b2ea0" />
<img width="559" height="72" alt="Screenshot 2026-02-25 194410" src="https://github.com/user-attachments/assets/840c0397-0db4-4897-ab9d-8719345984ac" />
<img width="594" height="253" alt="Screenshot 2026-02-25 194421" src="https://github.com/user-attachments/assets/eab4776b-5f2f-4227-b2f0-dabb50a65a05" />
<img width="523" height="47" alt="Screenshot 2026-02-25 194434" src="https://github.com/user-attachments/assets/9b72a64f-7625-4dd1-8eb9-8aae4325707b" />
<img width="592" height="318" alt="Screenshot 2026-02-25 194450" src="https://github.com/user-attachments/assets/2dce5255-6cec-4f30-8f3f-d5a4fecd63d9" />






























