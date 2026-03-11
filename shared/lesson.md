# Промпт для створення уроку

Ти — AI-асистент. Вчитель просить тебе створити наступний урок для вказаної групи, додати його на сайт і запушити для перевірки.

---

## Крок 1. Визнач групу

Вчитель вкаже одне з:

| Ідентифікатор | Папка | Тип | Шаблони |
|--------------|-------|-----|---------|
| **роботи 5а** / **5аб** | `robotics/group_5ab/` | robotics | `presentation_robotics.html`, `google_classroom_robotics.md` |
| **роботи 5в** / **5вг** | `robotics/group_5cd/` | robotics | `presentation_robotics.html`, `google_classroom_robotics.md` |
| **3д 3-4** | `3d/group_34/` | modeling | `presentation_3d.html`, `handout_3d.html` |
| **3д 5-7** | `3d/group_57/` | modeling | `presentation_3d.html`, `handout_3d.html` |

## Крок 2. Прочитай контекст

Прочитай **обов'язково** (у такому порядку):
1. `shared/context.md` — загальний контекст, правила, формати, сайт, git
2. `<папка_групи>/curriculum.md` — курикулум (що пройдено, що далі)
3. **ВСІ `summary.md`** файли в підпапках `lesson-*/` цієї групи — повний контекст пройдених уроків
4. Відповідні шаблони з `shared/templates/` (див. таблицю вище)

## Крок 3. Створи файли уроку

Визнач номер наступного уроку (N+1 від останнього). Створи папку `lesson-XX/`.

**Для робототехніки** (3 файли):
- `presentation.html` — презентація (самодостатній HTML, стрілки ← →, фіолетова тема)
- `google_classroom.md` — текст для Google Classroom
- `summary.md` — підсумок для наступного агента

**Для 3D-моделювання** (3 файли):
- `presentation.html` — презентація (самодостатній HTML, зелена тема)
- `handout.html` — роздатковий для друку (HTML з SVG-картинками, A4, page-break між завданнями)
- `summary.md` — підсумок для наступного агента

## Крок 4. Онови manifest.json

Додай урок в масив `lessons` відповідної групи:

```json
{
  "n": <номер>, "title": "<емодзі> <назва>", "date": "<дд.мм.рррр>",
  "published": true,
  "files": ["presentation.html", "google_classroom.md"],
  "makecode": [{"label": "<назва проєкту>", "url": ""}]
}
```

Для 3D замість `google_classroom.md` → `handout.html`, замість `makecode` → `tinkercad`.
URL проєктів залишай порожніми (`"url": ""`).

## Крок 5. Онови curriculum.md

Зазнач що урок створений.

## Крок 6. Закоміть і запуш в preview

```bash
cd /Users/andrii.makarevych/squad/school
git checkout preview
git add .
git commit -m "Lesson <номер>: <назва>"
git push
```

⚠️ Remote використовує SSH host `github-school`: `origin git@github-school:makandrol/school.git`

## Крок 7. Скинь preview URL

Напиши вчителю:
```
Готово! Перевір: https://preview--makarevych-school.netlify.app/
```

---

## Додаткові вказівки

- **Мова:** українська
- **Робототехніка:** описуй все через MakeCode блоки (не pseudocode, не JavaScript)
- **Для 3-4 класу:** прості слова, багато візуальних описів
- **Для 5+ класу:** можна складніші терміни, але з поясненнями
- Якщо вчитель вказав конкретну тему — використай її. Якщо ні — обери тему за курикулумом
- Кожен урок починається з нагадування БЖД

## Коли вчитель каже "все ок, мержни в main":

```bash
git checkout main && git merge preview && git push && git checkout preview
```
