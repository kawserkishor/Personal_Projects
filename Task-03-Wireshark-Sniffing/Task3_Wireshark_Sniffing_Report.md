# 🛠️ Task 03 – Sniffing Attack using Wireshark

## 🎯 Objective

To simulate a credential sniffing attack using Wireshark by capturing unencrypted HTTP traffic from the target website:

> http://testphp.vulnweb.com

This task demonstrates how sensitive information, like login credentials, can be intercepted over unsecured HTTP connections — a critical web security weakness.

---

## 🧰 Tools Used

- **Wireshark** (GUI-based network analyzer)
- **Browser** (to manually send HTTP POST request)

---

## 🧪 Methodology

### Step 1: Packet Capture Initialization
- Launched **Wireshark** and began capturing on the active network interface (`eth0` / `wlan0`)
- Applied a basic capture filter (optional): tcp.pot==80

### Step 2: Performed Login Action on Target
- Opened browser and navigated to: http://testphp.vulnweb.com/login.php
- Submitted dummy credentials:
  - Username: admin
  - Password: admin

### Step 3: Filtering HTTP POST Requests
- Applied the display filter in Wireshark: http.request.method == “POST”
- Located the `POST` request to `/login.php`

> <img width="1322" alt="image" src="https://github.com/user-attachments/assets/82193beb-fae5-4a4c-b2ef-6348856141c2" />


### Step 4: Extracting Plaintext Credentials
- Right-clicked on the HTTP POST request → `Follow > HTTP Stream`
- Observed the full raw HTTP request containing: uname=admin&pass=admin&submit=submit
- > <img width="682" alt="image" src="https://github.com/user-attachments/assets/adb4563e-1343-4a26-8fde-6a722ba876bc" />


---

## 🔍 Observations

- Login credentials were transmitted in **plaintext**
- This is expected since the site uses **HTTP instead of HTTPS**
- Any attacker on the same network can easily intercept these credentials

---

## 🛡️ Mitigation Strategies

| Vulnerability | Recommendation |
|---------------|----------------|
| Plaintext credential transmission | Enforce HTTPS using valid TLS certificates |
| Network sniffing risk | Use VPNs and secured Wi-Fi for end users |
| Sensitive endpoints unprotected | Implement HSTS, secure cookies, and CSRF tokens |

---

## ✅ Conclusion

This task clearly demonstrates how insecure web traffic can be intercepted using network sniffing tools. In a real-world scenario, this type of attack is used in **Man-in-the-Middle (MitM)** attacks to steal credentials or sensitive data.

> Sniffing is trivial when the application doesn't use encryption. Always use HTTPS.

---

**Prepared by**: A K M Kawser Ahmed  
**Internship Program**: Future Intern  
**Task**: #3 – Sniffing Attack with Wireshark
