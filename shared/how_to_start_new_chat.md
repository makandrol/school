# Інструкція для нового чату (агента)

## Як почати роботу в новому чаті Cursor

Коли потрібно створити новий урок, відкрий новий чат і вставте промпт нижче.

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
5. Додай урок в manifest.json (published: true, files: ["presentation.html", "google_classroom.md"])
6. Онови curriculum.md
7. Закоміть в гілку preview і запуш (git checkout preview && git add . && git commit && git push)

Після пушу — скинь мені preview URL: https://preview--makarevych-school.netlify.app/
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
5. Додай урок в manifest.json (published: true, files: ["presentation.html", "google_classroom.md"])
6. Онови curriculum.md
7. Закоміть в гілку preview і запуш

Після пушу — скинь мені preview URL: https://preview--makarevych-school.netlify.app/
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
5. Додай урок в manifest.json (published: true, files: ["presentation.html", "handout.html"])
6. Онови curriculum.md
7. Закоміть в гілку preview і запуш

Після пушу — скинь мені preview URL: https://preview--makarevych-school.netlify.app/
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
5. Додай урок в manifest.json (published: true, files: ["presentation.html", "handout.html"])
6. Онови curriculum.md
7. Закоміть в гілку preview і запуш

Після пушу — скинь мені preview URL: https://preview--makarevych-school.netlify.app/
```

---

## Після перевірки preview — мержимо в прод:
```
Все ок, мержни в main:
git checkout main && git merge preview && git push && git checkout preview
```

---

## Після створення уроку — чекліст:
1. ✅ `plan.md` створений
2. ✅ `presentation.html` створений
3. ✅ `google_classroom.md` (робототехніка) або `handout.html` (3D) створений
4. ✅ `summary.md` створений
5. ✅ `curriculum.md` оновлений
6. ✅ `manifest.json` оновлений (урок додано з `published: true`)
7. ✅ Зміни закомічені в гілку `preview` і запушені
8. ✅ Preview URL надісланий вчителю для перевірки

## Файли, які створюються для кожного уроку

### Робототехніка:
| Файл | Опис | На сайті? |
|------|------|-----------|
| `plan.md` | План уроку (хід уроку, мета, блоки MakeCode) | ❌ |
| `presentation.html` | Презентація — відкрити в браузері, стрілки ← → | ✅ |
| `google_classroom.md` | Текст для публікації в Google Classroom | ✅ (в деталях уроку) |
| `summary.md` | Короткий підсумок (для контексту наступного агента) | ❌ |

### 3D-моделювання:
| Файл | Опис | На сайті? |
|------|------|-----------|
| `plan.md` | План заняття (3 уроки, хід, мета) | ❌ |
| `presentation.html` | Презентація — відкрити в браузері, стрілки ← → | ✅ |
| `handout.html` | Роздатковий матеріал — відкрити в браузері → Cmd+P друк | ✅ |
| `summary.md` | Короткий підсумок (для контексту наступного агента) | ❌ |

## Шаблони
Шаблони лежать в `shared/templates/`:
- `lesson_plan_robotics.md` — план уроку для робототехніки
- `lesson_plan_3d.md` — план заняття для 3D-моделювання
- `presentation_robotics.html` — HTML-презентація (фіолетова тема)
- `presentation_3d.html` — HTML-презентація (зелена тема)
- `handout_3d.html` — HTML роздатковий матеріал з SVG-картинками
- `google_classroom_robotics.md` — текст для Google Classroom
