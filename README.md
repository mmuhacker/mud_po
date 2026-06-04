<div align="center">

```
  ██████╗  ██████╗     ░░░░░░  ░░░░░░
  ██╔══██╗██╔═══██╗   ░██╔══█╗░██╔══█╗
  ██████╔╝██║   ██║   ░██████╔╝░██║  ░║
  ██╔═══╝ ██║   ██║   ░██╔═══╝ ░██║  ░║
  ██║     ╚██████╔╝   ░██║     ░╚█████╔╝
  ╚═╝      ╚═════╝    ░╚═╝     ░ ╚════╝
```

# 📱 MUD-PO — Phone OSINT Tool

**أداة استخبارات أرقام الهاتف مفتوحة المصدر**

[![Python](https://img.shields.io/badge/Python-3.8%2B-blue?style=flat-square&logo=python)](https://python.org)
[![Platform](https://img.shields.io/badge/Platform-Termux%20%7C%20Kali%20Linux-green?style=flat-square)](https://github.com/mmuhacker/mud-po)
[![License](https://img.shields.io/badge/License-MIT-yellow?style=flat-square)](LICENSE)
[![Author](https://img.shields.io/badge/Author-mmuhacker-red?style=flat-square)](https://github.com/mmuhacker)

</div>

---

## 📋 نظرة عامة

**MUD-PO** أداة سطر أوامر مكتوبة بـ Python تُستخدم لجمع المعلومات المفتوحة المصدر (OSINT) حول أرقام الهاتف. تعمل بشكل كامل على **Termux (Android)** و**Kali Linux** مع واجهة مستخدم عربية بالكامل.

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

### المكتبات (تُثبَّت تلقائياً)
```
phonenumbers
requests
```

### أدوات النظام
| البيئة | الأمر |
|--------|-------|
| Termux | `pkg install python` |
| Kali Linux | `sudo apt install python3 python3-pip` |

---

## 🚀 التثبيت

### على Termux (Android)

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

## 📄 الرخصة

```
MIT License — حر الاستخدام والتعديل والتوزيع
```

---

<div align="center">

**صُنع بـ ❤️ بواسطة [mmuhacker](https://github.com/mmuhacker)**

[![GitHub](https://img.shields.io/badge/GitHub-mmuhacker-black?style=flat-square&logo=github)](https://github.com/mmuhacker)

</div>
