# تسليم سياق إدارة الجهاز — متابعة في محادثة ChatGPT جديدة

**تاريخ إعداد الملف:** 2026-11-20  
**المستودع:** `hamdanaltawaf-cpu/-_-`  
**الفرع:** `main`  
**المرجع الأساسي:** `docs/system/SYSTEM-PROFILE.md`

> هذا الملف نقطة تسليم للمحادثة الجديدة. الملف المرجعي أعلاه يحتوي السجل التفصيلي والمواصفات والفحوصات؛ اقرأه قبل طلب معلومات سبق جمعها.

## دور المساعد وقواعد العمل
- يعمل المساعد كـ System Architect & AI SysAdmin للجهاز الشخصي: التخطيط، التشخيص، تحليل النتائج، وتوثيق GitHub. المستخدم هو من ينفذ الأوامر على Windows.
- أسلوب المستخدم: العربية باللهجة اليمنية، هادئ، مختصر، وخطوات قليلة قابلة للنسخ.
- التشخيص أولاً وبالتدرج؛ لا نكرر الفحوصات دون سبب.
- أوامر القراءة فقط أولاً. لا تثبيت أو إزالة برامج، أو حذف بيانات، أو تعديل إعدادات/services/registry، إلا بعد موافقة واضحة من المستخدم.
- لا تدّعِ أن إجراء محلي تم؛ نحتاج تأكيد المستخدم أو مخرجات تحقق.
- تحديث `docs/system/SYSTEM-PROFILE.md` بعد كل جلسة تشخيص/قرار مهم، مع حالة مؤكدة مقابل غير مؤكدة.
- لا تعتبر مرحلة من خطة الجهاز مكتملة بلا أدلة موثقة.

## الجهاز
- Lenovo ThinkPad T470، model 20HD000MMX.
- Intel Core i5-7300U 2.60GHz، 2 cores / 4 logical processors.
- RAM: 8GB (7.84GB usable)، شريحة واحدة، 2133MHz.
- Windows 10 Pro 22H2، build 19045، 64-bit، UEFI.
- BIOS Lenovo N1QETA4W 1.79.
- Secure Boot On، VBS On، Kernel DMA Protection Off، Hypervisor detected.
- Intel HD Graphics 620، driver 26.20.100.6709، 1920x1080.
- Samsung NVMe SSD MZVLB256HAHQ-000L7، نحو 238.5 GiB.
- آخر مساحة C موثقة: Free 15,475,662,848 bytes (نحو 14.41 GiB / 15.48 GB عشري) في 2026-11-09؛ يلزم تحديثها بعد عمليات إزالة المتصفحات.
- Battery 01AV421: design 24,000mWh، full charge 21,030mWh، 379 cycles، صحة تقديرية 87.6%.

## الحالة الحالية للمتصفحات
### مؤكد
- Chrome 156.0.8078.82؛ بيانات `%LOCALAPPDATA%\\Google\\Chrome` نحو 2.76 GB.
- Edge 152.0.4191.66؛ بيانات `%LOCALAPPDATA%\\Microsoft\\Edge` نحو 0.75 GB.
- Edge WebView2 Runtime 152.0.4191.66: مكوّن runtime، لا تحذفه كمتصفح.
- Firefox 159.0.1 (x64 ar)؛ بيانات `%APPDATA%\\Mozilla\\Firefox` نحو 0.18 GB.
- Vivaldi جُرّب، ولم يظهر خيار واجهة عربية؛ قرر المستخدم إزالته. لم يتأكد توثيقياً فحص ما بعد الإزالة.
- Brave ثُبّت؛ العربية أضيفت عبر `brave://settings/languages` واختيار Display Brave in this language ثم Relaunch. المستخدم أكد أن واجهة Brave أصبحت عربية.
- Brave المرشح للاعتماد؛ لا تزال بياناته/حجمه واختبار المواقع والإضافات غير مجرودة.
- المستخدم قرر: **حذف Firefox والاعتماد على Brave**. لم يؤكد حذف Firefox بعد.
- لا يوجد دليل على إزالة Chrome أو Edge؛ لا تحذف أيّاً منهما حالياً.

### الخطوة التالية المباشرة: إرشاد المستخدم لحذف Firefox
1. أغلق Firefox.
2. Windows Settings > Apps > Apps & features.
3. ابحث عن Mozilla Firefox (x64 ar) > Uninstall.
4. أكمل معالج Firefox: Next > Uninstall > Finish.
5. لا تختَر حذف بيانات Firefox/Profile إذا كان الخيار موجوداً؛ الهدف إزالة البرنامج فقط والمحافظة على البيانات حتى التحقق. لا تحذف `%APPDATA%\\Mozilla\\Firefox` يدويًا.
6. بعد التنفيذ، اطلب تأكيد المستخدم، ثم فحص قراءة فقط: هل Firefox ما زال في قائمة البرامج؟ هل توجد عملية firefox؟ وقياس المساحة الحرة C.
7. وثّق نتيجة الإزالة الفعلية، المساحة التي تغيرت (لا تنسب كل الفرق للبرنامج دون مقارنة)، وما إذا بقي profile. حدّث SYSTEM-PROFILE.

مرجع Mozilla الرسمي للإزالة: https://support.mozilla.org/en-US/kb/uninstall-firefox-from-your-computer

## خطة المتصفحات بعد إزالة Firefox
- Brave: متصفح أساسي مرشح؛ Arabic UI confirmed.
- Chrome: احتفظ به مؤقتاً للمقارنة/التوافق، وبياناته الكبيرة 2.76GB؛ لا حذف أو تنظيف دون مراجعة profile.
- Edge: احتفظ به مؤقتاً؛ بيانات 0.75GB؛ لا حذف.
- WebView2 Runtime: احتفظ به.
- لا نضيف متصفحات أو extensions كثيرة قبل اختبار Brave.
- بعد إزالة Firefox: اختبار Brave مع GitHub وChatGPT وNotion وArena، أدوات DevTools، الإضافات، الأداء والذاكرة، وتحقق التحديثات.
- لا تثبت إضافات من مصادر مجهولة ولا تمنح extensions tokens أو صلاحيات واسعة بلا مراجعة.
- أولوية المستخدم للمتصفح: شامل (واجهة، مزايا، تطوير، خصوصية)، لا يشترط open-source، وتصميم modern. شرط واجهة العربية مهم؛ Vivaldi استُبعد بسبب غياب العربية في النسخة التي جُربت.

## جرد البرامج/المساحة والملاحظات الأخرى
- C: كان محدود المساحة (حوالي 13.36 GB free في قياس سابق)، ثم بعد حذف Codex زاد إلى 15.48 GB عشري وفق قياس 2026-11-09؛ لا ننظف عشوائياً.
- Docker Desktop data نحو 9.61GB، Docker مغلق وقت فحص سابق، لا prune أو حذف VHDX.
- npm cache نحو 1.395GB؛ لا تنظيف دون قرار.
- Adobe ARM نحو 1.002GB، ثلاثة ملفات tmp كبيرة؛ لا حذف قبل تحقق.
- Codex وبياناته المحلية حُذفت بموافقة المستخدم بتاريخ 2026-11-09: `%LOCALAPPDATA%\\OpenAI\\Codex` و`%USERPROFILE%\\.codex`; لا تحذف parent OpenAI أو منتجات أخرى.
- Chrome User Data نحو 2.78GiB، Profiles 3 و5، Service Worker/CacheStorage كبيرة؛ لم يُنظف أي شيء.
- Spotify site data حُذف من Chrome بواسطة المستخدم في 2026-11-09؛ لم يُقَس reclaim.
- Windows Update: NoVirusThanks Win Update Stop v1.4 موجود، خدمة WinUpdStopSvc Automatic/LocalSystem. الوثائق المرفقة بالبرنامج تؤكد أنه يعطّل تحديثات Windows ويعيد تعطيلها تلقائياً. المستخدم وافق سابقاً على استئناف التحديثات، لكن لا يوجد توثيق أن البرنامج أزيل أو أن التحديثات اكتملت. لا تغيّر service أو uninstall دون موافقة منفصلة.
- Windows Update بحث يدوي سابق نجح؛ أخطاء متقطعة مسجلة. لا تعتبر التحديثات مكتملة.

## خارطة العمل
1. إنهاء خطوة حذف Firefox والتحقق وتوثيقها.
2. جرد Brave (version، الحجم، profile/data، language، update state) وتهيئته.
3. مراجعة extensions المرشحة؛ تثبيت تدريجي، ابدأ Refined GitHub بعد فحص المصدر والصلاحيات، ثم React DevTools إذا كان React development يحتاجه.
4. اختبار Brave على مواقع المستخدم ومهام التطوير.
5. مراجعة قرار Chrome/Edge لاحقاً بناء على توافق وبيانات وأداء، دون إزالة تلقائية.
6. استكمال Software Inventory وبقية مراحل الجهاز وفق SYSTEM-PROFILE.

## آخر مزامنة GitHub
- `docs/system/SYSTEM-PROFILE.md` أُضيف إليه قسم مراجعة المتصفحات واعتماد Brave بتاريخ 2026-11-20.
- Commit: `a6486a455e1d0a558a4e6aef044e2b109281ced5`.
- هذا الملف نفسه هو handoff الجديد، ويُنشأ على `main`.


## متابعة المحادثة الجديدة — 2026-11-20
- المستخدم أرسل نص أمر التحقق من إزالة Firefox، لكن لم يتضمن ناتج التنفيذ. لا تعتبر Firefox removed أو مساحة C محدّثة حتى يصل الناتج.
- إذا لم تتم الإزالة بعد: أغلق Firefox ثم Windows Settings > Apps > Apps & features > Mozilla Firefox (x64 ar) > Uninstall. لا تحدد حذف بيانات المستخدم/Profile ولا تحذف مجلد Mozilla يدوياً.
- بعد الإزالة، اطلب ناتج فحص Registry/process/Free C من الأمر السابق؛ تحقق من Installed=False وRunning=False، ووثّق مساحة C الحالية. لا تنسب كامل تغير المساحة إلى Firefox.
- Brave: مثبت، واجهة العربية مؤكدة عملياً، وهو المتصفح المرشح الأساسي. لم يُجرَ بعد اختبار مواقع GitHub/ChatGPT/Notion/Arena أو جرد الإضافات والحجم/الذاكرة.
- لا تُزل Chrome أو Edge، ولا Edge WebView2 Runtime. بيانات Chrome وEdge ما زالت غير مفحوصة للحذف.

## أحدث تحديث للحالة — 2026-11-20

هذا التحديث يتقدم على أي تعليمات أقدم داخل هذا الملف إذا تعارضت معه:

- Firefox: لا يظهر في سجلات Uninstall أو العمليات في فحص 2026-11-20، لكن مجلد بيانات Firefox الشخصي `%APPDATA%\\Mozilla\\Firefox` ما زال موجوداً. لا تحذفه.
- Vivaldi: لا يظهر في سجلات Uninstall، ومسارات تثبيته المعتادة التي فُحصت غير موجودة، ولا تظهر عملية Vivaldi. الإزالة مرجحة بقوة ضمن نطاق الفحص.
- Brave 158.1.100.58 مثبت بواجهة عربية؛ المستخدم أكد نجاح اختبارات مواقع العمل وDevTools، وطلب تجاوز التجهيز. لا تثبت إضافات دون طلب منفصل.
- Chrome 156.0.8078.82 وEdge 152.0.4191.66 باقيان مثبتين بحسب الجرد. Edge WebView2 Runtime 152.0.4191.66 يجب الإبقاء عليه.
- C: آخر قياس 12.85 GiB حرة من 108.45 GiB إجماليًا.
- تمت قراءة ملفات المستودع الثلاثة كاملة من `main`. شجرة المستودع تتضمن وثائق Markdown فقط، دون سكربتات أو ملفات إعداد قابلة للتنفيذ.
- أولوية المساحة التاريخية من الجرد: Docker VHDX 9.505 GB؛ Chrome User Data 2.78 GiB؛ npm-cache 1.395 GB؛ Adobe ARM نحو 1.002 GB. كل هذه قياسات قديمة من 2026-11-09 وتحتاج إعادة فحص قبل أي إجراء. Docker كان مغلقاً، ومحركه غير متاح وقت الفحص.
- ملف `SYSTEM-PROFILE.md` هو المرجع التفصيلي الأساسي؛ `HANDOFF-2026-11-20.md` أحدث من هذا الملف وكان متضمناً فحص إزالة المتصفحات قبل نجاح Brave. استخدم التحديثات اللاحقة في الملفات الثلاثة عند وجود تعارض مع النص التاريخي القديم.


## أحدث تحديث — Windows Update وNoVirusThanks (2026-11-20)

هذا القسم يتقدم على الملاحظات القديمة داخل الملف التي تفيد بأن اكتمال تثبيت التحديثات لم يتأكد:

- المستخدم أفاد الآن بأن تحديثات Windows اكتملت. يُسجل ذلك كإفادة المستخدم؛ لم يصل ناتج Get-HotFix منفصل.
- الخدمات حسب آخر مخرجات PowerShell: BITS Running/Automatic؛ CryptSvc Running/Automatic؛ wuauserv Running/Manual؛ WinUpdStopSvc Running/Automatic.
- WinUpdStopSvc يعمل تلقائياً من: `C:\Program Files\NoVirusThanks\Win Update Stop\WinUpdStopSvc.exe`.
- Authenticode Status = Valid، Signer = NoVirusThanks Company Srl (support@novirusthanks.org).
- وفق FAQ الرسمي، يبقي البرنامج خدمته لتعيد تعطيل Windows Updates تلقائياً إذا أعاد Windows تفعيلها بعد reboot أو مرور الوقت؛ ويمكن إعادة التفعيل من واجهة البرنامج باختيار Enable: https://www.winupdatestop.com/faqs/
- واجهة البرنامج لم تُفحص بعد، لذلك لا نعرف هل حالته الحالية Enabled أم Disabled.
- لا توجد تغييرات على الجهاز. الخطوة التالية قراءة الحالة من واجهة البرنامج فقط دون الضغط على Enable/Disable. أي تغيير أو إزالة يحتاج موافقة المستخدم.


## أحدث تحديث — حالة واجهة NoVirusThanks (2026-11-20)

هذا القسم يتقدم على تحذير التسليم السابق الذي اعتبر استمرار التحديثات التلقائية غير محسوم بسبب بقاء الخدمة:

- لقطة الشاشة التي أرسلها المستخدم من NoVirusThanks Win Update Stop v1.4 تعرض العبارة الخضراء **Windows Updates are enabled**.
- حالة البرنامج المعروضة الآن: Enabled. لم يتم الضغط على أي زر في الواجهة.
- خدمة WinUpdStopSvc لا تزال Running/Automatic حسب PowerShell، لكن وجودها وتشغيلها لا يعنيان أنها تعطل التحديثات في الوضع الحالي. FAQ البرنامج يوضح أن الخدمة تعيد فرض التعطيل إذا كان المستخدم قد اختار Disable ثم أعاد Windows تفعيل التحديثات: https://www.winupdatestop.com/faqs/
- لا حاجة لإيقاف الخدمة أو إزالة البرنامج بسبب حالتها وحدها؛ لا يوجد دليل في الصورة على تعطيل التحديثات حالياً.
- يمكن لاحقاً قراءة حالة Windows Update من إعدادات Windows كتحقق مستقل، دون تغيير أي إعداد.
- لم تُجرَ أي تغييرات على الجهاز.
