# ڕێکخستنی هاوکاتکردن (تەنها یەکجار، ~٥ خولەک)

1. بڕۆ بۆ https://console.firebase.google.com ← **Add project** (Analytics پێویست نییە).
2. **Build → Realtime Database → Create database** (هەر شوێنێک) ← Start in locked mode.
3. تابی **Rules** بکەرەوە و ئەمە دابنێ (ئیمەیڵەکەت بنووسە)، پاشان Publish:
```
{ "rules": { ".read": true, ".write": "auth != null && auth.token.email === 'EMAIL_ی_تۆ@gmail.com'" } }
```
   واتە هەموو کەس دەتوانێت بیبینێت، تەنها تۆ دەتوانیت زیاد/دەستکاری بکەیت.
4. **Build → Authentication → Get started → Email/Password → Enable**، پاشان تابی Users ← **Add user** (هەمان ئیمەیڵ + وشەی نهێنی).
5. **Project settings (⚙) → General → Web API Key** کۆپی بکە. URLی داتابەیسیش لە Realtime Database دایە (https://….firebasedatabase.app).
6. لە کۆتایی index.html بگەڕێ بۆ `const CLOUD = {` و `dbUrl` و `apiKey` پڕبکەرەوە.
7. فایلەکان دووبارە بارکە (upload) بۆ هۆستەکەت.

بەکارهێنان: ڕێکخستنەکان (Settings) ← Admin ← چوونەژوورەوە ← هاب یان بانک/ژمارە زیاد بکە. هەموو بەکارهێنەران لە ≤٣٠ چرکەدا دەیبینن (یان کاتێک ئەپەکە دەکەنەوە).
