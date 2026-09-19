ChatClaud — сайт на GitHub Pages + ключи на Render
================================================

СХЕМА
  Браузер → GitHub Pages (index.html, иконки, PWA)
         → Render (server.js + Environment Variables с ключами)

КЛЮЧИ
  Не клади ENV-KEYS.txt и ключи в GitHub.
  Ключи остаются только в Render → Environment.

ШАГ 1. Render должен быть ONLINE
  Если "This service has been suspended" — чат с GitHub не заработает,
  пока Render снова не запустится (новый аккаунт / снятие лимита).

ШАГ 2. URL API в index.html
  В начале страницы (в <head>) найди:
    window.CC_API_BASE = ... 'https://chatclaud.onrender.com'
  Замени на СВОЙ адрес Render, например:
    https://твой-сервис.onrender.com
  Без / в конце.

  Или в консоли браузера один раз:
    localStorage.setItem('CC_API_BASE', 'https://твой-сервис.onrender.com');
    location.reload();

ШАГ 3. GitHub Pages
  1) Создай репозиторий (можно public)
  2) Залей ТОЛЬКО фронт:
       index.html
       sw.js
       manifest.json
       icon-192.png
       icon-512.png
       google....html (если нужен Search Console)
  3) НЕ заливай server.js с ключами (в этом zip server.js без секретов —
     но бэкенд должен жить на Render, не на Pages)
  4) Settings → Pages → Deploy from branch → main / root (или /docs)
  5) Открой https://НИК.github.io/РЕПО/

ШАГ 4. Проверка
  - Сайт открывается с GitHub
  - В Network запросы идут на *.onrender.com/api/chat
  - Если CORS: в server.js уже Access-Control-Allow-Origin: *

server.js и package.json в zip — для Render (деплой бэкенда), не для Pages.
