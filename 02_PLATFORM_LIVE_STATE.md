# AITA Platform --- Live State Snapshot
> Актуальный снимок данных платформы AITA. Сгенерирован 2026-04-02.
> Источник: AITA MCP API (prod). Компания: AITA WORLD, SL.

---

## 1. Портфель проектов (10 проектов)

### Испания

| Проект | Мощность | Статус | Тип | Локация | CAPEX | IRR | SPV |
|--------|----------|--------|-----|---------|-------|-----|-----|
| ST George British International School | 50 kW | GREENFIELD | SOLAR + BESS | Bilbao, ES | -- | -- | -- |
| Saint George British International School - Solar | 0.5 MW | GREENFIELD | SOLAR | -- | -- | -- | Saint George Solar SPV, SL |
| PV Placencia | 1.18 MW | UNDER_CONSTRUCTION | SOLAR | -- | $878K | 2.9% | FV Orgiva |
| FV DISPOSOL | 4 MW | READY_TO_BUILD | SOLAR | -- | $2.25M | 1.67% | FV Orgiva |

### Польша

| Проект | Мощность | Статус | Тип | Локация | CAPEX | SPV |
|--------|----------|--------|-----|---------|-------|-----|
| Objazda | 25 MW | READY_TO_BUILD | SOLAR | Objazda, PL | -- | -- |
| PV_LIWKI_WLOSCIANISKIE | -- | FEASIBILITY_STUDY | SOLAR | -- | -- | -- |
| Galaxy 2 | 22.6 MW | OPERATION | SOLAR | -- | -- | -- |

### Украина

| Проект | Мощность | Статус | Тип | Локация | CAPEX | SPV |
|--------|----------|--------|-----|---------|-------|-----|
| MC Donalds Chernivtsi | 0.2 MW | GREENFIELD | SOLAR + BESS | Чернiвцi, UA | -- | ТОВ «ЕСI» |
| Lviv Polytech PV + BESS + AI campus | 1 MW | GREENFIELD | SOLAR | Lviv, UA | $1.86M | -- |
| Westing Cover Energy Park | 6 MW | READY_TO_BUILD | SOLAR + BESS | Lviv Oblast, UA | -- | -- |

### Сводка по статусам

| Статус | Кол-во |
|--------|--------|
| GREENFIELD | 4 |
| READY_TO_BUILD | 3 |
| UNDER_CONSTRUCTION | 1 |
| FEASIBILITY_STUDY | 1 |
| OPERATION | 1 |

---

## 2. SPV (Special Purpose Vehicles) --- 4 шт.

| SPV | Тип | Статус | Проектов | Суммарная мощность | Оценка |
|-----|-----|--------|----------|-------------------|--------|
| Aster Streams PL | JOINT_VENTURE | ACTIVE | 4 | 81.12 MW | $81.1M |
| ТОВ «ЕСI» | JOINT_VENTURE | ACTIVE | 3 | 38.8 MW | $38.8M |
| FV Orgiva | PROJECT_FINANCING | ACTIVE | 3 | 9.38 MW | $9.4M |
| Saint George Solar SPV, SL | PROJECT_FINANCING | ACTIVE | 0 | 0 MW | -- |

**Итого SPV-портфель:** 129.3 MW, оценка ~$129.3M

---

## 3. CRM

### Контакты
- **Всего:** 100+ контактов
- Типы: B2B и B2C
- Примеры: Дима Ся (DX comp), Марiя Ткаченко (EcoPower, Одеса), Святослав Мельник и др.

### Лиды
- **Всего:** 559 лидов
- **Quality A:** 13 (2.3%)
- **Quality B:** 471 (84.3%)
- **Quality C:** 75 (13.4%)
- **Конверсия:** 0% (critical alert)
- **Средний срок конверсии:** нет данных

### Источники лидов
1. Referral
2. Power Connect Event
3. LinkedIn; Onbound

### Воронки (12 шт.)

| Воронка | Кол-во этапов | Направление |
|---------|--------------|-------------|
| AITA Panels | 22 | Продажа солнечных панелей (опт) |
| AITA Equipment | 24 | Продажа оборудования |
| AITA Engineering | 19 | Инженерные услуги |
| Power Connect | 10 | Event-лиды |
| Inbound Qualification | 6 | Входящая квалификация |
| Investment UA | 9 | Инвестиции в Украине |
| Platform User Generation | 4 | Привлечение пользователей |
| Bizkaia_agent | 9 | Агентская сеть Бискайя |
| CCEP Zona Norte | 2 | Северная зона Испании |
| Asador Erillo | 4 | Отдельный клиент |
| Fallback | 1 | Фоллбэк |
| Leads | 0 | Пустая |

---

## 4. Сделки и Офферы

### Сделки --- 1 активная
| Сделка | Статус | Контакт | Воронка | Этап |
|--------|--------|---------|---------|------|
| Deal from Lead #9d84a633 | DRAFT | Святослав Мельник | AITA Panels | Пiдготовка КП |

Святослав --- розничный клиент, ищет ~20 кВт для дома. Основной барьер: наш минимум --- палета (21-30 кВт). Ожидает прайс-лист.

### Офферы --- 4 шт. (все DRAFT, B2B SUPPLY)
1. **LONGi** --- Hi-MOX9/X6 Max, 600-660W, от 1 контейнера
2. **JinkoSolar** --- JKM625-650N, N-type, от 1 контейнера
3. **HT-SAAE** --- 455W-705W, широкий диапазон
4. **Hanersun** --- до 730W, топовая линейка

### Заказы --- 57 шт.

### Инвойсы --- 0

---

## 5. Каталог

### Продукты: 100+ позиций
Солнечные панели, инверторы, BESS-оборудование от ведущих производителей.

### Сервисы: 0
Каталог сервисов пуст --- нужно заполнить.

---

## 6. Задачи платформы (топ приоритетные)

### Urgent (P0)
- Зробити в AITA воронку з актуальним списком агентiв (Kateryna Abramova)
- Запуск Germany track: онбординг Юрия под Ampir Energy Germany (Danylo Molokoiedov)

### High (P1)
- [SLD Bug] Fix DXF paper space sheets rendering
- [SLD Bug] Fix MV voltage label showing 0 kV
- BESS Penalty Avoidance & Financial Optimization (epic, 5 subtasks)

### Medium (P2)
- [EPIC] External Context Sources --- тендерные коммуникации и meeting summaries (Dmytro Mekhed)
- feat(solar): split DXF export --- planta general и SLD
- fix: WASM CAD viewer --- render text/annotations (In Review)
- Add contracted power optimization via BESS
- BESS capacity sensitivity analysis

### Завершённые недавно (Done)
- fix(cad-viewer): inverted zoom, broken tools
- feat(tasks): Kanban board view
- Chat: show entity name instead of ID
- [Story 7.1-7.3] PDF spec extraction, merge into ECS, compliance metadata
- [Story 4.2-4.4] File placement, gap analysis, duplicate detection
- [Story 5.1-5.3] AI question generation + clarification panel

---

## 7. Команда (видимые профили)

| Имя | Роль (по задачам) |
|-----|--------------------|
| Danylo Molokoiedov | CEO / Product Owner |
| Kateryna Abramova | Business Operations |
| Dmytro Mekhed | Lead Developer |

---

## 8. Алерты и проблемы

| Алерт | Серьёзность | Текущее значение | Порог |
|-------|-------------|-----------------|-------|
| Audit score | CRITICAL | 2.4 | 70 |
| Lead conversion | CRITICAL | 0% | 15% |

### Аудит
- Всего аудитов: 16
- GO: 0
- NO-GO: 16
- GO with fixes: 0

---

## 9. Ключевые метрики платформы

| Метрика | Значение |
|---------|----------|
| Проекты | 10 |
| SPV | 4 |
| Суммарная мощность SPV | 129.3 MW |
| Контакты CRM | 100+ |
| Лиды | 559 |
| Конверсия | 0% |
| Активные сделки | 1 |
| Офферы | 4 |
| Заказы | 57 |
| Продукты | 100+ |
| Воронки | 12 |
| Задачи (открытые) | ~40 |
| Задачи (выполнены) | ~10 |
