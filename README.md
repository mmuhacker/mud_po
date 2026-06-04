<div align="center">

# 📱 Phone OSINT Tool
# 📱 أداة جمع معلومات رقم الهاتف

---

![Version](https://img.shields.io/badge/1.0-%EF%BA%8D%EF%BB%B9%EF%BA%BB%EF%BA%AA%EF%BA%8D%EF%BA%AE-blue?style=for-the-badge)<br>
![Platform](https://img.shields.io/badge/%EF%BB%9B%EF%BA%8E%EF%BB%9F%EF%BB%B2%20%EF%BB%9F%EF%BB%B4%EF%BB%A8%EF%BB%9C%EF%BA%B2-%EF%BA%8D%EF%BB%9F%EF%BA%92%EF%BB%B4%EF%BA%8C%EF%BA%94-green?style=for-the-badge&logo=kalilinux)<br>
![Platform](https://img.shields.io/badge/%EF%BA%84%EF%BB%A7%EF%BA%AA%EF%BA%AE%EF%BB%AE%EF%BB%B3%EF%BA%AA-%EF%BA%8D%EF%BB%9F%EF%BA%92%EF%BB%B4%EF%BA%8C%EF%BA%94-green?style=for-the-badge&logo=android)<br>
![Python](https://img.shields.io/badge/3.x-%EF%BA%91%EF%BA%8E%EF%BB%B3%EF%BA%9C%EF%BB%AE%EF%BB%A6-blue?style=for-the-badge&logo=python)<br>
![License](https://img.shields.io/badge/MIT-%EF%BA%8D%EF%BB%9F%EF%BA%98%EF%BA%AE%EF%BA%A7%EF%BB%B4%EF%BA%BA-red?style=for-the-badge)<br>
[![Author](https://img.shields.io/badge/mmuhacker-%EF%BA%8D%EF%BB%9F%EF%BB%A4%EF%BB%84%EF%BB%AE%D8%B1-red?style=flat-square)](https://github.com/mmuhacker)<br>
![Status](https://img.shields.io/badge/%EF%BB%A7%EF%BA%B8%EF%BB%82-%EF%BA%8D%EF%BB%9F%EF%BA%A4%EF%BA%8E%EF%BB%9F%EF%BA%94-blue?style=for-the-badge)

</div>

---

**📚 المحتويات**

- [نظرة عامة](#-نظرة-عامة)
- [المميزات](#-المميزات)
- [المتطلبات](#-المتطلبات)
- [التثبيت](#-التثبيت)
  - [التثبيت على Termux](#-على-Android-(Termux))
  - [التثبيت على Kali Linux](#التثبيت-على-kali-linux)

## 📋 نظرة عامة

أداة سطر أوامر مكتوبة بـ Python تُستخدم لجمع المعلومات المفتوحة المصدر (OSINT) حول أرقام الهاتف. تعمل بشكل كامل على **Termux (Android)** و**Kali Linux** مع واجهة مستخدم عربية بالكامل.

> ⚠️ **تنبيه قانوني:** هذه الأداة مخصصة للأغراض التعليمية والبحث الأمني الأخلاقي فقط. استخدمها بمسؤولية ووفقاً لقوانين بلدك.

---

## ✨ المميزات

| الميزة | الوصف |
|--------|-------|
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
```
phonenumbers
requests
```

## أدوات النظام
| البيئة | الأمر |
|--------|-------|
| Termux | `pkg install python` |
| Kali Linux | `sudo apt install python3 python3-pip` |

---

## 🚀 التثبيت

## على Termux (Android)

```bash
# 1. تثبيت Python إذا لم يكن مثبتاً
pkg update && pkg install python git

# 2. استنساخ المستودع
git clone https://github.com/mmuhacker/mud-po
cd mud-po

# 3. تشغيل الأداة (ستثبت المكتبات تلقائياً)
python mud_po.py
```

### على Kali Linux

```bash
# 1. استنساخ المستودع
git clone https://github.com/mmuhacker/mud-po
cd mud-po

# 2. تثبيت المكتبات
pip install -r requirements.txt

# 3. تشغيل الأداة
python3 mud_po.py
```

### تشغيل مباشر (بدون git)

```bash
# Termux
curl -LO https://raw.githubusercontent.com/mmuhacker/mud-po/main/mud_po.py
python mud_po.py

# Kali Linux
wget https://raw.githubusercontent.com/mmuhacker/mud-po/main/mud_po.py
python3 mud_po.py
```

---

## ⚙️ إعداد المفاتيح (اختياري)

لاستخدام APILayer و AbstractAPI (مجاناً حتى 100 طلب/شهر):

```bash
# احصل على مفتاح مجاني من https://apilayer.com
export APILAYER_KEY="مفتاحك_هنا"

# احصل على مفتاح مجاني من https://app.abstractapi.com
export ABSTRACT_KEY="مفتاحك_هنا"

# لحفظ المفاتيح بشكل دائم (Termux)
echo 'export APILAYER_KEY="مفتاحك"' >> ~/.bashrc
echo 'export ABSTRACT_KEY="مفتاحك"' >> ~/.bashrc
source ~/.bashrc
```

---

## 🎯 طريقة الاستخدام

### تشغيل الأداة

```bash
python3 mud_po.py
```

### الاستخدام خطوة بخطوة

```
1. شغّل الأداة
2. أدخل رقم الهاتف بالصيغة الدولية:
   مثال:  +962799123456   (الأردن)
          +966501234567   (السعودية)
          +201001234567   (مصر)
3. انتظر نتائج التحليل التلقائي الكامل
4. استخدم روابط OSINT للبحث الإضافي
5. اضغط Enter للبحث عن رقم آخر
6. اكتب  0  للخروج
```

### أزرار التحكم

| المفتاح | الوظيفة |
|---------|---------|
| `0` | خروج من الأداة |
| `8` | رجوع / إلغاء |
| `Enter` | تأكيد / متابعة |

---

## 📊 مثال على النتائج

```
╔══════════════════════════════════════════════════════════════════╗
║  ①  التحليل الأساسي للرقم
╠══════════════════════════════════════════════════════════════════╣
  ◦  الحالة                    ✅ رقم صحيح
  ◦  النوع                     📱 محمول
  ◦  E.164                     +962799123456
  ◦  المنطقة (عربي)            الأردن
  ◦  الشبكة                    Zain Jordan
  ◦  التوقيت                   Asia/Amman

  ②  NumLookup
  ◦  الدولة                    Jordan
  ◦  الشبكة                    Zain
  ◦  نوع الخط                  mobile

  ⑦  تقرير المخاطر
  🟢  لم يُرصد خطر واضح في التحليل الأولي
```

---

## 🗂️ هيكل الملفات

```
mud-po/
├── mud_po.py          # الملف الرئيسي
├── requirements.txt   # المكتبات المطلوبة
├── README.md          # هذا الملف
└── LICENSE            # رخصة MIT
```

---

## 📝 ملف requirements.txt

```
phonenumbers>=8.13.0
requests>=2.28.0
```

---

## 🤝 المساهمة

المساهمات مرحب بها! يمكنك:
- فتح Issue للإبلاغ عن خطأ
- تقديم Pull Request لإضافة ميزة
- اقتراح تحسينات عبر Issues

---

<div align="center">

## 👨‍💻 المطور

**Muhannad Daher**

[![GitHub](https://img.shields.io/badge/GitHub-mmuhacker-black?style=for-the-badge&logo=github)](https://github.com/mmuhacker)

---

## 📄 الرخصة
**MIT License — حر الاستخدام مع ذكر المصدر**

---
</div>

- أداة فحص المتاحات المتطورة (32) منصة
- البيئة: Termux (Android) / Kali Linux
- الإصدار: v1.0



---
<div align="center">

***Madarik Tools — صُنع بالعربية***

⭐ **إذا أعجبتك الأداة، لا تنسَ النجمة!** ⭐
</div>


</div>
