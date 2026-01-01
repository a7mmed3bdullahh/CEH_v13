

دي مرحله اسمها مرحله جمع المعلومات ال Pentester بيجيب بقا المعلومات اللي هتفيدو في عمليه البينتيست دي وفيها هنا نوعين لجمع المعلومات اول نوع وهو

Passive information Gathering:

دا ال Pentester بيجيب معلومات عن التارجت او الهدف بدون التفاعل مع الهدف والمعلومات اللي بيحصل عليها معلومات زي

- تحديد عناوين IP ومعلومات DNS.
- تحديد أسماء النطاقات وملكيتها.
- تحديد عناوين البريد الإلكتروني وملفات التعريف على وسائل التواصل الاجتماعي.
- تحديد التقنيات المستخدمة في المواقع المستهدفة.
- تحديد النطاقات الفرعية.

Active Information Gathering:

المرحله دي بيحصل تفاعل بين البينتستر وبين الهدف بتاعه والمعلومات اللي بيحصل عليها معلومات زي

- اكتشاف المنافذ المفتوحة على الأنظمة المستهدفة.
- التعرف على البنية التحتية الداخلية لشبكة الهدف.
- استخراج المعلومات من الأنظمة المستهدفة.

**طيب هو هنا الهاكر او الشخص ال Pentester بيستخدم اي علشان يجيب المعلومات دي يعني اي الادوات اللي بيستخدمها وهكذا**

- Whois Enumeration :لجمع معلومات النطاق.
- **DNS Recon**: DNS. لاستكشاف وتحليل معلومات
- **WAF Detection With wafw00f**: للكشف عن جدران الحماية.
- **Subdomain Enumeration With Sublist3r**: لتحديد النطاقات الفرعية
- **Google Dorks**: لاستخدام محركات البحث بفعالية في جمع المعلومات
- .**Email Harvesting With theHarvester**: لجمع عناوين البريد الإلكتروني
- .**Leaked Password Databases**: للبحث في قواعد بيانات كلمات المرور المسربة.
- **DNS Zone Transfers**: DNS.لاستكشاف نقل المناطق في
- **سجلات DNS**: A, AAAA, NS, MX, CNAME, TXT، وغيرها.
- **استجواب DNS (DNS Interrogation)**: هو عملية تحليل سجلات DNS للحصول على معلومات هامة مثل عناوين IP والنطاقات الفرعية.
- **نقل منطقة DNS (DNS Zone Transfer)**:إذا كان مكونًا بشكل غير صحيح، يمكن استغلال هذه العملية للحصول على نظرة شاملة على شبكة المنظمة.
- **Host Discovery With Nmap**: لاكتشاف الأجهزة الموجودة على الشبكة.
- **Port Scanning With Nmap**: لفحص المنافذ المفتوحة

---

طيب هنتكلم عن الادوات وازاي تثبتها وتشتغل بيها

- **`Whois`**

للتثبيت علي لينكس

`sudo apt-get update sudo apt-get install whois`

استخدامها

`whois [example.com](<http://example.com/>)`

`whois 8.8.8.8`

- Waffw00f تثبيت

`python3 --version`

`pip3 install waffw00f`

`waffw00f [<http://example.com>](<http://example.com/>)`

- Sublist3r تثبيت

sudo apt-get install git

`pip install -r requirements.txt`

استخدامها

`python [sublist3r.py](<http://sublist3r.py/>) -d [example.com](<http://example.com/>)`

- theHarvester تثبيت

`sudo apt-get install git`

**`git clone <https://github.com/laramies/theHarvester.git`**>

`pip install -r requirements.txt`

استخدامها

`python3 [theHarvester.py](<http://theharvester.py/>) -d [example.com](<http://example.com/>) -b all`

- Nmap تثبيت

`sudo apt-get update sudo apt-get install nmap`

استخدامها

```
nmap -p 80 [example.com](<http://example.com/>)
```

**`كدا الحمد لله تم انتهاء سكشن ال Information Gathering علي خير `**


