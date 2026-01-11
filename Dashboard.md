# 🏠 Dashboard

## 📅 Сегодня
Сегодня: `= dateformat(date(today), "cccc, dd MMMM yyyy")`

## 🎯 Активные проекты
```dataview
TABLE status, updated as "Обновлено"
FROM "🎯 Projects"
WHERE status = "🟢 active"
SORT updated DESC
LIMIT 5
```

## ✅ Задачи на сегодня
```dataview
TASK
WHERE !completed
LIMIT 10
```

## 🎮 Недавние игровые гайды
```dataview
TABLE type, updated as "Обновлено"
FROM "🎮 Gaming"
SORT updated DESC
LIMIT 5
```

## 📚 Недавно добавленное в базу знаний
```dataview
TABLE topics, created as "Создано"
FROM "💡 Knowledge Base"
SORT created DESC
LIMIT 5
```

## 📝 Последние заметки из Inbox
```dataview
TABLE file.ctime as "Создано"
FROM "📥 Inbox"
SORT file.ctime DESC
LIMIT 5
```

---
[[Task Dashboard]]