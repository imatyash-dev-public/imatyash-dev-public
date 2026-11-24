# Иван Матяш — Lead Systems Analyst | Data Engineer | AI Systems Architect

**18+ лет в ИТ:** проектирование архитектуры корпоративных и государственных систем (B2G/Enterprise), инженерия больших данных (Medallion Lakehouse, PySpark, DWH/BI) и разработка детерминированных мультиагентных LLM-конвейеров.

---

### 🎯 Ключевые архитектурные компетенции

* **Системный анализ и архитектура (SA / Enterprise Architecture):** проектирование высоконагруженных интеграционных контуров (REST API, OpenAPI/Swagger, gRPC, Kafka/RabbitMQ), моделирование процессов и конечных автоматов (BPMN 2.0, UML, FSM), разработка ТЗ/ЧТЗ, внедрение и импортозамещение в B2G/Enterprise.
* **Инженерия данных и аналитика (Data Engineering & BI):** построение хранилищ по архитектуре Medallion Lakehouse (Bronze → Silver → Gold), распределенная обработка данных на **Python 3.13 / PySpark 4.3** (Catalyst/Tungsten, Parquet Snappy), сложный аналитический SQL (оконные функции, CTE), витрины данных и BI-дашборды (**Yandex DataLens, Power BI / DAX, FineBI**).
* **Инженерия ИИ-систем (Agentic AI & LLM Pipelines):** паттерн **Thin-Agent / Thick-Tool**, детерминированная оркестрация ролевых агентов через конечные автоматы (SQLite WAL FSM) и строгие JSON CLI-контракты, защита от косвенных промпт-инъекций (Indirect Prompt Injection Defense), FinOps-оптимизация инференса и Automated QA Gates.

---

### 📂 Витрина открытых инженерных проектов (Pinned Repositories)

Все публичные проекты в этом профиле полностью автономны (включают синтетические/сэмпл-фикстуры для локального запуска без внешних ключей) и суммарно покрыты **146 автотестами на `pytest`**:

| Репозиторий | Домен и архитектурный фокус | Стек и верификация |
| :--- | :--- | :--- |
| **[`document_pipeline_public`](https://github.com/imatyash-dev-public/document_pipeline_public)** | **Multi-Agent ETL & Document Pipeline:** архитектура *Thin-Agent / Thick-Tool* (5 LLM-агентов + 5 Python CLI-тулов), конечный автомат на 12 состояний в SQLite (WAL), защита от косвенных промпт-инъекций (проверка на adversarial-фикстурах), FinOps-гейткипер и автоматический гейт качества `.docx` (`keyword_overlap_pct ≥ 85%`). | `Python 3.13` `SQLite WAL` `Jinja2` `python-docx` `Multi-Agent CLI`<br>✅ **112 автотестов Pytest** |
| **[`caucasus_trail_lakehouse`](https://github.com/imatyash-dev-public/caucasus_trail_lakehouse)** | **Big Data Medallion Lakehouse & Geo-Analytics:** сквозной конвейер обработки 12+ млн геопространственных и телеметрических записей (OSM, SRTM, GPS-треки по 3 горным кластерам Кавказа). Оптимизация на уровне Catalyst/Tungsten (0 Python UDF), Broadcast Hash Join (11.76 млн точек × 75 833 маршрута), сжатие Parquet Snappy в 3.43 раза, 4 витрины Gold и слой BI. | `PySpark 4.3` `Spark SQL` `Parquet` `Yandex DataLens` `Power BI (DAX)` `Leaflet/Plotly`<br>✅ **21 автотест Pytest** |
| **[`jumpometer_garmin_fit_analytics`](https://github.com/imatyash-dev-public/jumpometer_garmin_fit_analytics)** | **Binary Telemetry Inspector & Agentic SDLC Case Study:** декодирование бинарного протокола Garmin `.FIT` для аналитики прыжков MTB, генератор синтетических бинарных `.FIT`-фикстур без GPS/PII на базе SDK Encoder и инженерный разбор реинжиниринга через команду из 4 ролевых ИИ-агентов (`Manager`, `Backend`, `Frontend`, `QA`). | `Python 3.13` `garmin-fit-sdk` `Binary Protocols` `Agentic SDLC`<br>✅ **13 автотестов Pytest** |

---

### 🌐 О языке репозиториев (Language & Prompt Engineering Note)

> **Почему документация кода, контракты и системные промпты в репозиториях написаны на английском языке (English C1):**
> В проектах, связанных с мультиагентной оркестрацией (Agentic SDLC) и LLM-пайплайнами, английский язык выбран осознанно как инженерный стандарт. При взаимодействии с современными LLM он обеспечивает:
> 1. **Семантическую однозначность** при следовании строгим схемам данных (JSON-контракты, FSM-переходы, Tool Calling).
> 2. **FinOps-эффективность токенизации:** за счет устройства BPE-токенизаторов спецификации и промпты на английском языке расходуют на **35–45% меньше токенов** и контекстного окна, чем аналогичные конструкции на кириллице, при более высокой точности кодогенерации.
>
> При этом вся проектная, архитектурная и бизнес-документация для заказчиков (ТЗ/ЧТЗ, ГОСТ 34 / 19, спецификации API, регламенты и аналитические отчеты) свободно ведется на русском языке.
