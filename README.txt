FIX: ccApiUrl + иконки спираль

1. Залей ВСЕ файлы в chatclaud.github.io (не только index.html):
   index.html, icon-192.png, icon-512.png, chatclaud-avatar-transparent.png,
   manifest.json, sw.js

2. В начале index.html CC_API_BASE = URL твоего бэкенда (Render/Replit)
   Или в консоли:
   localStorage.setItem('CC_API_BASE','https://ТВОЙ-БЭКЕНД'); location.reload();

3. Иконка «C» → удали ярлык с Домой, залей icon-192/512, добавь снова.

4. Ошибка ccApiUrl исправлена: функция всегда window.ccApiUrl.
