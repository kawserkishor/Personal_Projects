## Task 3 – Sniffing Attack using Wireshark

We used Wireshark to capture HTTP login credentials from `http://testphp.vulnweb.com`. The attack exploited the fact that HTTP transmits data in plaintext.

By applying a `http.request.method == "POST"` filter and submitting dummy credentials to the login form, we captured the raw request and extracted:

- **Username**: admin
- **Password**: admin

This simulates a real-world network attack where attackers on the same network intercept credentials from unsecured sites.

### Mitigation:
Use HTTPS to encrypt traffic and prevent credential sniffing.
