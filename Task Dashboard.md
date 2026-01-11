# 📋 Task Dashboard

## 🎯 Активные проекты
```dataview
TABLE status, updated as "Обновлено"
FROM "🎯 Projects"
WHERE status = "🟢 active"
SORT updated DESC
```

## 📝 Задачи на сегодня
```dataview
TASK
WHERE !completed AND due <= date(today)
SORT due ASC
```

## 📅 Предстоящие задачи
```dataview
TASK
WHERE !completed AND due > date(today)
SORT due ASC
LIMIT 10
```

## 🎮 Игровые гайды
```dataview
TABLE type, updated as "Обновлено"
FROM "🎮 Gaming"
SORT updated DESC
LIMIT 10
```

## 📚 База знаний
```dataview
TABLE topics, created as "Создано"
FROM "💡 Knowledge Base"
SORT created DESC
LIMIT 10
```

## 📥 Inbox
```dataview
TABLE file.ctime as "Создано"
FROM "📥 Inbox"
SORT file.ctime DESC
LIMIT 10
```

---
[[Dashboard|← На Dashboard]]