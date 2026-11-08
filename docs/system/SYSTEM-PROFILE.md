# الملف المرجعي الدائم للجهاز الشخصي (System Profile)

> **الغرض:** مرجع موحّد لمواصفات الجهاز ونتائج الفحوصات التي أُجريت، ليستطيع المساعد استكمال الإدارة والتشخيص عبر المحادثات دون إعادة جمع المعلومات من الصفر.
>
> **آخر مراجعة:** 2026-11-09 (تحديث لاحق لفحص مجلد NoVirusThanks)  
> **حالة العمل:** اكتشاف العتاد مكتمل مبدئيًا، وجرد البرامج والخدمات جارٍ. لم تُجرَ أي تغييرات على إعدادات الجهاز أو ملفاته.

## 1. قواعد إدارة الجهاز

- المساعد يتولى التخطيط والتحليل وتحديد خطوات التشخيص؛ المستخدم ينفذ الأوامر على الجهاز.
- التدرج من الفحوصات الآمنة للقراءات فقط إلى الاختبارات الأعمق.
- لا تعطيل خدمات أو برامج، ولا حذف ملفات أو تنظيف أو تغيير إعدادات أو تثبيت/إزالة برامج دون شرح الأثر والحصول على موافقة صريحة مسبقة.
- كل نتيجة تُصنّف بوضوح: حقيقة مرصودة، استنتاج مبدئي، أو أمر لم يُتحقق منه.
- تحديث هذا الملف وسجل التغييرات بعد كل جلسة تشخيص مهمة.
- لا تُخزّن أسماء حسابات ويندوز أو أسماء المستخدمين أو الموقع الدقيق.

## 2. خارطة إدارة الجهاز

1. **Hardware & System Discovery:** اكتشاف المواصفات والعتاد.
2. **Software Inventory:** جرد البرامج والتطبيقات والتعريفات والخدمات وعناصر بدء التشغيل.
3. **System Audit & Security:** إعدادات ويندوز والتحديثات والحماية والشبكة والصلاحيات والملفات المؤقتة.
4. **Performance & Optimization:** تحليل الاستهلاك والاختناقات وتحسين الأداء.
5. **Maintenance & Incident Response:** الصيانة الدورية والنسخ الاحتياطي وتشخيص الأخطاء.

لا تُعد أي مرحلة مكتملة إلا بعد استكمال فحوصاتها وتوثيق أدلتها. حتى تاريخ هذا الملف لم تُجرَ تغييرات على الجهاز.

## 3. مواصفات الجهاز والعتاد

### الجهاز والنظام
| البند | القيمة |
|---|---|
| الشركة | Lenovo |
| الجهاز | ThinkPad T470 |
| رقم الطراز | 20HD000MMX |
| المعالج | Intel Core i5-7300U @ 2.60GHz |
| الأنوية / المعالجات المنطقية | 2 / 4 |
| تردد المعالج المرصود | 2712 MHz |
| الذاكرة المثبتة | 8.00 GB |
| إجمالي الذاكرة الفعلية الظاهر | 7.84 GB |
| الذاكرة المتاحة وقت تقرير msinfo32 | 2.45 GB |
| النظام | Windows 10 Pro |
| إصدار النظام / البناء | 10.0.19045 / Build 19045 |
| البنية | 64-bit |
| BIOS | Lenovo N1QETA4W (1.79) |
| تاريخ BIOS | 2024-11-05 |
| وضع BIOS | UEFI |
| Secure Boot | Enabled |
| Virtualization-Based Security (VBS) | Running |
| Kernel DMA Protection | Off |
| Hypervisor | Detected |
| PCR7 Configuration | Binding غير متاح؛ تظهر رسالة ترقية مطلوبة |
| Windows Defender Application Control | Policy Enforced |

**ملاحظات:** ظهور Hypervisor يعني أن بعض ميزات Hyper-V قد لا تظهر بالطريقة المعتادة في استعلامات النظام. لا يُستنتج من ذلك وجود خلل.

### الذاكرة RAM
| البند | القيمة |
|---|---|
| الشرائح الظاهرة في الفحص | شريحة واحدة |
| BankLabel | BANK 0 |
| DeviceLocator | ChannelA-DIMM0 |
| السعة | 8 GB |
| السرعة الحالية | 2133 MHz |
| ConfiguredClockSpeed | 2133 MHz |
| Manufacturer code | 0443 |
| Part Number | RMSA3260MB78HAF2400 |

رقم القطعة يتضمن 2400، لكن السرعة الحالية والمضبوطة 2133MHz. لا يُحسم توافق ترقية الذاكرة أو شراء شريحة إضافية قبل الرجوع إلى مواصفات Lenovo الدقيقة والتحقق من تكوين الجهاز.

### التخزين
| البند | القيمة |
|---|---|
| القرص | SAMSUNG MZVLB256HAHQ-000L7 |
| النوع | SSD |
| الناقل | NVMe |
| السعة بالبايت | 256060514304 |
| السعة التقريبية | 238.5 GiB |
| HealthStatus في Windows | Healthy |

| القسم | نظام الملفات | الإجمالي | المساحة الحرة |
|---|---|---:|---:|
| C: | NTFS | 108.4 GB | 13.5 GB |
| D: | NTFS | 129.8 GB | 70.7 GB |

المساحة الحرة في C تقارب 12.5%. لا يبدأ التنظيف أو الحذف قبل تحليل استهلاك المساحة. قيمة HealthStatus من Windows ليست اختبار SMART شاملاً ولا تشخيصًا مادياً نهائياً للقرص.

### الرسوميات والشاشة
| البند | القيمة |
|---|---|
| GPU | Intel(R) HD Graphics 620 |
| DriverVersion | 26.20.100.6709 |
| دقة العرض المرصودة | 1920 × 1080 |

لا تُستنتج سعة VRAM من AdapterRAM في الرسوميات المدمجة.

### البطارية
| البند | القيمة |
|---|---:|
| اسم البطارية | 01AV421 |
| الشركة المصنعة | SMP |
| السعة التصميمية | 24,000 mWh |
| سعة الشحن الكامل | 21,030 mWh |
| عدد دورات الشحن | 379 |
| الصحة التقديرية | 87.6% |
| التآكل التقديري | 12.4% |

الحساب: 21,030 ÷ 24,000 = 87.625%. التقدير جيد مبدئيًا ولا يعطي وحده سببًا واضحًا لاستبدال البطارية. تقرير Windows تقديري وليس اختبارًا ماديًا. أظهر فحص Win32_Battery حالة OK وشحنًا 100% وقت الفحص.

سجل استهلاك مرصود:
- 2026-11-05: استهلاك 81% خلال 1:50:24.
- 2026-11-07: استهلاك 15% خلال 26:04.
لا تُستنتج مدة تشغيل ثابتة من هاتين الجلستين؛ الحمل والسطوع والاتصال والبرامج تؤثر.

## 4. جرد البرامج والتطبيقات

تم استخراج جرد من مفاتيح Uninstall في Registry؛ التقرير الأصلي احتوى 390 سطرًا. من البرامج البارزة:

- Cloudflare One Client 26.6.880.0
- Copilot 152.0.4191.64
- Cursor 3.7.36
- Docker Desktop 4.80.0
- Git 2.54.0
- Google Chrome 156.0.8078.82
- Kaspersky VPN 21.27.6.532
- K-Lite Mega Codec Pack 17.2.5
- Microsoft Edge 152.0.4191.66
- Microsoft OneDrive 26.189.0928.0009
- Microsoft Silverlight 5.1.10411.0 وSilverlight 4/5 SDK
- مكونات SQL Server 2012 وSSDT وIIS Express و.NET
- Visual Studio Code 1.143.1
- NVM for Windows 1.2.2
- Python 3.13.14
- Windows Subsystem for Linux 2.7.12.0
- Firefox 159.0.1
- WinRAR 6.11 64-bit و6.23 32-bit
- FormatFactory وGIMP وVLC وPotPlayer وMPC-BE وUltraISO
- NoVirusThanks Win Update Stop v1.4
- تطبيقات Chrome مسجلة مثل Docs وGmail وGoogle Drive وSheets وSlides وYouTube.

هذه قائمة جرد وليست توصية بإزالة البرامج. لا تُصنّف البرامج القديمة أو النسخ المتعددة بأنها غير لازمة أو ضارة دون فحص الاستخدام والاعتماديات.

## 5. عناصر بدء التشغيل

أظهر فحص Win32_StartupCommand عشرة عناصر:

1. OneDrive — مزامنة خلفية.
2. Microsoft Edge Update.
3. BingWallpaperDaemon — مساره يشير إلى UnInstDaemon.exe داخل مسار مؤقت تحت LOCALAPPDATA؛ عنصر غير معتاد ويحتاج تحققًا، لكنه ليس دليلًا كافيًا على برمجية ضارة.
4. Adobe Acrobat Synchronizer.
5. Docker Desktop.
6. Microsoft.Lists — OneDrive.Sync.Service.exe.
7. Mozilla Firefox مع الوسيط -os-autostart.
8. MicrosoftEdgeAutoLaunch.
9. SecurityHealth — أيقونة Windows Security.
10. CloudflareWARP.

لم يتم تعطيل أي عنصر.

## 6. الخدمات المهمة

تم فحص الخدمات التي حالتها Running أو نمط بدء تشغيلها Automatic؛ التقرير احتوى 292 سطرًا. من النتائج المهمة:

- **WinUpdStopSvc:** خدمة NoVirusThanks Win Update Stop، Running، Automatic، تعمل باسم LocalSystem.
- **wuauserv:** Windows Update، ظهرت Stopped وManual في لقطة الفحص.
- **UsoSvc:** Update Orchestrator، Running وAutomatic.
- **BITS:** Background Intelligent Transfer Service، Running وAutomatic.
- **WaaSMedicSvc:** Stopped وManual.
- خدمات Microsoft Defender الأساسية وخدمة الجدار الناري mpssvc كانت تعمل.
- خدمات Cloudflare WARP والمحدّث كانت تعمل.
- خدمة Kaspersky VPN كانت تعمل.
- خدمات WSL وHyper-V compute/network ظهرت ضمن الخدمات العاملة.
- SQLWriter يعمل؛ وهذا لا يثبت أن محرك SQL Server نفسه يعمل.
- SysMain وWSearch يعملان.
- توجد خدمات أخرى متوقفة عند الطلب، وهو أمر قد يكون طبيعيًا.

لم يتم تعطيل أو تعديل أي خدمة.

## 7. تدقيق Windows Update

### السياسات ومفاتيح Registry
تم فحص:
- HKLM:\SOFTWARE\Policies\Microsoft\Windows\WindowsUpdate
- HKLM:\SOFTWARE\Policies\Microsoft\Windows\WindowsUpdate\AU

لم يُعثر على هذين المفتاحين. كما فُحص المسار:
- HKLM:\SOFTWARE\Microsoft\Windows\CurrentVersion\WindowsUpdate\Auto Update

المسار الأخير موجود، لكن لم تظهر قيم WUServer أو WUStatusServer أو UseWUServer أو AUOptions في المخرجات. غياب المفتاحين الأولين لا يثبت غياب كل وسائل التحكم بالتحديثات.

### البحث اليدوي عن التحديثات
استخدم المستخدم Windows Update COM API:
```powershell
$session = New-Object -ComObject Microsoft.Update.Session
$searcher = $session.CreateUpdateSearcher()
$result = $searcher.Search("IsInstalled=0 and IsHidden=0")
```

النتيجة:
- Search Result Code: 2 (Succeeded)
- Available Updates: 2
- Microsoft Defender Antivirus security intelligence KB2267602، version 1.463.191.0 (current channel extended)
- MediaTek - Other hardware - Android Composite ADB Interface

هذا يثبت نجاح البحث اليدوي في لحظة الاختبار فقط؛ لا يثبت نجاح التنزيل أو التثبيت أو عمل التحديث التلقائي.

### سجل التحديثات والأخطاء
نتائج QueryHistory تضمنت عمليات ناجحة، وأخرى برموز غير ناجحة/متوقفة. أمثلة:
- 2026-10-23: LivelyWallpaper، ResultCode 5، HRESULT 0x8024000B.
- 2026-09-30: WindowsAppRuntime.2 و1.5، ResultCode 4، HRESULT 0x80240034.
- 2026-07-21: Defender intelligence، ResultCode 4، HRESULT 0x80240017.
- 2026-07-17: Defender platform، ResultCode 4، HRESULT 0x80240009.
- 2026-07-16: Defender intelligence، ResultCode 4، HRESULT 0x80240034.
- 2026-07-08: Defender intelligence، ResultCode 4، HRESULT 0x80240016.
- 2026-07-06: Windows 10 cumulative KB5094127، ResultCode 5، HRESULT 0x8024000B، مع عمليات أخرى.
- 2026-06-30: تعريفات Samsung USB/modem وتحديثات Defender وWindows وMRT ظهرت لها عمليات برموز 4 أو 5.

لا يعني كل سجل غير 2 بالضرورة فشل تثبيت؛ قد يعكس إلغاء أو تخطي أو عدم انطباق.

أحداث WindowsUpdateClient:
- Event ID 26 تكرر بين 2026-11-05 و2026-11-09 مع عمليات بحث ناجحة عثرت على أعداد مختلفة من التحديثات.
- Event ID 25 في 2026-11-08 00:06:00: الخطأ 0x80240439.
- أخطاء سابقة في 2026-11-02: 0x8024402C و0x8024402F.
- أخطاء في 2026-09-27: 0x80240438 و0x80240440 و0x80240439.
- أخطاء في 2026-09-16: 0x8024402C و0x80240438.

الأخطاء متقطعة وتتخللها عمليات بحث ناجحة؛ لم يثبت سبب جذري بعد.

### Proxy وDNS والاتصال
- WinHTTP Proxy: Direct access (no proxy server).
- Internet Settings: ProxyEnable=0، ProxyServer فارغ، AutoConfigURL فارغ.
- DNS النشط على Wi-Fi: 192.168.100.1.
- واجهة Wi-Fi النشطة: Intel Dual Band Wireless-AC 8265.
- Default IPv4 route عبر Wi-Fi 2 إلى 192.168.100.1.
- محول Kaspersky VPN: Disconnected.
- Hyper-V Default Switch: Up.
- لم يظهر محول باسم Cloudflare/WARP في فحص المحولات، رغم أن خدمات Cloudflare كانت تعمل.
- فشل استعلام DNS سابق بسبب اختلاف/محارف اسم الواجهة؛ نجح استخدام InterfaceIndex. لا يُعد ذلك عطلًا بالنظام.

اختبارات Resolve-DnsName وTest-NetConnection على TCP 443 نجحت وقت الاختبار مع:
- www.microsoft.com
- update.microsoft.com
- download.windowsupdate.com
- sls.update.microsoft.com

هذه النتائج تثبت حل DNS والوصول إلى TCP 443 وقت الاختبار فقط، ولا تثبت TLS أو HTTP أو نجاح بروتوكول التحديث أو التنزيل والتثبيت.

## 8. التحقيق في NoVirusThanks Win Update Stop

### هوية الملف والتوقيع
المسار:
`C:\Program Files\NoVirusThanks\Win Update Stop\WinUpdStopSvc.exe`

| الخاصية | القيمة |
|---|---|
| الحجم | 2,178,280 bytes |
| CreationTime | 2022-10-18 17:45:58 |
| LastWriteTime | 2018-08-24 17:25:28 |
| CompanyName | NoVirusThanks Company Srl |
| ProductName | NoVirusThanks Win Update Stop Service |
| FileDescription | NoVirusThanks Win Update Stop Service |
| FileVersion | 1.0.0.0 |
| Authenticode Status | Valid |
| StatusMessage | Signature verified. |
| Signer | NoVirusThanks Company Srl |

### إعداد الخدمة
نتيجة sc.exe qc:
- TYPE: WIN32_OWN_PROCESS
- START_TYPE: AUTO_START
- ERROR_CONTROL: IGNORE
- BINARY_PATH_NAME: المسار أعلاه
- SERVICE_START_NAME: LocalSystem
- لا توجد Dependencies.
- sc.exe enumdepend أظهر entriesread = 0.

كما ظهر process باسم WinUpdStopSvc، PID 4544، ولم يعرض الاستعلام مسار ExecutablePath.

### التقييم
- التوقيع الرقمي صالح ويطابق اسم الشركة المضمّن في بيانات الملف.
- هذا يقلل الشك في انتحال الملف لهوية الشركة، لكنه لا يثبت سلامة كل سلوك البرنامج أو حداثته.
- الخدمة تعمل تلقائيًا بصلاحيات LocalSystem، واسم المنتج ووظيفته المعلنة مرتبطان بإيقاف Windows Update.
- لذلك فهي **عامل محتمل مهم** في سلوك التحديثات، لكن لا يوجد حتى الآن دليل مباشر يثبت أنها سبب الأخطاء أو أنها تمنع التحديث التلقائي تحديدًا.
- لم تُعثر مفاتيح Registry في HKLM:\SOFTWARE\NoVirusThanks أو HKLM:\SOFTWARE\WOW6432Node\NoVirusThanks؛ وهذا لا يثبت عدم وجود إعدادات في مواقع أخرى.

### فحص المجلد والملفات والعمليات — نُفّذ
نفّذ المستخدم فحص قراءة فقط لمجلد البرنامج وملفاته والعمليات ذات الصلة، وكانت النتائج:

**نتائج المجلد:**
- FullName: `C:\Program Files\NoVirusThanks\Win Update Stop`
- CreationTime: 2022-10-18 17:45:57
- LastWriteTime للمجلد: 2022-10-18 17:45:58

**الملفات الموجودة:**

| الملف | الحجم بالبايت | LastWriteTime |
|---|---:|---|
| Changelog.txt | 1,621 | 2018-08-24 20:36:34 |
| EULA.txt | 4,133 | 2018-01-13 16:23:14 |
| Help.txt | 1,590 | 2018-08-23 18:29:14 |
| Homepage.url | 55 | 2011-05-03 10:58:04 |
| unins000.dat | 14,187 | 2022-10-18 17:45:58 |
| unins000.exe | 727,272 | 2022-10-18 17:45:54 |
| unins000.msg | 11,401 | 2022-10-18 17:45:58 |
| WinUpdateStop.exe | 2,735,336 | 2018-08-25 00:51:56 |
| WinUpdStopSvc.exe | 2,178,280 | 2018-08-24 17:25:28 |

**العمليات ذات الصلة:**
- ظهرت عملية واحدة: `WinUpdStopSvc.exe`، PID `4544`.
- `ExecutablePath` و`CommandLine` لم يُرجعهما الاستعلام.

**الاستنتاج المحدّث:**
- الملفات التنفيذية الرئيسية تعود تواريخ تعديلها إلى أغسطس 2018، بينما أُنشئ مجلد التثبيت وملفات إلغاء التثبيت في أكتوبر 2022.
- هذا يرجّح أن نسخة البرنامج قديمة، لكنه لا يثبت وحده عدم توافقها أو وجود سلوك ضار.
- وجود ملفي البرنامج الرئيسي والخدمة وسجل المساعدة/التغييرات يتيح الانتقال إلى مراجعة الوثائق النصية المرفقة قبل أي قرار.
- لا توقف الخدمة أو تغيّر Startup Type أو تحذف البرنامج قبل شرح الأثر والحصول على موافقة صريحة.

**الخطوة التالية المقترحة (لم تُنفذ بعد):** قراءة محتويات `Changelog.txt` و`Help.txt` و`EULA.txt` فقط، لفهم ما يذكره البرنامج عن وظائفه وطريقة التحكم بالتحديثات. لا يتطلب ذلك أي تغيير في الجهاز.

## 9. ما لم يُفحص بعد

- بقية تفاصيل التعريفات والأجهزة الملحقة.
- جرد شامل للبرامج مع تحديد الاستخدام والاعتماديات، لا مجرد الأسماء.
- تحليل عناصر بدء التشغيل والخدمات غير المعتادة بالتفصيل.
- فحص حالة Cloudflare WARP الفعلية ونفقه.
- فحص سلامة ملفات ويندوز ومكونات النظام.
- تحليل مساحة C: على مستوى المجلدات والملفات دون حذف.
- مراجعة الحماية والأمان والشبكة بصورة أوسع.
- تحليل الأداء واستهلاك CPU وRAM والقرص.
- النسخ الاحتياطي وخطة الاستعادة.

## 10. سجل التغييرات

### 2026-11-09 — تحديث فحص NoVirusThanks
- إضافة نتائج تاريخ المجلد والملفات التسعة الموجودة فيه.
- تسجيل ظهور عملية الخدمة الوحيدة (PID 4544) مع عدم توفر مسار التنفيذ وسطر الأوامر في الاستعلام.
- تحديث الاستنتاج: ملفات البرنامج الرئيسية معدّلة في 2018، ومجلد التثبيت أُنشئ في 2022؛ لا يُعد ذلك دليلًا على الضرر أو عدم التوافق.
- تحديد قراءة ملفات Changelog وHelp وEULA كخطوة تالية للقراءة فقط.
- **لم تُجرَ أي تغييرات على الجهاز.**

### 2026-11-09 — إنشاء الملف المرجعي الأول
- تجميع نتائج العتاد والنظام والتخزين والبطارية.
- إضافة جرد البرامج وعناصر بدء التشغيل والخدمات.
- توثيق فحوص Windows Update والشبكة والأخطاء.
- توثيق التحقق من توقيع وإعداد خدمة NoVirusThanks.
- تسجيل الخطوة التشخيصية التالية غير المنفذة.
- **لم تُجرَ أي تغييرات على الجهاز.**
