CAPOSAT Car Android - بناء APK من GitHub بدون Android Studio
============================================================

هذه النسخة فيها GitHub Actions جاهز يبني لك APK و AAB من GitHub.
لا تحتاج Android Studio في جهازك.

المهم:
- APK للتجربة على الهاتف.
- AAB هو المطلوب لاحقاً للرفع على Google Play.
- ملف AAB في هذه المرحلة unsigned للتجربة فقط؛ للرفع النهائي على Google Play سنضيف التوقيع لاحقاً بمفتاح رسمي.

الخطوات:

1) افتح GitHub.
2) أنشئ Repository جديد باسم:
   caposat-car-android

3) افتح ملف ZIP هذا وفك الضغط.
4) ارفع كل محتويات المجلد إلى GitHub، وليس المجلد الفارغ فقط.
   يجب أن تظهر في GitHub الملفات مثل:
   app/
   build.gradle
   settings.gradle
   .github/workflows/build-android.yml

5) بعد رفع الملفات، افتح في GitHub تبويب:
   Actions

6) ستجد Workflow باسم:
   Build CAPOSAT Car Android

7) اضغط عليه ثم اضغط:
   Run workflow

8) انتظر حتى ينتهي. إذا أصبح أخضر يعني نجح.

9) افتح آخر عملية Build، انزل إلى الأسفل إلى Artifacts.

10) حمّل:
    CAPOSAT-Car-debug-APK

11) فك الضغط عن artifact، ستجد ملف APK.
    أرسله إلى هاتفك وثبته للتجربة.

ملاحظات مهمة:
- إذا ظهر تحذير في الهاتف عند تثبيت APK، اختر السماح بالتثبيت من مصدر غير معروف.
- زر الرجوع داخل التطبيق تم ضبطه: يرجع داخل صفحات التطبيق، ولا يخرج مباشرة إلا إذا كنت في الصفحة الرئيسية.
- رابط الموقع داخل التطبيق هو:
  https://caposat-car.pages.dev

للنشر على Google Play:
- نحتاج لاحقاً إنشاء مفتاح توقيع Keystore.
- نضيف أسرار التوقيع في GitHub Secrets.
- بعدها GitHub Actions يعطيك AAB موقّع جاهز للرفع على Play Console.
