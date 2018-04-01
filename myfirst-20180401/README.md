## Binary : From reverse to Pwn

- soeasy

**說明：**

第一堂逆向工程課

課堂老師出了一題簡單的程式要比對輸入的資料是否滿足某條件，聰明的你應該很快就解出答案。

**File**

/binary/reverse

- MyFirstObfuscatedCode

**說明：**

日本風格的javascript變裝術

軟體保護技術中,代碼混淆是一種常見的技術。

wikipedia上說明"代碼混淆是將電腦程式的代碼，轉換成一種功能上等價，但是難於閱讀和理解的形式的行為"。

這是你的第一堂代碼混淆課,請嘗試解出附件。

提示1: 開始了解代碼混淆,請看維基百科的說明 :

[https://zh.Wikipedia.org/zh-tw/代碼混淆](https://zh.wikipedia.org/zh-tw/%E4%BB%A3%E7%A2%BC%E6%B7%B7%E6%B7%86)

提示2: "功能上等價"就是可以執行,答案會和原始程式執行所得到的答案一樣。

**File**

/binary/MyFirstObfuscatedCode.txt

- pwntools

**說明：**

網路上有很多資源，駭客總是可以自行解決難題。

你也來練習撰寫script替自己解決問題。

提示:需在60秒內解決1000道簡單數學計算

nc 140.110.112.29 2113

**File**

/binary/pwntools.c
/binary/pwntools

- return

**說明：**

控制暫存器rip等同控制世界!

提示1 : 經典的buffer overflow漏洞

提示2 : 你可透過劫持當下function的return address來控制程式執行指針至目標位置。

nc 140.110.112.29 2114

**File**

/binary/return


- shellcode

**說明：**

厲害的駭客都擅長shellcoding

提示1:題目將輸入直接當machine code執行

提示2:撰寫組語，以及提交正確功能的shellcode。

nc 140.110.112.29 2115

**File**

/binary/shellcode


- rop

**說明：**

NX位元(No eXecute bit，意即「禁止執行位」)是應用在CPU中的一種安全技術。

本題NX Protection是啟用的，但它仍然是可以是駭客的pwnable。

提示1 : 有關 NX 位元的說明請參看[維基百科](https://en.wikipedia.org/wiki/NX_bit)

提示2 : 你如何繞過 strlen 的檢查。

nc 140.110.112.29 2116

**File**

/binary/rop

- memo_manager

**說明：**

所有保護都已啟用，如果可以的話給它 Pwn 下去!!

提示1:透過leak memory來bypass ASLR以及PIE，而overflow漏洞並不是直接性的，必須分析binary的行為來觸發漏洞。

提示2:在 relro full 全開的情況下，不能 GOT hijacking，最後只能 overflow 16 bytes，可以直接 onegadget，或是 stack migration 後做簡單的 ret2libc。

nc 140.110.112.29 2117


**File**

/binary/memo_manager
/binary/libc.so.6


## Misc : From PPC to Forensics

- Ascii

**說明：**

ASCII(American Standard Code for Information Interchange)全名為美國資訊交換標準代碼，是基於拉丁字母的電腦編碼，前期主要用於表示現代英文，擴展版本後甚至支援其他部分西歐語言。

最著名的就是Ascii Table，請對照Ascii Table解碼下列十進位資料:

77 121 70 105 114 115 116 67 84 70 123 90 50 79 97 115 54 55 65 69 54 68 117 65 51 73 50 112 56 69 53 125

- Secrets in PDF

**說明：**

第一線資安工程師在攻擊事件現場蒐集到犯罪所遺留的文件，身為鑑識專家的你請協助我們完成找出隱藏在資料裡的資料。

**File**

/misc/Secret.pdf

- Secret of Metadata

**說明：**

這是一張可疑圖片，身為鑑識專家的你請協助我們完成者找出隱藏在圖片裡的資料。

**File**

/misc/Meta_pic.jpg

- Secret images in pictures

**說明：**

另一張可疑圖片。

身為鑑識專家的你，發現圖片大小異常，很可能還藏著另一張圖片，請協助我們完成者找出隱藏在圖片裡的圖片。

提示1 : 你如何知道圖片藏有圖片??

提示2 : dd是一個linux平台上好用的工具，可以幫助你解題。

**File**

/misc/Secret_pic.png

- Sniffering

**說明：**

Insecurity 銀行的遠端連線伺服器發現遭受到駭客植入木馬，銀行的資安人員通知MyFirstSecurity資安技術服務工程師到場進行蒐證。

MyFirstSecurity資安技術服務工程師在現場收集網路封包後，建議Insecurity銀行採用安全的遠端連線。

請你找出網路封包中的flag。

提示1: 遠端連線使用的協定中使用明文傳輸容易遭致網路竊聽

**File**

/misc/Broken_session.pcap


- InSecureDataTransfer

**說明：**

MyFirstSecurity資安工程師在攻擊事件現場側錄到遺留有犯罪的可疑封包。

身為鑑識專家的你請協助我們完成者找出隱藏在資料的秘密。

提示1 : Wireshark 可以幫助你

**File**

/misc/File_transfer.pcap


## Web : From OWASP to TOP10

- Developer Tools

**說明：**

資安人員在某公司的網站上發現網站開發人員因為方便開發，而將重要資訊列在前端程式碼中，你能快速的找到這致命的錯誤嗎?

提示1: MyFirstCTF{xxxxxxxxxxx}

提示2: 你清楚知道 base64 編碼與解碼的原理嗎?

參看[維基百科](https://zh.wikipedia.org/wiki/Base64)

**File**

/web/index.html

## Crytpo : From classical to modern

- 我愛凱薩

**說明：**

凱撒密碼(Caesar cipher)將加密前的字串按照一定的數目向左或向右移動，替換出來的字串就成為密文。這是古典密碼最知名的加密方式也是破密分析第一堂課。

請破解以下凱薩密碼:

TfMpyzaJAM{PcrHMREJZErVwHuUwFYH}

提示1:答案格式 : MyFirstCTF{xxxxxxxxxxx}

提示2:線上資源或是使用python都可以快速解出答案

提示3:嘗試看看brute force解題

- Transposition ciphers

**說明：**

資安人員在InsecureBank做資安健檢，發現某台電腦存在可疑的程式在深夜固定時間都會送出一些特定封包給特定IP，顯示似乎已遭到駭客植入木馬。在網路封包中經常發現底下附件的通關密語，內容看似亂碼又似乎有規則性，聰明的你能分辯出正確的訊息嗎?

提示1 : 答案格式 : MyFirstCTF{xxxxxxxxxxx}

提示2 : 答案格式本身就是提示

**File**

/crytpo/Transposition_ciphers.txt

- MyFirstRSA

**說明：**

RSA加密演算法是著名的非對稱加密演算法，在電子商業中RSA加密被廣泛使用。資安人員在某間公司發現他們的產品使用RSA加密技術時，RSA某些參數設計不夠嚴謹很容易被破解。

這是你的第一堂RSA破密分析作業。聰明的你能解出明文嗎?

提示1 :請參看維基百科RSA加密演算法的說明 :

https://en.wikipedia.org/wiki/RSA_(cryptosystem)

當然你可以點選中文解說

提示2：n很小可以先分解出p和q質數。你可以善用線上資源解質因數分解。　

提示3：解出來的明文必須是MyFirstCTF{xxxxxxxxxxx}答案格式。

**File**

/crytpo/RSA.txt

- XOR_Cipher

**說明：**

對稱式密碼中常用xor運算，廷廷宣稱他把一支程式用xor加密了，誰都打不開。

你應該可以證明他錯了!

提示1:你應該清楚xor運算的特色 ，請參看維基百科的說明:https://en.wikipedia.org/wiki/Exclusive_or

當然你可以點選中文解說

提示2:你必須要先算出解密用的key。

**File**

/crytpo/Encrypted