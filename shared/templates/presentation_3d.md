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
    background: linear-gradient(135deg, #00b894 0%, #00cec9 100%);
    color: white;
  }
  section.lead h1, section.lead h2, section.lead p {
    color: white;
  }
  h1 { color: #2d3436; }
  h2 { color: #00b894; }
  h3 { color: #6c5ce7; }
  blockquote { border-left: 4px solid #00b894; background: #f8f9fa; padding: 10px 20px; }
  table { font-size: 0.85em; }
  code { background: #f1f2f6; padding: 2px 6px; border-radius: 4px; color: #e17055; }
---

# Шаблон презентації (3D-моделювання, Tinkercad)

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
4. Останній слайд — підсумки

### Оформлення:
- **Колірна схема 3D:** зелений градієнт (#00b894 → #00cec9) для титульного
- Максимум **5-7 слайдів** (не рахуючи титульний)
- Для 3-4 класу: дуже прості слова, мало тексту
- Для 5-7 класу: можна трохи складніше
- Використовуй `>` для блоків-підказок
- НЕ писати "Слайд 1", "Слайд 2"
- Детальна інструкція — в handout.md, не в презентації

### Приклад слайду:

```
---

<!-- _class: lead -->

# 3D-моделювання | Заняття [НОМЕР]
## [НАЗВА ТЕМИ]
**[ДАТА] | Група: [ГРУПА]**

---

## 🆕 [Що нового]

- [Пояснення]

> 💡 Підказка

---

## Підсумки

- ✅ [Що навчились]
```
