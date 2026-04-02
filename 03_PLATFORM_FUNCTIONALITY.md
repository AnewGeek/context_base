# AITA Platform --- Functionality & Capabilities
> Описание функциональных модулей платформы AITA. Сгенерирован 2026-04-02.
> Основано на реальном API (MCP) и продуктовом состоянии.

---

## 1. Обзор платформы

**AITA** --- это вертикальная B2B-платформа для управления жизненным циклом проектов возобновляемой энергетики. Объединяет CRM, управление проектами, dataroom, каталог оборудования, финансовое моделирование, AI-инструменты и торговые операции в единой экосистеме.

**Компания:** AITA WORLD, S.L. (Испания)
**Стек:** Web-приложение, REST API, MCP-интеграция, AI (Claude Vision, генерация вопросов)
**Юрисдикция:** Испания (EU), операции в ES/PL/UA/DE

---

## 2. Модули платформы

### 2.1 Project Management

Управление проектами солнечной энергетики полного цикла.

**Возможности:**
- Создание, редактирование, удаление проектов
- Жизненный цикл: PRE_FEASIBILITY_STUDY -> GREENFIELD -> FEASIBILITY_STUDY -> READY_TO_BUILD -> UNDER_CONSTRUCTION -> OPERATION -> DECOMMISSIONING
- Типы установок: GROUND_MOUNTED, ROOFTOP, INDOOR, STREET
- Компоненты: SOLAR, BESS (батарейные хранилища)
- Географическая привязка (координаты, адрес, страна, город)
- Lifecycle badges: isLandSecured, isGridConnectionSecured, isEpcSecured, isOfftakeSecured

**Технические параметры проекта:**
- Мощность (installedCapacity, totalCapacity, inverterPower, gridConnectionPower)
- Площадь (installationArea, effectiveArea, communicationArea)
- Параметры панелей (tiltAngle, orientation, rowSpacing, moduleCount)
- Производство энергии (estimatedAnnualProduction, prRatio, stationEfficiency, totalLosses)
- CO2 Emissions
- Распределение производства (месячное, почасовое)
- EMS (Energy Management System) и мониторинг (LOCAL/REMOTE)

**Финансовые параметры:**
- CAPEX, OPEX, Insurance
- IRR, ROI, NPV, Payback Period
- EBITDA, EBIDA, Tax
- Total Investment (equipment + works + services)
- Market Value, Subsidies
- Inflation Rate, Market Fluctuation, Discounting Rate

**Timeline & Permits:**
- Project Start Date, COD Scheduled, RTB Scheduled
- Building Permit (issued/final dates)
- Connection Conditions (issued/final dates)
- Construction Time, Development Time, Project Lifetime

**Legal / Offtake:**
- Offtake contract types: PPA, FIT, FIP, CfD, MerchantOfftake, VPPA, SPPA, CPPA
- PPA energy share, base price, contract formula
- Construction & operational guarantees
- Corporate structure description
- Financing scheme & mechanisms
- Ownership structure
- Participants structure

**Access Control:**
- Уровни доступа: OWNER, ADMIN, WRITE, READ
- Управление списком аккаунтов с доступом к проекту
- Publication status (isPublished)

---

### 2.2 SPV (Special Purpose Vehicles)

Управление юридическими сущностями (SPV) и их связями с проектами.

**Возможности:**
- Создание, редактирование, удаление SPV
- Типы: JOINT_VENTURE, PROJECT_FINANCING
- Юридические структуры: LIMITED_LIABILITY_COMPANY и др.
- Статусы: ACTIVE
- Привязка/отвязка проектов к SPV
- Автоматический расчёт: totalCapacity, actualValuation, projectsCount
- Initial Capital, Currency
- Registration ID, Jurisdiction

---

### 2.3 CRM (Customer Relationship Management)

Полноценная CRM для управления контактами, лидами и воронками.

#### Контакты
- Создание, редактирование, удаление, поиск
- Типы: B2B, B2C
- Поля: fullName, emails[], phones[], addresses[], companyName, position, gender, birthDate, description

#### Лиды
- Создание, редактирование, удаление, поиск
- Привязка к контакту, источнику, воронке, этапу
- Quality levels: A, B, C
- Quality score (0-100)
- Поля: region, service, kw, cost, description, metadata (JSON)
- Перемещение между этапами воронки (crm_lead_move_stage)
- Lost reasons (причины потери лида)
- История изменений (includeHistory)

#### Воронки (Funnels)
- Создание кастомных воронок с произвольным числом этапов
- Типы: B2B
- Каждый этап (stage): name, description, color, order
- Drag-and-drop перемещение лидов между этапами

#### Источники лидов (Lead Sources)
- Настраиваемые источники: Referral, Power Connect Event, LinkedIn и др.

---

### 2.4 Deals (Сделки)

Управление сделками от создания до закрытия.

**Возможности:**
- Создание сделок вручную или из лида (deal_create_from_lead)
- Типы: EQUIPMENT_SERVICE_SALE и др.
- Статусы: DRAFT, ACTIVE, CLOSED
- Привязка к офферу, лиду, контакту
- Привязка к воронке и этапу воронки

**Line Items (позиции сделки):**
- Типы: PRODUCT, SERVICE, PROJECT, CUSTOM
- Добавление/удаление позиций
- Цена и количество

**Negotiation Context:**
- Версионирование контекста переговоров
- Текущий/принятый контекст

**Дополнительно:**
- Документы сделки
- Сообщения/комментарии (deal chat)
- Metadata (JSON)

---

### 2.5 Offers (Офферы)

Управление коммерческими предложениями.

**Возможности:**
- Создание, редактирование, удаление, закрытие офферов
- Типы: SALE, PURCHASE
- Статусы: DRAFT, ACTIVE, CLOSED
- Direction: SUPPLY
- Deal type: B2B
- Investment parameters: amount, equity %, expected return, period, exit strategy
- Metadata (JSON)

---

### 2.6 Orders (Заказы)

Управление заказами оборудования.

**Возможности:**
- Создание, редактирование заказов
- Жизненный цикл: DRAFT -> SUBMITTED -> CONFIRMED -> (CANCELLED)
- Добавление/удаление позиций (order items)
- Привязка к продуктам из каталога
- Привязка к компании-клиенту
- Quantity, unitPrice (override)

---

### 2.7 Invoices (Инвойсы)

Управление счетами и платежами.

**Возможности:**
- Создание из сделки или заказа (invoice_create_from_order)
- Due date, VAT rate
- Payment terms, notes
- Запись платежей (record_payment): amount, payment method, note

---

### 2.8 Product Catalog

Каталог оборудования и сервисов.

**Продукты:**
- 100+ позиций (солнечные панели, инверторы, BESS)
- Категории, поиск, фильтрация
- Интеграция с заказами

**Сервисы:**
- CRUD для сервисов
- Категории сервисов
- Published/unpublished статус
- Цена, описание

**Категории каталога:**
- Иерархические категории (parentId)
- Поиск по имени

---

### 2.9 Dataroom (Хранилище документов)

Структурированное хранилище файлов для проектов, SPV и компаний.

**Возможности:**
- Создание папок (с иерархией)
- Загрузка файлов (base64 или локальный путь)
- Скачивание файлов (presigned URL)
- Удаление файлов
- Business units: COMPANY, PROJECT, SPV
- Автоматическая организация по бизнес-юнитам

---

### 2.10 Task Management

Управление задачами с полноценным workflow.

**Возможности:**
- Создание, редактирование, удаление задач
- Привязка к entity (PROJECT, SPV, COMPANY)
- Assignee (назначение исполнителя)
- Priority: 0 (urgent) -> 4 (lowest)
- Status categories: OPEN, IN_PROGRESS, REVIEW, DONE, CANCELED
- Due dates

**Связи между задачами:**
- PARENT_OF / CHILD_OF (epics / subtasks)
- BLOCKS / BLOCKED_BY
- Автоматическое создание обратных связей

**Дополнительно:**
- Комментарии к задачам
- Labels (метки) --- 30 настроенных меток
- Вложения файлов (через dataroom)
- Kanban board view (недавно реализовано)
- Поиск, фильтрация, сортировка
- Slim mode (compact output)

**Метки (Labels) --- 30 шт.:**
- Бизнес: AITA, Finance, Legal, Marketing, Project, supply, events
- SDLC: planning, requirements, design, implementation, review, testing, documentation, deploy
- Тестирование: backend, ui, migration, typecheck, coupled:auth/crm/orders, skip
- Специальные: prod-bug, tech-debt, solar-design, Онбординг, Коммерческий, from Dima S

---

### 2.11 Entity Graph (Граф связей)

Визуализация и управление связями между сущностями.

**Возможности:**
- BFS-обход графа от любой сущности (depth 1-3)
- Типы сущностей: PROJECT, SPV, COMPANY, CONTACT, LEAD, DEAL, TASK, PROFILE, FOLDER, OFFER, ORDER
- Типы связей: LINKED_TO, CREATED_FROM, MEMBER_OF, OWNS, MANAGES, PARTICIPATES_IN, CHILD_OF
- Создание ручных связей между сущностями
- Фильтрация по направлению (outgoing/incoming/both)

---

### 2.12 Analytics

Аналитические модули платформы.

**Portfolio Analytics:**
- Общее кол-во проектов, мощность, распределение по статусам
- Географическое распределение

**Financial Analytics:**
- Per-project: CAPEX, OPEX, IRR, NPV, LCOE
- Portfolio-wide: total CAPEX, avg IRR, avg LCOE
- Financial model calculation (analytics_calculate per project)

**CRM Funnel Analytics:**
- Conversion rates, stage distribution
- Lead velocity, pipeline value
- Quality distribution (A/B/C)

**Audit & Compliance:**
- Document completeness
- Permit status tracking
- Regulatory compliance scores
- GO / NO-GO / GO with fixes

**Trends:**
- Revenue, capacity, leads, conversion over time
- Configurable date range

**Alerts:**
- Threshold-based alerts
- Types: audit_low, conversion_low
- Severity levels

**Context Summary:**
- Natural-language AI summary для copilot-контекста

---

### 2.13 AI-powered Features

**PDF Spec Extraction (Claude Vision):**
- Автоматическое извлечение технических спецификаций из PDF-файлов
- Маппинг на ECS-сущности

**AI Clarification Panel:**
- Автоматическая генерация уточняющих вопросов для заполнения проектных данных
- State machine для Q&A flow

**Gap Analysis Engine:**
- Определение пробелов в документации проекта
- Автоматическое предложение следующих шагов

**Duplicate Detection:**
- Обнаружение дублей файлов
- Vendor CAD filtering

---

### 2.14 Solar Design Tools

**Возможности:**
- Solar design ECS (Entity Component System)
- SLD (Single Line Diagram) генерация
- DXF export (planta general + SLD)
- SVG export с title block
- WASM CAD viewer
- Grounding data rendering
- Country-specific electrical norms
- KTP type designation
- BESS financial optimization (penalty avoidance, capacity sensitivity)

---

### 2.15 User Management

**Profiles:**
- Поиск пользователей по имени
- Profile details: fullName, avatar, language, verificationStatus
- Reference/equivalent currency settings

**Authentication:**
- Login / status check
- Verification statuses

---

### 2.16 MCP Integration

Платформа полностью доступна через Model Context Protocol (MCP), что позволяет AI-агентам:
- Читать и записывать данные всех модулей
- Создавать и управлять проектами, лидами, сделками
- Запускать аналитику и финансовые расчёты
- Управлять задачами и файлами
- Строить и навигировать граф связей

**MCP Tools:** 100+ инструментов покрывают все модули платформы.

---

## 3. Интеграции

| Интеграция | Описание |
|------------|----------|
| MCP API | Full CRUD + analytics через AI-агентов |
| Claude Vision | PDF spec extraction |
| S3 (AWS) | Хранение файлов dataroom |
| WASM CAD | Просмотр DXF/CAD файлов в браузере |
| SSE | Real-time updates (pipeline progress) |

---

## 4. Карта файлов контекста

| Файл | Содержание |
|------|-----------|
| `01_AITA_FULL_CONTEXT.md` | Бизнес-модель, монетизация, договоры (юридическая база) |
| `02_PLATFORM_LIVE_STATE.md` | Актуальный снимок данных платформы (проекты, CRM, задачи) |
| `03_PLATFORM_FUNCTIONALITY.md` | Описание функциональных модулей и возможностей платформы |
