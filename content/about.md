---
title: "GPG Key & CTF Challenge"
layout: "about"
summary: "verify my identity"
---

<h1>🔒 我的 GPG 公鑰</h1>
<p>這是我的身分驗證金鑰。如果您需要傳送加密訊息給我，請使用此公鑰。</p>

<pre style="background-color: #161b22; border: 1px solid #30363d; padding: 15px; color: #7ee787; overflow-x: auto;">
-----BEGIN PGP PUBLIC KEY BLOCK-----

mJMEaV6kqxMJKyQDAwIIAQENBAMEfe/Lw/rBU/s3PYSJFCcBUzxLIimoKTOa0Kr7
fFcnzskg/StJ4xJSwbmoSvKokToTWD5IzVJxT4ybehSB6DQFqToF+svfh0MKvYI/
uRmaxMQSvQDWLaqAqG3o0NJO3zkGUo8H+uEeUeDb4lHsFnOnLm/nEbA1YbRmCIcX
UQQ1JZi0OG1haW4gPGYwZDFhYzJhLTNjODctNDFiMS1hYWNmLTIyYWM2ZGRlOWE0
YkBhbm9uYWRkeS5jb20+iNMEExMKADsWIQSdL5ASUDYOAwpbwVRpO0rS+JFLsQUC
aV6kqwIbAwULCQgHAgIiAgYVCgkICwIEFgIDAQIeBwIXgAAKCRBpO0rS+JFLsfdi
AgCVHM7CkB1bImyL7XAmqYd5viTXtN0sjVucX2tpTgTMOrIm+DylN3CW/VFwtAMQ
hgaTYWhdazC34tT+QC0L3zFEAf99FGOSbKzX2lS0qe+rNsP2jmiH2rnDyjrJKP6j
b6OeGNV+BXLs1uQKxNs9Cd8r1NhkhlbKMx1zWpvNZvhDfbCWiLUEEBMKAB0WIQRJ
mNU4F60g5oYTUspgsJxAOghp8AUCaV6k5QAKCRBgsJxAOghp8CBNAgCC4/OdXoHo
TODywqHq0HBpNa9iuJSOqO+OQwKE7djHtjK69HzsydxEMAZz3sOdyYdAT6u2MXr7
qp3yF/BtWxG4AgCUzQiqd92eRzOkciCnsvKBYradCOdzzl8RlQf5ExhgC4kPLGnO
Y+Sp9LywosfjNlvZmlc/N3YrDV7V5lz/sutHuJcEaV6kqxIJKyQDAwIIAQENBAME
ZoROU2kzGT4QzeibZUnSzZfGW5OcIJcXt6UMDz48n46sZzZp7pbG009cAgFGDPuA
2u2Sm6MjiarSIb+GGGlsnUA0MmUKUtt+yx2CJkIphlIzJ9ctK8VcOAeJ9zrNijba
yjQ0qB8eiallxPUWFr9LT00hgImdYrot98+vmJyVtroDAQoJiLgEGBMKACAWIQSd
L5ASUDYOAwpbwVRpO0rS+JFLsQUCaV6kqwIbDAAKCRBpO0rS+JFLsbJyAgCVeuj7
IYZoEhu2Cm1+4gBgD5X8RqxHcWdHUacS8RMTKlfcdiiBPRTi/cqzcezq5K8ICuWj
242fkBqZV+LkTBF8AfoCWUUHratvKh0gZdeov+aWvWVQz64Pg+T/GcX8fQDfTBTR
E3JB+i/9dMXrtmstPYab6ZN3/ShLyNgq4L5Ik5Oo
=fSDZ
-----END PGP PUBLIC KEY BLOCK-----
</pre>

<div style="margin-top: 30px; border-top: 1px solid #30363d; padding-top: 20px;">
    📂 <a href="https://12587456.xyz/public.asc" download="9D2F901250360E030A5BC154693B4AD2F8914BB1_gpg.asc" style="color: #58a6ff;">下載公鑰 (.asc)</a>
</div>

<div class="ctf-zone" style="margin-top: 50px; border: 1px dashed #d29922; padding: 20px; background-color: #1c1c1c;">
<h3>🕵️ CTF Challenge: Find the Flag</h3>
<p>此區域已被鎖定。只有擁有 root 權限的人才能找到密碼。</p>

<input type="text" id="passInput" placeholder="Enter Password" style="background-color: #0d1117; border: 1px solid #30363d; color: #c9d1d9; padding: 5px;">
<button onclick="checkPass()" style="background-color: #238636; color: white; border: none; padding: 6px 12px; cursor: pointer;">Unlock</button>

<p id="result" style="margin-top:10px; color: #ff7b72;"></p>
</div>

<script>
console.log("%c [SYSTEM] Debug Mode: ON", "color: orange; font-weight: bold;");
console.log("Hint: The password is obfuscated using Base64.");

function checkPass() {
var userIn = document.getElementById('passInput').value;
var resultDisplay = document.getElementById('result');
var secret = "U2VjcmV0MjAyNg=="; 

if (btoa(userIn) === secret) {
    resultDisplay.style.color = "#7ee787";
    resultDisplay.innerHTML = "🎉 ACCESS GRANTED! <br> FLAG{GitHub_Pages_Hacker_101}";
    alert("恭喜！你成功破解了前端驗證！");
} else {
    resultDisplay.style.color = "#ff7b72";
    resultDisplay.innerHTML = "⛔ ACCESS DENIED. Password Incorrect.";
}
}
</script>

### 🛠️ Tech Stack & Tools

![Linux](https://img.shields.io/badge/Linux-FCC624?style=for-the-badge&logo=linux&logoColor=black)
![Kali](https://img.shields.io/badge/Kali_Linux-557C94?style=for-the-badge&logo=kali-linux&logoColor=white)
![Bash](https://img.shields.io/badge/Shell_Script-121011?style=for-the-badge&logo=gnu-bash&logoColor=white)
![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Git](https://img.shields.io/badge/GIT-E44C30?style=for-the-badge&logo=git&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)

### ⚔️ Security & CTF

![Metasploit](https://img.shields.io/badge/Metasploit-333333?style=for-the-badge&logo=metasploit&logoColor=white)
![Wireshark](https://img.shields.io/badge/Wireshark-1679A7?style=for-the-badge&logo=wireshark&logoColor=white)
![Burp Suite](https://img.shields.io/badge/Burp_Suite-FF6633?style=for-the-badge&logo=burpsuite&logoColor=white)
![CTF](https://img.shields.io/badge/CTF-Capture_The_Flag-red?style=for-the-badge&logo=hack-the-box&logoColor=white)
![GPG](https://img.shields.io/badge/GPG-Privacy-0093dd?style=for-the-badge&logo=gnuprivacyguard&logoColor=white)


<br>
<hr style="border: 0; border-top: 1px dashed #333; margin: 40px 0;">

<div style="background: #0d1117; border: 1px solid #30363d; padding: 20px; border-radius: 6px; font-family: 'Courier New', monospace;">
  <h3 style="margin-top: 0; color: #ff7b72;">💉 SQL Injection Playground</h3>
  <p style="font-size: 0.9rem; color: #8b949e; margin-bottom: 15px;">
    Legacy database query interface. <br>
    <span style="color: #d2a8ff;">DO NOT</span> attempt to drop tables.
  </p>
  
  <div style="display: flex; gap: 10px; flex-wrap: wrap;">
    <input type="text" id="sqlTrapAbout" placeholder="SELECT * FROM users WHERE id=..." 
           style="flex: 1; padding: 10px; background: #010409; border: 1px solid #30363d; color: #79c0ff; border-radius: 4px; font-family: inherit; min-width: 200px;">
    
    <button onclick="runSQLTrap()" 
            style="padding: 10px 20px; background: #238636; color: white; border: none; border-radius: 4px; cursor: pointer; font-weight: bold; transition: 0.2s;">
      EXECUTE
    </button>
  </div>
  
  <div id="sqlOutputAbout" style="margin-top: 15px; padding: 10px; min-height: 40px; border-left: 3px solid #30363d; background: #161b22; color: #8b949e; font-size: 0.85rem;">
    > Waiting for input...
  </div>
</div>

<script>
function runSQLTrap() {
  const input = document.getElementById('sqlTrapAbout').value;
  const output = document.getElementById('sqlOutputAbout');
  
  // 偵測攻擊特徵
  const suspicious = /['";]|\b(OR|UNION|SELECT|DROP|INSERT|DELETE|UPDATE|--)\b/i;
  
  output.innerHTML = "<span style='color:#79c0ff'>[+] Connecting to MySQL server...</span>";
  
  setTimeout(() => {
    if (suspicious.test(input)) {
      // 觸發陷阱
      output.innerHTML = `
        <span style='color:#ff7b72'>[!] FATAL ERROR: WAF INTERCEPTION</span><br>
        ----------------------------------------<br>
        Payload: <span style='color:#d2a8ff'>${input}</span><br>
        Signature: <span style='color:#d2a8ff'>SQL_INJECTION_ATTEMPT</span><br>
        Source IP: <span style='color:#d2a8ff'>LOGGED</span><br>
        Action: <span style='color:red; font-weight:bold; background:#300;'>BLOCK & REPORT</span>
      `;
    } else if (input.trim() === "") {
      output.innerHTML = "> Waiting for input...";
    } else {
      // 普通輸入
      output.innerHTML = "<span style='color:#d29922'>[-] Error: Connection timed out (Error Code: 0xDEADBEEF)</span>";
    }
  }, 600);
}
</script>