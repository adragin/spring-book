# Многоуровневая архитектура

## Layered architecture

<img src = "https://www.oreilly.com/api/v2/epubs/9781491971437/files/assets/sapr_0101.png" width = 600>

также известной как n-tier архитектура. Это один из наиболее распространенных шаблонов архитектуры, особенно в приложениях Java EE. Основные моменты этой архитектуры:

## Основные концепции многоуровневой архитектуры

- **Структура**: Компоненты организованы в горизонтальные слои, каждый из которых выполняет определенную роль в приложении. Обычно архитектура состоит из четырех стандартных слоев: презентационный, бизнес-логики, персистентности и базы данных. В некоторых случаях бизнес-слой и слой персистентности могут быть объединены.

- **Роли и ответственность**:
  - **Презентационный слой**: Обрабатывает пользовательский интерфейс и логику взаимодействия с браузером.
  - **Бизнес-слой**: Выполняет бизнес-правила, связанные с запросами.
  - **Слой персистентности**: Управляет доступом к данным и взаимодействием с базой данных.
  - **База данных**: Хранит данные приложения.

- **Разделение ответственности**: Каждый слой отвечает только за свою часть логики, что упрощает разработку, тестирование и поддержку приложений.

- **Закрытые и открытые слои**: 
  - **Закрытые слои**: Каждый запрос должен проходить через все слои, начиная с презентационного и заканчивая слоем базы данных, что обеспечивает изоляцию изменений.
  - **Открытые слои**: Позволяют пропускать некоторые слои для оптимизации доступа, например, бизнес-слой может напрямую обращаться к слою персистентности.

## Пример использования

Предположим, пользователь хочет получить информацию о клиенте. Запрос начинается с презентационного слоя, который передает его в бизнес-слой. Бизнес-слой обрабатывает запрос, обращаясь к слою персистентности для получения данных, а затем возвращает результат обратно в презентационный слой для отображения.

## Преимущества и недостатки

- **Преимущества**:
  - Высокая тестируемость благодаря четкому разделению слоев.
  - Простота разработки из-за известности и простоты реализации.

- **Недостатки**:
  - Низкая производительность из-за необходимости прохождения через несколько слоев.
  - Сложности с масштабируемостью, так как архитектура склонна к монолитности.
  - Низкая гибкость при изменениях из-за тесной связи компонентов.

Многоуровневая архитектура является хорошим стартовым шаблоном для большинства приложений, особенно если вы не уверены, какой шаблон архитектуры лучше всего подходит для вашего приложения.

[Далее >>](./part-05.md)