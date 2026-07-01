CAPOSAT Car Android WebView v1
================================

هذا مشروع Android Studio لتطبيق سيارة CAPOSAT.
التطبيق يفتح الرابط:
https://caposat-car.pages.dev

المهم: زر الرجوع في الهاتف يعمل داخل التطبيق:
- إذا كنت داخل صفحة داخلية أو نافذة/تنقل داخل الموقع، يرجع للخلف داخل WebView.
- إذا لا يوجد رجوع، يرجع إلى الصفحة الرئيسية.
- إذا أنت أصلاً في الرئيسية، يخرج من التطبيق.

الخطوات:
1) افتح Android Studio.
2) File > Open.
3) اختر مجلد caposat-car-android-webview-v1.
4) انتظر Gradle Sync.
5) للتجربة: Build > Build Bundle(s) / APK(s) > Build APK(s).
6) للرفع على Google Play: Build > Generate Signed Bundle / APK > Android App Bundle.

Package name:
com.caposat.car

اسم التطبيق:
سيارة CAPOSAT

صلاحيات التطبيق:
- Internet
- Location للموقع من Maps
- Camera اختياري لو احتجنا لاحقاً رفع صورة

إذا أردت تغيير رابط الموقع:
افتح الملف:
app/src/main/java/com/caposat/car/MainActivity.java
وغيّر HOME_URL.
