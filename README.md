![FANAKDZ PKG + Assassin's Creed DZ + Rockstar DZ](banner.png)

# متجر FANAKDZ للـ PlayStation 4

ثلاث حزم (fake PKG) لتشغيل مكتبة ألعاب على PS4 مكسور الحماية: تتصفّح الألعاب
بالصور، ثم تنزّل وتثبّت اللعبة مباشرة من الجهاز — **بدون حاسوب**.

---

## 📦 الحزم الثلاث

| الحزمة | المعرّف | الوصف |
|---|---|---|
| `IV0000-FANK00001_00-FANAKDZPKG000000.pkg` | FANK00001 | **FANAKDZ PKG** — المتجر الكامل بكل الألعاب |
| `IV0000-FANK00002_00-ASSASSINSCREEDZ0.pkg` | FANK00002 | **Assassin's Creed DZ** — ألعاب Assassin's Creed فقط |
| `IV0000-FANK00003_00-ROCKSTARDZ000000.pkg` | FANK00003 | **Rockstar DZ** — ألعاب Rockstar فقط |

الحزم **تطبيقات مستقلّة**: تُثبَّت معًا ولا تمحو إحداها الأخرى، ولكل واحدة
أيقونتها وصورتها الخاصة في مكتبة الجهاز. تطبيقا **Assassin's Creed DZ** و
**Rockstar DZ** يعرضان ألعابهما فقط بمجرّد الفتح (لا يحتاجان أي إعداد)، بينما
**FANAKDZ PKG** يعرض المكتبة كاملة.

الألعاب التي يعرضها كل تطبيق مأخوذة من المكتبة نفسها (866 لعبة):

| التطبيق | الألعاب |
|---|---|
| FANAKDZ PKG | المكتبة كاملة (866 لعبة) |
| Assassin's Creed DZ | Chronicles Trilogy · III · IV Black Flag · Mirage · Odyssey · Origins · Rogue · Syndicate · The Ezio Collection · Unity · Valhalla |
| Rockstar DZ | Grand Theft Auto V · Red Dead Redemption · Red Dead Redemption 2 · L.A. Noire |

---

## ✅ المتطلبات

* PS4 مكسور الحماية (GoldHEN أو أي HEN يعمل).
* اتصال بالإنترنت على الجهاز (Wi‑Fi أو كابل).
* مساحة كافية في `/data` (اللعبة الواحدة قد تصل إلى 90 غيغا، والتثبيت يستهلك
  الضعف مؤقتًا: التنزيل + التثبيت).

---

## 🛠️ طريقة التثبيت

### الطريقة 1 — عبر FTP ثم مُثبِّت الحزم (الأسهل)

**1) انسخ الملف إلى الجهاز**

عن طريق **FileZilla**:

| الحقل | القيمة |
|---|---|
| Host | `192.168.x.x` ‏(عنوان جهازك) |
| Port | `2121` |
| User | `anonymous` |
| Password | (اتركه فارغًا) |

ثم اسحب الملف إلى المجلد `/data/pkg/`.

أو بالأمر مباشرة (Windows / Linux / macOS):

```bash
curl -T IV0000-FANK00001_00-FANAKDZPKG000000.pkg  ftp://192.168.x.x:2121/data/pkg/
curl -T IV0000-FANK00002_00-ASSASSINSCREEDZ0.pkg  ftp://192.168.x.x:2121/data/pkg/
curl -T IV0000-FANK00003_00-ROCKSTARDZ000000.pkg  ftp://192.168.x.x:2121/data/pkg/
```

**2) ثبّت من الجهاز**

* افتح **GoldHEN** ← **Package Installer**، أو
  **Settings ← Debug Settings ← Game ← Package Installer**.
* اختر الملف من `/data/pkg` واضغط **Install**.
* انتظر انتهاء التثبيت، ثم ستجد التطبيق في الشاشة الرئيسية.

### الطريقة 2 — عبر فلاش USB (بدون شبكة)

1. ضع ملف `.pkg` في **جذر** فلاش USB مهيّأ بصيغة `FAT32` أو `exFAT`.
2. أشبك الفلاش في الجهاز.
3. **Package Installer** ← اختر **USB** ← حدّد الملف ← **Install**.

---

## 🎮 طريقة الاستخدام

افتح التطبيق: تظهر صورة البداية، ثم شبكة الألعاب بالصور.

| الزر | الوظيفة |
|---|---|
| **X** | تنزيل اللعبة المحدّدة وتثبيتها |
| **O (Circle)** | إلغاء / رجوع / خروج |
| **△ (Triangle)** | تسجيل الدخول إلى archive.org (للألعاب التي تحتاج حسابًا) |
| **الاتجاهات / العصا** | التنقّل بين الألعاب |
| **L1 / R1** | الصفحة التالية / السابقة |
| **L2 / R2** | قفزة كبيرة داخل القائمة |

عند اختيار **X** يظهر شريط التقدّم (نسبة التنزيل والسرعة)، وعند الانتهاء يبدأ
التثبيت تلقائيًا. لا تُغلق التطبيق أثناء التنزيل.

---

## 📁 المسارات المهمّة

| المسار | الوظيفة |
|---|---|
| `/data/pkg` | التنزيلات وملفات `.pkg` الجاهزة |
| `/data/fanakdz.log` | سجل التطبيق (يُقرأ عبر FTP عند أي مشكلة) |
| `/data/fanakdz_cookie.txt` | جلسة تسجيل الدخول إلى archive.org |
| `/data/fanakdz_store.txt` | كلمات رفّ FANAKDZ / Assassin's Creed (كلمة في كل سطر) |
| `/data/rockstar_store.txt` | كلمات رفّ Rockstar (اختياري — للتعديل فقط) |

> تطبيقا Assassin's Creed و Rockstar يعملان **بدون** أي ملف إعداد: قائمة
> ألعابهما مدمجة داخل التطبيق. الملفان أعلاه للتخصيص فقط إن أردت تغيير الرفّ.

---

## ❓ مشاكل شائعة

| المشكلة | الحل |
|---|---|
| **لا تظهر أي لعبة** | تأكّد من اتصال الجهاز بالإنترنت، ثم أعد فتح التطبيق |
| **التطبيق يتوقف عند الفتح** | افتح `/data/fanakdz.log` وأرسله؛ غالبًا سببها الشبكة |
| **التنزيل يتوقف في المنتصف** | أعد المحاولة؛ التنزيل يستأنف من حيث توقّف |
| **لا يظهر التطبيق في المكتبة** | أعد تشغيل الجهاز بعد التثبيت |
| **اللعبة تُنزَّل ببطء** | السرعة تعتمد على سيرفر الأرشيف؛ جرّب وقتًا آخر |

---

## 🔧 ملاحظات تقنية

* التطبيقات تعتمد على مكتبة عامة من موقع archive.org، وتُخزِّن قائمة الألعاب
  محليًّا لتعمل بسرعة عند كل فتح.
* التثبيت يستخدم خدمة **BGFT** الرسمية في النظام (نفس طريقة الألعاب العادية).
* التنزيل مُقسَّم إلى عدّة أقسام متوازية لتسريع التحميل، ويستأنف بعد الانقطاع.
* التطبيقات الثلاثة تُبنى من مصدر واحد، وكل تطبيق نسخة مستقلة بمعرّف خاص
  (`FANK00001` / `FANK00002` / `FANK00003`).

---

## English

Three PlayStation 4 homebrew packages (fake PKG) — no PC needed.

| File | Title ID | Description |
|---|---|---|
| `IV0000-FANK00001_00-FANAKDZPKG000000.pkg` | FANK00001 | **FANAKDZ PKG** — the full game store |
| `IV0000-FANK00002_00-ASSASSINSCREEDZ0.pkg` | FANK00002 | **Assassin's Creed DZ** — Assassin's Creed games only |
| `IV0000-FANK00003_00-ROCKSTARDZ000000.pkg` | FANK00003 | **Rockstar DZ** — Rockstar games only |

The two shelf builds show their own games as soon as they open, no setup at
all; the full store shows the whole library. All three can be installed side
by side.

**Install**

1. Copy the `.pkg` to the console, e.g. over FTP to `/data/pkg`
   (`curl -T file.pkg ftp://<console-ip>:2121/data/pkg/`), or put it on a
   FAT32/exFAT USB stick.
2. On the console open **GoldHEN → Package Installer**, pick the file and
   press **Install**.

**Controls** — `X` download & install, `O` cancel, `△` sign in to
archive.org, `L1/R1` page, `L2/R2` jump. Downloads land in `/data/pkg`.
