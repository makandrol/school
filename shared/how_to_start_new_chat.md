# Інструкція для нового чату (агента)

## Як почати роботу в новому чаті Cursor

Коли потрібно створити новий урок, відкрий новий чат і напиши приблизно так:

---

### Для робототехніки (група 5-АБ):
```
Прочитай файли:
- @shared/context.md
- @robotics/group_5ab/curriculum.md
- summary.md останнього уроку в robotics/group_5ab/
- @shared/templates/presentation_robotics.html
- @shared/templates/google_classroom_robotics.md

Створи наступний урок за планом. Зроби:
1. plan.md — план уроку
2. presentation.html — презентацію (самодостатній HTML, навігація стрілками)
3. google_classroom.md — текст для Google Classroom
4. summary.md
```

### Для робототехніки (група 5-ВГ):
```
Прочитай файли:
- @shared/context.md
- @robotics/group_5cd/curriculum.md
- summary.md останнього уроку в robotics/group_5cd/
- @shared/templates/presentation_robotics.html
- @shared/templates/google_classroom_robotics.md

Створи наступний урок. Зроби:
1. plan.md — план уроку
2. presentation.html — презентацію (самодостатній HTML, навігація стрілками)
3. google_classroom.md — текст для Google Classroom
4. summary.md
```

### Для 3D-моделювання (група 3-4 клас):
```
Прочитай файли:
- @shared/context.md
- @3d/group_34/curriculum.md
- summary.md останнього заняття в 3d/group_34/
- @shared/templates/presentation_3d.html
- @shared/templates/handout_3d.html

Створи наступне заняття (3 уроки). Зроби:
1. plan.md — план заняття
2. presentation.html — презентацію (самодостатній HTML)
3. handout.html — роздатковий матеріал для друку (HTML з SVG-картинками, page-break між завданнями)
4. summary.md
```

### Для 3D-моделювання (група 5-7 клас):
```
Прочитай файли:
- @shared/context.md
- @3d/group_57/curriculum.md
- summary.md останнього заняття в 3d/group_57/
- @shared/templates/presentation_3d.html
- @shared/templates/handout_3d.html

Створи наступне заняття (3 уроки). Зроби:
1. plan.md — план заняття
2. presentation.html — презентацію (самодостатній HTML)
3. handout.html — роздатковий матеріал для друку (HTML з SVG-картинками, page-break між завданнями)
4. summary.md
```

---

## Після створення уроку — не забудь попросити:
1. Оновити `curriculum.md` — поставити ✅ навпроти пройденого уроку
2. Перевірити що `summary.md` створений в папці уроку — щоб наступний агент знав контекст

## Файли, які створюються для кожного уроку

### Робототехніка:
| Файл | Опис |
|------|------|
| `plan.md` | План уроку (хід уроку, мета, блоки MakeCode) |
| `presentation.html` | Презентація — відкрити в браузері, стрілки ← → |
| `google_classroom.md` | Текст для публікації в Google Classroom |
| `summary.md` | Короткий підсумок (для контексту наступного агента) |

### 3D-моделювання:
| Файл | Опис |
|------|------|
| `plan.md` | План заняття (3 уроки, хід, мета) |
| `presentation.html` | Презентація — відкрити в браузері, стрілки ← → |
| `handout.html` | Роздатковий матеріал — відкрити в браузері → Cmd+P друк |
| `summary.md` | Короткий підсумок (для контексту наступного агента) |

## Шаблони
Шаблони лежать в `shared/templates/`:
- `lesson_plan_robotics.md` — план уроку для робототехніки
- `lesson_plan_3d.md` — план заняття для 3D-моделювання
- `presentation_robotics.html` — HTML-презентація (фіолетова тема)
- `presentation_3d.html` — HTML-презентація (зелена тема)
- `handout_3d.html` — HTML роздатковий матеріал з SVG-картинками
- `google_classroom_robotics.md` — текст для Google Classroom

## Формати файлів
- **plan.md, summary.md, curriculum.md, google_classroom.md** — залишаються Markdown (тільки для читання агентом та копіювання тексту)
- **presentation.html** — самодостатній HTML, відкривається в браузері як слайд-шоу
- **handout.html** — самодостатній HTML, друкується через Cmd+P з правильними розривами сторінок та SVG-ілюстраціями
