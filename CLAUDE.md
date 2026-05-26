This project uses AGENTS.md as the source of truth for AI assistant behavior.

See ./AGENTS.md for full instructions on how to assist with this challenge.

---
description: Базовые правила учебного FrontEnd-проекта
alwaysApply: true
---

- Before we begin, tell me how you'll verify everything was done correctly? Ask clarifying questions if necessary.

# Стек проекта

- HTML5 (семантическая вёрстка)
- CSS3 (чистый CSS, без препроцессоров пока, Flexbox, Grid basics)
- Vanilla JavaScript (ES6+, без фреймворков)

# Структура файлов

Придерживайся такой структуры:
/project
├── index.html # главная страница
├── /css
│ └── style.css # все стили
├── /js
│ └── script.js # весь JavaScript
└── /images # картинки

# HTML-правила

- Используй семантические теги: `<header>`, `<main>`, `<section>`, `<footer>`,
  `<nav>`, `<article>`. Не злоупотребляй `<div>`.
- Каждому изображению — обязательный атрибут alt.
- Для форм используй правильные type: email, tel, number.
- Пиши понятные id и class в kebab-case (например: user-profile).

# CSS-правила

- Именование классов — в стиле BEM или просто kebab-case.
  Пример BEM: .card, .card__title, .card--active
- Никогда не используй !important без крайней необходимости.
  Если использовал — оставь комментарий ПОЧЕМУ.
- Не используй #id для стилизации — только .class.
- Мобильная вёрстка (mobile-first): сначала стили для телефона,
  потом через @media (min-width: ...) — для десктопа.
- Используй CSS-переменные для повторяющихся цветов и размеров:
  :root { --main-color: #3498db; }

# JavaScript-правила

- const по умолчанию, let — только если значение меняется. var — НИКОГДА.
- Обработчики событий именуй с префиксом handle:
  handleClick, handleSubmit, handleInput.
- Ранний return вместо вложенных if:
  // Плохо:
  if (user) { if (user.age > 18) { ... } }
  // Хорошо:
  if (!user) return;
  if (user.age <= 18) return;
  ...
- Всегда проверяй, существует ли элемент, перед тем как с ним работать:
  const btn = document.querySelector('.btn');
  if (!btn) return;

# Доступность (accessibility)

- Все интерактивные элементы должны быть доступны с клавиатуры.
- Кнопки — это `<button>`, ссылки — это `<a>`. Не наоборот.
- Контраст текста и фона — достаточный для чтения.

# Сохрани и запомни

- Ты код не пишешь, код пишу только я.
- Ты создаешь план, я его воплащаю сам, пишу сам, учусь лучшим практикам.
- Ты даешь рекомендации и советы.
- Style guide: ./style-guide.md
- У нас три версии: mobile, tablet, desktop
