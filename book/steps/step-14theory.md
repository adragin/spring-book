## Комментарий

Процесс разделения таблицы на более мелкие, логически связанные таблицы, чтобы устранить избыточность данных и улучшить их организацию, называется нормализацией базы данных. Нормализация включает в себя создание таблиц и установление связей между ними в соответствии с определенными правилами, чтобы защитить данные и повысить гибкость базы данных.

### Основные цели нормализации:

- **Устранение избыточности данных**: Нормализация помогает избежать дублирования данных, что уменьшает объем базы данных и предотвращает несогласованные зависимости.
- **Упрощение структуры базы данных**: Разделение данных на логически связанные таблицы делает базу данных более управляемой и легкой для понимания.
- **Повышение целостности данных**: Нормализация обеспечивает сохранение целостности данных путем установления четких связей между таблицами.

### ? Примеры нормальных форм:

1. **Первая нормальная форма (1NF)**: Устранение повторяющихся групп данных. Каждое поле в таблице должно содержать атомарные (неделимые) значения.
2. **Вторая нормальная форма (2NF)**: Устранение частичных зависимостей. Все неключевые атрибуты должны зависеть от всего первичного ключа, а не от его части.
3. **Третья нормальная форма (3NF)**: Устранение транзитивных зависимостей. Неключевые атрибуты должны зависеть только от первичного ключа и не должны зависеть друг от друга.

[Шаг 15](./step-15.md)