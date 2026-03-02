---
marp: true
theme: default
paginate: true
style: |
  section {
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    background: #ffffff;
  }
  section.lead {
    display: flex;
    flex-direction: column;
    justify-content: center;
    text-align: center;
    background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
    color: white;
  }
  section.lead h1, section.lead h2, section.lead p {
    color: white;
  }
  h1 { color: #2d3436; }
  h2 { color: #6c5ce7; }
  h3 { color: #00b894; }
  blockquote { border-left: 4px solid #6c5ce7; background: #f8f9fa; padding: 10px 20px; }
  table { font-size: 0.85em; }
  code { background: #f1f2f6; padding: 2px 6px; border-radius: 4px; color: #e17055; }
---

# Шаблон презентації (Робототехніка, micro:bit, MakeCode)

## Формат: Marp (Markdown Presentations)

Файл — це звичайний Markdown з front-matter блоком `marp: true` на початку.
Кожен слайд розділяється рядком `---`.

**Конвертація в HTML:** запусти `./build_presentations.sh` з кореня проєкту.
Результат — .html файл, який відкривається в браузері. Стрілки ← → для навігації.

---

## Правила створення презентації:

### Структура:
1. Front-matter блок `---` з `marp: true` та стилями — **ОБОВ'ЯЗКОВО** (копіювати з цього шаблону)
2. Перший слайд — титульний з `<!-- _class: lead -->` (градієнтний фон)
3. Далі — слайди з контентом, розділені `---`
4. Останній слайд — підсумки + самостійна робота

### Оформлення:
- **Колірна схема робототехніки:** фіолетовий градієнт (#667eea → #764ba2) для титульного
- Максимум **5-7 слайдів** (не рахуючи титульний)
- Мінімум тексту — великі заголовки, короткі пункти
- Використовуй `>` для блоків-підказок
- Таблиці для порівнянь (блоки MakeCode тощо)
- НЕ писати "Слайд 1", "Слайд 2" — Marp сам нумерує

### Приклад слайду:

```
---

<!-- _class: lead -->

# Робототехніка | Урок [НОМЕР]
## [НАЗВА ТЕМИ]
**[ДАТА] | Група: [ГРУПА]**

---

## 🆕 [Що нового]

- [Пояснення]
- [Приклад]

> 💡 Підказка

---

## Підсумки

- ✅ [Що вивчили]
- ✅ [Що вивчили]

### 🏠 Самостійна робота:
- [Завдання]
```
