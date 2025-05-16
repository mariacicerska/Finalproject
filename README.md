# JokesApp — Варіант 3 (Clean Architecture)

## Загальний опис:
Додаток отримує жарти з API [Jokes Always API](https://rapidapi.com/sohailFiza/api/jokes-always) та відображає їх за категоріями. Користувач може додавати жарти в улюблені, які зберігаються локально через Room. Архітектура побудована згідно з принципами Clean Architecture, MVVM.

---

## Архітектура:
- **MVVM** (Model-View-ViewModel)
- **3 модулі**:
  - `data` (Kotlin lib): робота з API, Room, репозиторій
  - `domain` (Kotlin lib): інтерфейси, моделі, use cases
  - `presentation` (Android модуль): UI, ViewModel, навігація
- `app` — головний модуль запуску

---

## Технології:
- **Retrofit** — для запитів до мережі
- **Gson** — для парсингу JSON
- **Room** — для збереження улюблених жартів
- **Jetpack Navigation** — навігація між екранами
- **Material 3 + Scaffold** — сучасний дизайн
- **Koin** — для Dependency Injection
- **Unit tests** — для перевірки репозиторію
- **libs.versions.toml** — централізоване керування залежностями

---

## Особливості:
- Чітке розділення: **Presentation / Domain / Data**
- **LocalDataSource** (Room) + **RemoteDataSource** (API)
- **Repository pattern** для обробки даних
- Усі **рядки** — у `strings.xml`
- Усі **відступи** — у `dimensions.xml`
- Кожен екран має горизонтальний падінг **16dp**
- Весь UI побудований на **Jetpack Compose + Navigation + Scaffold**

---

## Структура UI:
- `CategoryScreen` — список категорій жартів
- `JokeScreen` — показ жарту по категорії
- `FavouritesScreen` — улюблені жарти з Room
- Навігація — через `NavHost`

---

## Як додати API ключ:
1. Зайти на [https://rapidapi.com/sohailFiza/api/jokes-always](https://rapidapi.com/sohailFiza/api/jokes-always)
2. Підписатись (subscribe)
3. Скопіювати значення `X-RapidAPI-Key`
4. Вставити в `RemoteDataSource` або `NetworkModule`

---

## Як запустити:
1. Відкрити проект у Android Studio
2. Дочекатись Gradle Sync
3. Встановити API ключ
4. Натиснути Run

---

## Автор:Чичерська Марія
Проєкт — Варіант 3  
IT STEP University  
