Тестовый проект для Optimal City. Используемые технологии: **Vue.js 3** (фронтенд), **Element-Plus** (дизайн).

Недостатки и пути их решения:

- отсутствует нормальная база данных, после обновления страницы данные не сохраняются. Выход - создание локальной БД (к примеру - **SQLite**)

Пути усовершенствования приложения:

- создание отдельной БД для хранения элементов (к примеру - **MSSQL**)
- создание серверной части приложения (к примеру - на **.NET 7**), работа через API с клиентской частью - облегчение поддержки приложения
- добавление даты последнего изменения и показ изначального значения value