<div align="center">

# 📱 Phone OSINT Tool

# 📱 أداة جمع معلومات رقم الهاتف

---

<div align="center">

<img src="img/001.jpg"
width="90%"
style="border-radius: 20px;
border: 2px solid var(--color-border-default);
box-shadow: 0 8px 16px rgba(0,0,0,0.2);
background: var(--color-canvas-default);
padding: 5px;">

</div>

---

[![by](https://img.shields.io/badge/mmuhacker-%EF%BA%97%EF%BB%84%EF%BB%AE%EF%BB%B3%EF%BA%AE-blue?style=for-the-badge&logo=github)](https://github.com/mmuhacker)<br>
![Version](https://img.shields.io/badge/1.0-%EF%BA%8D%EF%BB%B9%EF%BA%BB%EF%BA%AA%EF%BA%8D%EF%BA%AE-blue?style=for-the-badge&logo=semver)<br>
![Platform](https://img.shields.io/badge/%EF%BB%9B%EF%BA%8E%EF%BB%9F%EF%BB%B2%20%EF%BB%9F%EF%BB%B4%EF%BB%A8%EF%BB%9C%EF%BA%B2-%EF%BA%8D%EF%BB%9F%EF%BA%92%EF%BB%B4%EF%BA%8C%EF%BA%94-green?style=for-the-badge&logo=kalilinux&logoColor=%23FFC107)<br>
![Platform](https://img.shields.io/badge/%EF%BA%84%EF%BB%A7%EF%BA%AA%EF%BA%AE%EF%BB%AE%EF%BB%B3%EF%BA%AA-%EF%BA%8D%EF%BB%9F%EF%BA%92%EF%BB%B4%EF%BA%8C%EF%BA%94-green?style=for-the-badge&logo=android)<br>
![Python](https://img.shields.io/badge/3.x-%EF%BA%91%EF%BA%8E%EF%BB%B3%EF%BA%9C%EF%BB%AE%EF%BB%A6-blue?style=for-the-badge&logo=python)<br>
![License](https://img.shields.io/badge/%EF%BA%97%EF%BA%AE%EF%BA%A7%EF%BB%B4%EF%BA%BA%20%EF%BA%A7%EF%BA%8E%D8%B5-%EF%BA%8D%EF%BB%9F%EF%BA%98%EF%BA%AE%EF%BA%A7%EF%BB%B4%EF%BA%BA-8A2BE2?style=for-the-badge&logo=law)<br>
![Status](https://img.shields.io/badge/%EF%BB%A7%EF%BA%B8%EF%BB%82-%EF%BA%8D%EF%BB%9F%EF%BA%A4%EF%BA%8E%EF%BB%9F%EF%BA%94-blue?style=for-the-badge&logo=statuspal)<br>

---

**📚 المحتويات**

</div>

- [نظرة عامة](#-نظرة-عامة)
- [المميزات](#-المميزات)
- [المتطلبات](#-المتطلبات)
- [التثبيت](#تثبيت)
  - [التثبيت على Termux](#تيرموكس)
  - [التثبيت على Kali Linux](#كالي)
- [التثبيت بأمر واحد](#أمر)
- [اعداد المفاتيح](#مفاتيح)
- [طريقة الاستخدام](#طريقة-الإستخدام)
- [أزرار التحكم](#أزرار)
- [أمثلة على النتائج](#نتائج)
- [هيكل الملفات](#-هيكل-الملفات)
- [ملف requirements.txt](#ملفات)
- [المساهمة](#مساهمة)
- [المطور](#المطور)
- [الرخصة](#رخصة)
- [صور الأداة](#img)

---

<div align="center">
     
## 📋 نظرة عامة

</div>

أداة سطر أوامر مكتوبة بـ Python تُستخدم لجمع المعلومات المفتوحة المصدر (OSINT) حول أرقام الهاتف. تعمل بشكل كامل على **Termux (Android)** و**Kali Linux** مع واجهة مستخدم عربية بالكامل.

> ⚠️ **تنبيه قانوني:** هذه الأداة مخصصة للأغراض التعليمية والبحث الأمني الأخلاقي فقط. استخدمها بمسؤولية ووفقاً لقوانين بلدك.

---

<div align="center">


## ✨ المميزات

| الميزة | الوصف |
|--------|-------|
| 🔑 **مفاتيح API**|يمكن إستخدام المفاتيح للحصول على معلومات أكثر دقة|
| 🔍 **تحليل أساسي كامل** | نوع الرقم، صحته، الشبكة، المنطقة الزمنية، صيغ E.164/INTL/RFC3966 |
| 🌍 **معلومات الدولة والشبكة** | اسم المشغل، رمز الدولة، المنطقة الجغرافية بالعربي والإنجليزي |
| 🔗 **12+ رابط OSINT مباشر** | Truecaller، Google، Telegram، Facebook، Twitter، Sync.me، WhoCallsMe، SpamCalls وغيرها |
| 💬 **تحقق واتساب** | رابط مباشر للتحقق من تسجيل الرقم في واتساب |
| 🌐 **NumLookup API** | استعلام مجاني تلقائي عن معلومات الرقم |
| 🔑 **APILayer + AbstractAPI** | دعم APIs إضافية (تتطلب مفتاح مجاني) |
| ⚠️ **تقرير المخاطر** | كشف أرقام VoIP، الأرقام المجانية، مزودي الخدمات المجهولين |
| 🇸🇦 **واجهة عربية كاملة** | جميع النصوص والرسائل بالعربية |
| 🤖 **تثبيت تلقائي** | تكتشف الأداة المكتبات الناقصة وتثبتها تلقائياً |

---

## 📦 المتطلبات


## المكتبات (تُثبَّت تلقائياً)

</div>


```
phonenumbers>=8.13.0
requests>=2.28.0
arabic-reshaper>=3.0.0
python-bidi>=0.4.0
```

<div align="center">
  
## أدوات النظام

| البيئة | الأمر |
|--------|-------|
| Termux | `pkg install python` |
| Kali Linux | `sudo apt install python3 python3-pip` |

</div>

---

<div align="center" id="تثبيت">
     
## 🚀 التثبيت والتشغيل

<div align="center" id="تيرموكس">
  
📱 **Android — Termux**

</div>

**الخطوة 1 — تحديث النظام وتثبيت Python**

```bash
pkg update && pkg upgrade -y
pkg install python -y
```

**الخطوة 2 — تثبيت المكتبات الأساسية**

```bash
pip install arabic-reshaper python-bidi
```

**الخطوة 3 — تثبيت الخط العربي (للعرض الصحيح)**

```bash
curl -L "https://fonts.gstatic.com/s/notonaskharabic/v33/RrQ5bpV-9Dd1b1OAGA6M9PkyDuVBePeKNaxcsss0Y7bwvc-VaA.ttf" -o ~/.termux/font.ttf
termux-reload-settings
```
⚠️ **هام: أغلق Termux تماماً من قائمة التطبيقات الخلفية وافتحه من جديد**

**الخطوة 4 — تنزيل الأداة وإنشاء الاختصار**

```bash
curl -o $`PREFIX/bin/mud_po.py https://raw.githubusercontent.com/mmuhacker/mud-po/main/mud_po.py
chmod +x `$PREFIX/bin/mud_po.py
ln -sf $`PREFIX/bin/mud_po.py `$PREFIX/bin/po
```

**الخطوة 5 — تشغيل الأداة**

```bash
po
```

⚡ **أو قم بكل شيء بأمر واحد مجمّع**

```bash
pkg update && pkg upgrade -y && pkg install python -y && pip install arabic-reshaper python-bidi && curl -L "https://fonts.gstatic.com/s/notonaskharabic/v33/RrQ5bpV-9Dd1b1OAGA6M9PkyDuVBePeKNaxcsss0Y7bwvc-VaA.ttf" -o ~/.termux/font.ttf && termux-reload-settings && curl -o $`PREFIX/bin/mud_po.py https://raw.githubusercontent.com/mmuhacker/mud-po/main/mud_po.py && chmod +x `$PREFIX/bin/mud_po.py && ln -sf $`PREFIX/bin/mud_po.py `$PREFIX/bin/po && echo "✅ تم التثبيت بنجاح! استخدم الأمر: po" && po
```

---

🐉 **Kali Linux**

**الخطوة 1 — تحديث النظام وتثبيت Python**

```bash
sudo apt update && sudo apt upgrade -y
sudo apt install python3 python3-pip -y
```

**الخطوة 2 — تثبيت المكتبات الأساسية**

```bash
pip3 install arabic-reshaper python-bidi
```

**الخطوة 3 — تنزيل الأداة وإنشاء الاختصار**

```bash
sudo curl -o /usr/local/bin/mud_po.py https://raw.githubusercontent.com/mmuhacker/mud-po/main/mud_po.py
sudo chmod +x /usr/local/bin/mud_po.py
sudo ln -sf /usr/local/bin/mud_po.py /usr/local/bin/po
```

**الخطوة 4 — تشغيل الأداة**

```bash
po
```

⚡ **أو قم بكل شيء بأمر واحد مجمّع**

```bash
sudo apt update && sudo apt upgrade -y && sudo apt install python3 python3-pip -y && pip3 install arabic-reshaper python-bidi && sudo curl -o /usr/local/bin/mud_po.py https://raw.githubusercontent.com/mmuhacker/mud-po/main/mud_po.py && sudo chmod +x /usr/local/bin/mud_po.py && sudo ln -sf /usr/local/bin/mud_po.py /usr/local/bin/po && echo "✅ تم التثبيت بنجاح! استخدم الأمر: po" && po
```

---

## ⚙️ إعداد المفاتيح (اختياري)

**لاستخدام APILayer و AbstractAPI (مجاناً حتى 100 طلب/شهر):**
⚡️**هذه المفاتيح تعطيك معلومات أكثر عن الأرقام وبدقة عالية
يمكن استخدام الأداة بدون مفاتيح**

احصل على مفتاح مجاني من https://apilayer.com
احصل على مفتاح مجاني من https://app.abstractapi.com
احفظ المفاتيح في مكان آمن

📷 الواجهة الرئيسية – إضافة مفاتيح API
الشكل 1: إضافة مفاتيح API


<div align="center">


📷 **القائمة الرئيسية – إدراج مفاتيح API**

<img src="img/PO1.png"
width="90%"
style="border-radius: 20px;
border: 2px solid var(--color-border-default);
box-shadow: 0 8px 16px rgba(0,0,0,0.2);
background: var(--color-canvas-default);
padding: 5px;">

<i style="color: var(--color-fg-default);">الشكل 1: إدخال المفاتيح</i>

</div>
───

## 🎯 طريقة الاستخدام
تشغيل الأداة
bash
po

الاستخدام خطوة بخطوة
1. شغّل الأداة
2. أدخل رقم الهاتف بالصيغة الدولية:
مثال: +962799123456 (الأردن)
+966501234567 (السعودية)
+201001234567 (مصر)

<div align="center">


📷 **إدخال الرقم**

<img src="img/PO2.png"
width="90%"
style="border-radius: 20px;
border: 2px solid var(--color-border-default);
box-shadow: 0 8px 16px rgba(0,0,0,0.2);
background: var(--color-canvas-default);
padding: 5px;">

<i style="color: var(--color-fg-default);">الشكل 2: إدخال الرقم</i>

</div>
1. اضغط Enter لبدء الفحص
2. انتظر نتائج التحليل التلقائي الكامل


<div align="center">


📷 **مثال على النتائج**

<img src="img/PO3.png"
width="90%"
style="border-radius: 20px;
border: 2px solid var(--color-border-default);
box-shadow: 0 8px 16px rgba(0,0,0,0.2);
background: var(--color-canvas-default);
padding: 5px;">
<img src="img/PO4.png"
width="90%"
style="border-radius: 20px;
border: 2px solid var(--color-border-default);
box-shadow: 0 8px 16px rgba(0,0,0,0.2);
background: var(--color-canvas-default);
padding: 5px;">

<i style="color: var(--color-fg-default);">الشكل 3: مثال على النتائج</i>

</div>

3. استخدم روابط OSINT للبحث الإضافي
4. اضغط Enter للبحث عن رقم آخر
5. اكتب 0 للخروج

───

أزرار التحكم
المفتاح الوظيفة
0 خروج من الأداة
8 رجوع / إلغاء
Enter تأكيد / متابعة

───

📊 أمثلة على النتائج
📷 صور النتائج

الشكل 4: النتائج

───

🗂️ هيكل الملفات
mud-po/
├── img/               # صور الأداة
├── mud_po.py          # ملف الأداة الرئيسي
├── requirements.txt   # المكتبات المطلوبة
├── LICENSE            # رخصة MIT
└── README.md          # هذا الملف


───

📝 ملف requirements.txt
phonenumbers&gt;=8.13.0
requests&gt;=2.28.0
arabic-reshaper&gt;=3.0.0
python-bidi&gt;=0.4.0


───

🤝 المساهمة
المساهمات مرحب بها! يمكنك:
· فتح Issue للإبلاغ عن خطأ
· تقديم Pull Request لإضافة ميزة
· اقتراح تحسينات عبر Issues

---

<div align="center" id="المطور">

## 👨‍💻 المطور

**Muhannad Daher**

[![GitHub](https://img.shields.io/badge/GitHub-mmuhacker-black?style=for-the-badge&logo=github)](https://github.com/mmuhacker)

</div>

---

<div align="center" id="رخصة">
  
## 📄 الرخصة

  </div>
  
**رخصة الاستخدام والنشر مع منع التعديل** – يُسمح باستخدام الأداة ونشرها بحرية، لكن يُمنع تعديل الكود أو هندسته عكسياً. راجع [الترخيص](https://github.com/mmuhacker/mud_po/blob/main/LICENSE.md) للتفاصيل الكاملة.

---

<div align="center" id="img">

## صور الأداة

</div>

<img src="img/po1.png" width="45%" style="border-radius: 20px;
border: 2px solid var(--color-border-default);
box-shadow: 0 8px 16px rgba(0,0,0,0.2);
background: var(--color-canvas-default);
padding: 5px;">
<img src="img/po2.png" width="45%" style="border-radius: 20px;
border: 2px solid var(--color-border-default);
box-shadow: 0 8px 16px rgba(0,0,0,0.2);
background: var(--color-canvas-default);
padding: 5px;">
<img src="img/po3.png" width="45%" style="border-radius: 20px;
border: 2px solid var(--color-border-default);
box-shadow: 0 8px 16px rgba(0,0,0,0.2);
background: var(--color-canvas-default);
padding: 5px;">
<img src="img/po4.png" width="45%" style="border-radius: 20px;
border: 2px solid var(--color-border-default);
box-shadow: 0 8px 16px rgba(0,0,0,0.2);
background: var(--color-canvas-default);
padding: 5px;">

---


- أداة جمع معلومات الأرقام
- البيئة: Termux (Android) / Kali Linux
- الإصدار: v1.0



---

<div align="center">

***Madarik Tools — صُنع بالعربية***

⭐ **إذا أعجبتك الأداة، لا تنسَ النجمة!** ⭐

</div>
