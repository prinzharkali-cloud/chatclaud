ChatClaud — ТВОИ файлы + GitHub Pages + Render

ЭТОТ ZIP = твой рабочий index.html (чат, картинки, спираль, Thinking).
Не лендинг. Не упрощённая версия.

1) Render (ключи)
   Environment Variables из ENV-KEYS.txt (значения ключей только там).
   Сервис должен быть Live (не Suspended).

2) index.html — строка CC_API_BASE
   Поставь URL своего Render:
   https://ТВОЙ-СЕРВИС.onrender.com
   (без слэша в конце)

   Или в консоли Safari:
   localStorage.setItem('CC_API_BASE','https://ТВОЙ-СЕРВИС.onrender.com'); location.reload();

3) GitHub Pages — залей:
   index.html
   sw.js
   manifest.json
   icon-192.png
   icon-512.png
   chatclaud-avatar-transparent.png
   google9da876d4cf2a261c.html

   НЕ заливай ENV-KEYS с заполненными секретами в public repo.

4) Иконка на «Домой»
   Должна быть спираль (icon-192 / icon-512), не буква C.
   Если буква C — старый кэш: удали ярлык с Домой, залей заново, добавь снова.

5) Если открывается «О ChatClaud» текст без чата
   На GitHub лежит не тот index.html — замени этим из ZIP.

server.js + package.json — только на Render, не обязательно на Pages.
