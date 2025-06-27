# 🔓 Task 04 – Password Cracking using John the Ripper

## 🎯 Objective

Simulate an offline password cracking scenario using John the Ripper by targeting a weak hash of the password `password123`. The goal is to demonstrate how attackers crack poorly chosen passwords using pre-built wordlists and basic hash algorithms.

---

## 🧰 Tools Used

| Tool | Purpose |
|------|---------|
| John the Ripper | Brute-force/dictionary hash cracking |
| rockyou.txt | Common password wordlist |
| md5sum | Linux tool to generate MD5 hashes |

---

## 🔢 Hash Generation

We first generated an MD5 hash for the string `password123`:

```bash
echo -n "password123" | md5sum
```

Output: 482c811da5d5b4bc6d497ffa98491e38

This hash simulates a compromised credential leaked from a vulnerable system.
<img width="501" alt="image" src="https://github.com/user-attachments/assets/1eee67fa-5e3a-45b0-91e5-1ea93372dae7" />


⚒️ Cracking Process
	1.	Saved the hash into a file:
      echo "482c811da5d5b4bc6d497ffa98491e38" > hash.txt

  2.	Executed John with a popular wordlist: ```bash john --format=raw-md5 --wordlist=/usr/share/wordlists/rockyou.txt hash.txt```
 
  3.	Cracked password was discovered successfully: password123
  
  4.	Verified the result: ```bash john --show hash.txt```
      output: 482c811da5d5b4bc6d497ffa98491e38:password123


<img width="768" alt="image" src="https://github.com/user-attachments/assets/8d746187-9320-400b-9a6c-678db7fcd2e3" />


⸻

🔍 Analysis

This task demonstrates how trivial it is to crack weak passwords using open-source tools and known wordlists. Attackers can crack thousands of leaked hashes in minutes using a basic CPU — and even faster using GPU tools like Hashcat.

⸻

✅ Conclusion

Even simple tools like John the Ripper can easily break common passwords like password123. This underscores the critical importance of secure password storage and usage practices.

⸻
