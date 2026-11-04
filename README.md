# Hi there, my name is Alexey

*связаться со мной - [TG: @HorsovAlexey](https://t.me/HorsovAlexey)*

---

## Обо мне

Инженер по образованию (природообустройство и водопользование), перешёл в разработку и работу с данными. 
Более года официального опыта. Так же прошёл профессиональную переподготовку по нейросетям.
Мне нравится разбираться, как устроены данные и сервисы: строить загрузки, искать причины расхождений, писать понятный код и проверять его тестами.

---

## Стек

- **Языки:** Python, SQL, Java
- **Данные:** PostgreSQL, Greenplum, ClickHouse, Hadoop (HDFS, Hive), Apache Spark (PySpark), Kafka, Apache Airflow
- **Backend и API:** FastAPI, aiogram, Spring Boot, Servlet API
- **ML:** scikit-learn, PyTorch, TensorFlow (Keras), Hugging Face Transformers
- **Инструменты:** Git, GitLab, Docker, Linux, Jira, PyCharm, VS Code

---

## Доп. образование (стажировки и прочее)

- ### Aston: [«Data Engineer»](https://drive.google.com/file/d/1jWzKF-csZCvjaBz3AMBm__d2hiGX0Yyf/view) 2026 г.
  - **Роль:** Data Engineer (стажёр)
  - **Чем занимался:** Углублённое изучение реляционных СУБД и SQL: проектирование схем, оптимизация запросов, работа с индексами и транзакциями; построение и отладка ETL-пайплайнов; обработка больших объёмов данных в распределённых средах Hadoop (HDFS, MapReduce, Hive) и Apache Spark (PySpark, Spark SQL); автоматизация задач на Python.
  - **Стек:** SQL, PostgreSQL, Greenplum, ClickHouse, Python, Apache Hadoop (HDFS, Hive, MapReduce), Apache Spark (PySpark, Spark SQL), Apache Airflow, Docker, Git.

- ### Программа ДПО проф. переподготовки: [«Разработчик нейросетей»](https://drive.google.com/file/d/12J14P0vu_3tltLOzO_0dO8_DJUasBhhk/view) 2025 г.
  - **Роль:** Разработчик нейросетей
  - **Чем занимался:** Комплексное изучение и реализация end-to-end ML/DL решений: сбор и очистка данных, feature-engineering; разработка и сравнение классических моделей и нейросетей; практические кейсы по компьютерному зрению, NLP, обработке аудио, рекомендательным системам и прогнозированию временных рядов; аугментация, перенос обучения, валидация, мониторинг и развёртывание моделей. В ходе курса дорабатывал учебные приложения с помощью ИИ-ассистентов (см. проекты AI Chat ниже).
  - **Стек:** Python, NumPy, Pandas, scikit-learn, OpenCV, PyTorch / TensorFlow (Keras), Hugging Face (Transformers), Librosa (аудио), statsmodels / Prophet (временные ряды), FastAPI, Jupyter, Git.

- ### Y_lab: [«Погружение в Java»](https://ylab.io/upload/certificates/java/80649yTlKK1zj1JJurPA.pdf) 2022 г.
  - **Роль:** Java Backend-разработчик
  - **Чем занимался:** Разбирался в чужом коде, дорабатывал функционал REST API, применяя популярные паттерны, писал юнит-тесты и тестировал API при помощи Postman.
  - **Стек:** Java 11

---

## PET-проекты

- ### Export_MapInfo — плагин для QGIS
  Плагин для программы QGIS. Изначально проект выполнялся для инженеров камерального отдела, с целью миграции из программы MapInfo в QGIS. Добавляет опцию экспорта («Экспорт в MapInfo») в контекстное меню векторных слоёв QGIS для сохранения в формате MIF/TAB с автоматической подстановкой пределов BOUNDS (только для субъектов РФ). Основное отличие от встроенного экспорта — автоматический расчёт и подстановка пределов BOUNDS.
  **Что внутри:** определение региона по пересечению слоя с границами субъектов РФ (пространственный индекс), экспорт в фоновой задаче QGIS, пресеты пользовательских пределов в CSV, интерфейс в Qt Designer.

  [Ссылка на проект](https://github.com/Paoak/Export_MapInfo)
  
  **Стек:** Python, PyQt5, QGIS API (qgis.core), GDAL/OGR, Pandas, CSV.

  ---

- ### nlp-comparison-transformers-classical-methods
  Исследование и сравнение двух подходов к анализу текстов на примере отзывов IMDb: классических методов машинного обучения и моделей на основе трансформеров. В работе последовательно реализованы подготовка данных, обучение, оценка и сравнение моделей.
  **Результат:** DistilBERT (accuracy 0.897) обошёл лучшую классическую модель — логистическую регрессию (0.882), при этом BERT-tiny (0.806) оказался слабее классических методов. Трансформеры точнее, но заметно дороже по времени и ресурсам.

  [Ссылка на проект](https://github.com/Paoak/nlp-comparison-transformers-classical-methods)
  
  **Стек:** Python, Pandas, NumPy, scikit-learn, transformers, peft, torch, seaborn, matplotlib.

  ---

- ### Telegram-бот «Викторина»
  Бот с викториной: вопросы с вариантами ответов на inline-кнопках, команды `/start`, `/quiz`, `/stats`, статистика пользователя. Состояние игры и последний результат хранятся в SQLite, при перезапуске бот уведомляет пользователей.

  [Ссылка на проект](https://github.com/Paoak/TelegramQuizBot) · [@test_quiz_game_bot](https://t.me/test_quiz_game_bot)
  
  **Стек:** Python, aiogram 3, asyncio, aiosqlite (SQLite).

  ---

- ### Распознавание рукописных цифр — REST API
  Обучение простой нейросети (Keras) на датасете MNIST и её публикация как REST API на FastAPI прямо из Google Colab. Эндпоинты: `/health`, `/predict` (загрузка PNG), `/history` (просмотр и очистка истории предсказаний), автоматическая Swagger-документация; публичная ссылка через SSH-туннель Serveo.

  [Ссылка на проект](https://github.com/Paoak/RestAPI_MNIST)
  
  **Стек:** Python, TensorFlow/Keras, FastAPI, Pydantic, Uvicorn, Pillow, Google Colab.

  ---

- ### AI Chat (Python, Flet) — доработка учебного приложения
  Настольный чат для общения с языковыми моделями через OpenRouter API (учебный проект курса, исходная версия — [neuro-fill/51-lesson](https://github.com/neuro-fill/51-lesson)).
  **Моя доработка:** система авторизации — ввод API-ключа с проверкой баланса, генерация 4-значного PIN, вход по PIN или сброс ключа; данные хранятся в SQLite.

  [Ссылка на проект](https://github.com/Paoak/Ai_chat_test)
  
  **Стек:** Python, Flet, SQLite, requests, PyInstaller.

  ---

- ### AIChatFlutter
  Мультиплатформенное приложение для чата с языковыми моделями на Flutter (оригинал — [neuro-fill/AIChatFlutter](https://github.com/neuro-fill/AIChatFlutter)). Работает с OpenRouter и VseGPT. Доработано с использованием ИИ-ассистентов в рамках курса по разработке нейросетей.
  **Что добавлено:** многостраничный интерфейс, экран настроек провайдера и ключей, валидация ключа и блокировка чата до его ввода, статистика по токенам и моделям, график расходов по дням, управление состоянием через Provider, локальная история в SQLite.

  [Ссылка на проект](https://github.com/Paoak/AIChatFlutter)
  
  **Стек:** Dart, Flutter, Provider, sqflite, OpenRouter API.


  ---

- ### Spring Boot REST API (учебный проект)
  REST API на Spring Boot 17 с in-memory хранилищем: пользователи и их книги. Слоистая архитектура (controller → facade → service → storage), DTO и MapStruct, валидация, глобальный обработчик исключений, Swagger-документация.

  [Ссылка на проект](https://github.com/Paoak/SpringBootLab)
  
  **Стек:** Java 17, Spring Boot, MapStruct, Lombok, springdoc-openapi, Maven.

  ---

- ### JavaServlet
  Сервлеты на Java: жизненный цикл (`init`, `service`, `doGet`, `doPost`), обработка GET/POST-запросов, загрузка файлов (multipart) и передача данных на JSP.

  [Ссылка на проект](https://github.com/Paoak/Servlet)
  
  **Стек:** Java, Servlet API, JSP, Maven, Jetty, Apache Tomcat.

