---
type: Page
title: Task - 1
description: null
icon: null
createdAt: '2025-06-27T09:33:17.129Z'
creationDate: 2025-06-27 15:33
modificationDate: 2025-06-27 16:47
tags: []
coverImage: null
---

## STEP 1: Advance Linux Commands:

[image](https://app.capacities.io/dbfac0d5-fc54-497f-b05f-90b6c4a00c27/ade0d1dd-cc57-4180-8c17-244754eae2fd)

[image](https://app.capacities.io/dbfac0d5-fc54-497f-b05f-90b6c4a00c27/f46f6090-666b-48a4-98ce-538de901dd10)

## STEP 2: Installing GitHub Tools

### dirsearch

```bash
git clone https://github.com/maurosoria/dirsearch.git
cd dirsearch
python3 dirsearch.py -u http://testphp.vulnweb.com
```

[image](https://app.capacities.io/dbfac0d5-fc54-497f-b05f-90b6c4a00c27/9001dabe-07b3-445e-9e36-c3963e8e566a)

### SQLMap

```bash
git clone https://github.com/sqlmapproject/sqlmap.git
cd sqlmap
python3 sqlmap.py --version
```

[image](https://app.capacities.io/dbfac0d5-fc54-497f-b05f-90b6c4a00c27/7bc87b79-61de-45f1-a7bb-73be26bc148e)

## **STEP 3: Launch Attacks on** **testphp.vulnweb.com**

### **Directory Brute Forcing via dirsearch**

```bash
python3 dirsearch.py -u http://testphp.vulnweb.com
```

[image](https://app.capacities.io/dbfac0d5-fc54-497f-b05f-90b6c4a00c27/a10bd21b-e1b7-4597-96fe-0c8f7f0c821b)

### SQL Injection via sqlmap

```bash
python3 sqlmap.py -u "http://testphp.vulnweb.com/artists.php?artist=1" --dbs
```

[image](https://app.capacities.io/dbfac0d5-fc54-497f-b05f-90b6c4a00c27/a49bc4dd-fa64-4790-a5ca-8d58f82b8cb3)
