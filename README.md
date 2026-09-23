# مِيزان — Android APK

هذا المشروع عبارة عن تطبيق «ميزان» مبني بواجهة ويب متجاوبة ومهيأ للعمل كتطبيق Android باستخدام Capacitor 6.

## بناء APK على Windows

### 1) المتطلبات
- Node.js LTS
- Android Studio
- Android SDK Platform 35 أو أحدث
- Android SDK Build-Tools

### 2) تثبيت الحزم
افتح CMD داخل مجلد المشروع:

```bash
npm install
```

### 3) إنشاء مشروع Android
```bash
npx cap add android
npx cap sync android
```

إذا كان مجلد `android` موجودًا مسبقًا، استخدم:

```bash
npx cap sync android
```

### 4) فتح Android Studio
```bash
npx cap open android
```

ثم من Android Studio:
**Build → Generate App Bundle(s) / APK(s) → Generate APK(s)**

ملف APK التجريبي سيظهر عادة في:

```text
android/app/build/outputs/apk/debug/app-debug.apk
```

## APK موقّع للنشر
استخدم:
**Build → Generate Signed Bundle / APK**

واختر **APK**، ثم أنشئ keystore خاصًا بالتطبيق واحفظه في مكان آمن.

## الهوية
- اسم التطبيق: مِيزان
- App ID: `com.mizan.app`
- اللون الأساسي: `#C9A86A`
- الخلفية: `#070B13`
- أيقونة أولية موجودة في: `resources/icon.svg`

## بعد أي تعديل على الموقع
```bash
npx cap sync android
```
ثم أعد بناء APK.
