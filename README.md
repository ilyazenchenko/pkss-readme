# Информационная система "Электронные визитки"

Информационная система "Репозиторий 3D моделей" позволяет загружать, выгружать, искать и просматривать 3D модели

## 1. Структура функциональных возможностей (Mind Map)

```mermaid
mindmap
  root((Репозиторий 3D моделей))
    Генерация моделей
      AI-интеграция
    Загрузка моделей
      Проверка целостности
      Метаданные
    Управление моделями
      Редактирование
      Удаление
    Поиск и фильтрация
      По тегам
      По автору
    Работа с пользователями
      Регистрация
      Авторизация
```

## 2. Диаграмма путешествия пользователя (User Journey Diagram)
Крит путь пользователя. Ииллюстрирует ключевые шаги клиента в процессе использования системы: от входа до завершения заказа.

```mermaid
journey
  title Путешествие пользователя в репозитории 3D моделей
  section Посетитель
    Посещение сайта: 5: Посетитель
    Поиск модели: 4: Посетитель
    Просмотр деталей модели: 4: Посетитель
  section Авторизованный пользователь
    Регистрация: 4: Пользователь
    Загрузка модели: 5: Пользователь
    Генерация 3D модели: 5: Пользователь
  section Администратор
    Проверка загруженных моделей: 3: Администратор
    Удаление нежелательного контента: 3: Администратор
```

## 3. Квадрант-граф (Quadrant Chart)
```mermaid
quadrantChart
    title Functional Capabilities of the Repository
    x-axis Low Creativity --> High Creativity
    y-axis Low Ease of Use --> High Ease of Use
    quadrant-1 Optimal Features
    quadrant-2 Needs Promotion
    quadrant-3 Requires Improvement
    quadrant-4 Promising Features
    "Model Generation": [0.8, 0.9]
    "Model Upload": [0.5, 0.8]
    "Model Editing": [0.6, 0.7]
    "Search and Filtering": [0.7, 0.9]
    "User Management": [0.4, 0.6]
```

## 4. Git-граф
Отображает историю разработки, включая основные ветки и слияния.

```mermaid
gitGraph
  commit id: "Инициализация проекта"
  branch feature/ai
  checkout feature/ai
  commit id: "Добавлен AI для генерации"
  commit id: "Оптимизация алгоритма генерации"
  checkout main
  merge feature/ai
  branch feature/auth
  checkout feature/auth
  commit id: "Добавлена авторизация"
  commit id: "Исправлены баги авторизации"
  checkout main
  merge feature/auth
  branch feature/ui
  checkout feature/ui
  commit id: "Добавлен интерфейс загрузки моделей"
  commit id: "Доработан дизайн страницы поиска"
  checkout main
  merge feature/ui
  branch feature/stats
  checkout feature/stats
  commit id: "Добавлена статистика пользователей"
  commit id: "Реализована агрегация данных"
  checkout main
  merge feature/stats
```
