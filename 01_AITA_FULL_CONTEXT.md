# AITA Corp OS — Full Context Document
> Единый файл со всем контентом платформы AITA. Сгенерирован 2026-03-04.
> Используйте этот файл как полный контекст для AI-модели.

---


---

# ═══ MONETIZATION MASTER v2 (главный документ) ═══

**AITA WORLD, S.L.**

**Монетизация экосистемы**

Мастер-документ v2.0

*Март 2026 · Corp OS · Конфиденциально*

**Источники (по приоритету):**

-   **Единая таблица монетизации AITA (основной документ структуры)**

-   AITA --- Архитектура экосистемы v2 (юридическая база, ставки, договоры)

-   Договоры: Cooperation, ISA, Partnership, Team, Project Lead, Agent, Recruiter, Marketing

**Содержание:**

-   §0 --- Pre-Sale Access

-   §1 --- Каркас монетизации: 4 слоя (A Free / B SaaS / C Transactional / D Internal)

-   §2 --- Единая таблица: 8 групп пользователей (Free → Paid)

-   §3 --- Billing Events: 21 код потока

-   §4 --- RBAC: ролевая модель и сущности платформы

-   §5 --- Маршруты взаимодействия (3 маршрута)

-   §6 --- Управляющие правила (5 правил)

-   §7 --- Revenue Matrix: 22 источника дохода

-   §8 --- Billing Policy (waterfall, anti-double, reserve)

-   §9 --- Token-Ready архитектура

**§0. Pre-Sale Access к платформе**

Invite-only доступ к AITA Platform до массового открытия. Ограниченное число мест на когорту.

  -------------- --------------------------------------------------------------------------------------
  **Параметр**   **Условие**
  Стоимость      €500 за место --- единоразово, невозвратно
  Включено       Полный role-based доступ + фирменная футболка AITA + welcome pack
  Модель         Strictly invite-only; место привязано к конкретному пользователю и компании
  Активация      После подтверждения оплаты; действует на весь срок соглашения
  Возврат        Не предусмотрен; покрывает онбординг, provisioning, мерч
  Приоритет      Участники pre-sale --- приоритетный доступ к раундам портфеля и расширенным функциям
  -------------- --------------------------------------------------------------------------------------

*Billing code: PRE_SALE_ACCESS. Плата --- коммерческий взнос за доступ, не инвестиция и не депозит.*

**§1. Каркас монетизации: 4 слоя в одной системе**

Вся монетизация AITA укладывается в четыре слоя. Единый контур: контакты → проекты → документы → статусы → сделки → платежи → доказательная база.

Free zone даёт вход без трения. Monetization включается по понятным триггерам.

  ------- -----------------------------------
  **A**   **Free Core --- вход без трения**
  ------- -----------------------------------

  ------------------------------------------- ----------------------
  **Что входит в Free Core**                  
  Личная страница / профиль                   Базовый workspace
  CRM                                         Чат
  2 проекта \"на пробу\" (только Developer)   Dataroom (хранилище)
  ------------------------------------------- ----------------------

  ------- ---------------------------------------------------
  **B**   **Subscriptions / Packages --- SaaS-монетизация**
  ------- ---------------------------------------------------

  --------------- ---------------------------------------------------------------------------
  **Кто**         **Что**
  Developer       Commercial Packages --- с 3-го проекта или при включении advanced-модулей
  Investor        ISA Packages A / B / C / D (ретейнер / скрининг / management fee)
  (Опционально)   Invite-only Pre-Sale как entry fee (§0)
  --------------- ---------------------------------------------------------------------------

  ------- --------------------------------------------
  **C**   **Transactional --- основная монетизация**
  ------- --------------------------------------------

  ------------------------------------------ ------------------------------------
  **Источник**                               **Ставка**
  Developer success fee (CapEx stage)        2.7% Total CapEx Deal Volume
  Developer success fee (Dev stage)          5% Development Deal Value
  Investor fees (ISA Pkg A)                  1.5% Investment Amount
  Investor fees (ISA Pkg B)                  €4 000/мес + 1% + 0.4% platform tx
  Partner revenue share (Lead in vertical)   50% Profit/Margin
  Partner revenue share (outside vertical)   30% Profit/Margin
  EPC / Works Sales                          50/50 Works Margin
  Agent: AITA доля                           20% маржи (всегда)
  Marketing Pool (опционально)               Success fee 1.5% от сделки клиента
  ------------------------------------------ ------------------------------------

  ------- ---------------------------------------------------
  **D**   **Internal --- Corp OS «зарплата от результата»**
  ------- ---------------------------------------------------

  ------------------- -------------------------------------------------------------------------
  **Участник**        **Формула**
  Team Profit Pool    30% Profit of the Deal (self-governed, accrual as profit realized)
  Project Lead        20% Profit of the Deal + участие в 30% team pool
  AITA Retained       50% Profit of the Deal (платформа + операционные расходы)
  Digital-Only rule   Если не записано в AITA --- \"неверифицируемо\" → может не оплачиваться
  ------------------- -------------------------------------------------------------------------

**§2. Единая таблица: 8 групп пользователей (Free → Paid)**

IN --- деньги приходят в AITA (клиент платит). OUT --- AITA платит пользователю (выплаты).

**1. Физик (Individual / Community)**

  --------------------- -------------------------------------------------------------------------------------------------------
  **Параметр**          **Описание**
  Роли                  Individual, Self-owner
  Бесплатная зона       Профиль, базовый workspace, CRM, участие в задачах/контенте
  Триггер монетизации   POLICY: (1) хочет получать выплаты регулярно; (2) достиг лимита выплат
  Платёж / формула      OUT --- не более 2 выплат физическому лицу; далее обязателен статус BUSINESS_VERIFIED (ФОП/Autónomo)
  Договор / база        POLICY (внутренняя)
  Платформа             ComplianceStatus + payout-gate; журнал выплат; авто-триггер upgrade_to_business_required
  Будущее               Инвестиционные/торговые планы через токенизацию (To-Be)
  --------------------- -------------------------------------------------------------------------------------------------------

**2. Агент (ФОП / Autónomo / BUSINESS_VERIFIED)**

  ---------------------- ----------------------------------------------------------------------------------------------------
  **Параметр**           **Описание**
  Роли                   Agent, Recruiter
  Старт                  Только при статусе BUSINESS_VERIFIED
  Триггер монетизации    Confirmed Transaction --- оплата клиента подтверждена
  Платёж / формула       OUT --- делёж маржи: AITA 20% (всегда); Агент 30→45→60%; Рекрутер 50→35→20% (max)
  Уровни (автопереход)   L1: €0--15 000 · L2: €15 001--50 000 · L3: €50 001+
  Договор                Агентский блок договоров
  Платформа              Orders→Invoices→Payment confirm→Auto payout; уровни агента; recruiter override; anti-circumvention
  ---------------------- ----------------------------------------------------------------------------------------------------

**3. Компания --- Девелопер (Developer)**

  ----------------- ----------------------------------------------------------------------------------------
  **Параметр**      **Описание**
  Роли              Owner (signer), Management, Workers
  Бесплатная зона   2 проекта бесплатно: basic card + upload + базовые checks + базовый dataroom
  Триггер 1         Создаёт 3-й проект → Commercial Package (подписка/покупка)
  Триггер 2         Включает продвинутые модули → Commercial Package
  Триггер 3         Подписан LOI → включается эксклюзивность
  Триггер 4         Definitive agreements / closing → success fee
  Платёж IN (a)     Commercial Package --- фиксированная цена/подписка (Annex)
  Платёж IN (b)     2.7% × Total CapEx Deal Volume ИЛИ 5% × Development Deal Value
  Договор           Cooperation Agreement (Developer)
  Платформа         Paywall project_count \> 2; статусы проекта; LOI upload→exclusivity; fee event engine
  ----------------- ----------------------------------------------------------------------------------------

**4. Компания --- Инвестор (Investor / Fund)**

  ----------------- --------------------------------------------------------------------------------------------------------
  **Параметр**      **Описание**
  Роли              Owner (signer), Investment Team, Analysts
  Бесплатная зона   Нет trial --- пакеты сервиса
  Триггер           Выбор пакета + наступление события: binding docs / capital transfer / месяц ретейнера / скрининг готов
  Pkg A IN          1.5% × Investment Amount (earliest of binding docs OR 1st capital transfer, pro-rata)
  Pkg B IN          €4 000/мес + 1% × Investment Amount (closing) + 0.4% × gross platform transaction
  Pkg C IN          10% management fee (база --- per term sheet)
  Pkg D IN          \$15 / проект --- screening output delivery
  Договор           Investor Services Agreement (ISA)
  Платформа         Package selector + billing; audit/scoring output; platform transactions tracking
  ----------------- --------------------------------------------------------------------------------------------------------

**5. Компания --- Партнёр / EPC / Поставщик**

  ---------------------------------- --------------------------------------------------------------------------------------------
  **Параметр**                       **Описание**
  Роли                               Owner, Sales, PMs
  Бесплатная зона                    Обычно нет --- включение через сделки/лиды
  Триггер                            Lead assigned / Project onboarded / Order paid / Margin verified
  Lead in vertical IN                50% Partner Profit/Margin
  Lead outside vertical IN           30% Partner Profit/Margin
  Partner registers own project IN   1.5% × Fee Base (CAPEX/Investment)
  Direct investor reco IN            3% × Fee Base
  Advertising IO IN                  10% Partner Profit/Margin
  Equipment Marketplace IN           30% Equipment Margin
  Works / EPC IN                     50/50 Works Margin
  Open-book нормы IN                 +9% works / +4% equipment
  Договор                            Partnership Agreement
  Платформа                          Partner Dashboard; lead assignment; margin/open-book доказательность; авто-расчёт комиссий
  ---------------------------------- --------------------------------------------------------------------------------------------

**6. Маркетинг-продукт (Marketing Pool Membership)**

  --------------------------- ---------------------------------------------------------------------------------------------------------
  **Параметр**                **Описание**
  Роли                        Company Owner (payer), Sales users
  Бесплатная зона             Нет --- персональных лендингов нет (FF:disable_landing_pages)
  Модель                      Пайевой взнос в Marketing Pool AITA → статус участника активен → участие в распределении входящих лидов
  Триггер                     Оплата пайевого взноса в пул
  Платёж IN                   pool_contribution (параметр --- определяется по Order Form/IO)
  Распределение               Лиды распределяются по Allocation Policy AITA (не персонализированные кампании)
  Success fee (опционально)   1.5% от закрытой сделки клиента --- подключается по договорённости
  Договор                     POLICY и/или отдельный Order Form / IO
  Платформа                   Pool membership; lead allocator; SLA/discipline; fairness; FF:disable_landing_pages
  --------------------------- ---------------------------------------------------------------------------------------------------------

*ВАЖНО: Landing Pages отключены (FF:disable_landing_pages). LaaS €30/лид и депозит €2 000 --- устаревшая модель. Текущий продукт --- пул-модель с allocation policy.*

**7. Внутренняя команда AITA (Delivery Team)**

  -------------- ------------------------------------------------------------------------
  **Параметр**   **Описание**
  Роли           Founder/CEO (approval gates), Team roles
  Триггер        Profit realized --- после подтверждения Profit of the Deal
  Платёж OUT     Team Profit Pool = 30% Profit of the Deal (accrual as profit realized)
  Договор        Team Agreement
  Платформа      Evidence ledger; profit formula; accruals/reserves; payout requests
  -------------- ------------------------------------------------------------------------

**8. Project Lead (внутренний лидер кейса)**

  ------------------- ---------------------------------------------------------------------------------
  **Параметр**        **Описание**
  Роли                Deal Project Lead
  Триггер             DoD (Definition of Done) / Profit realized (по правилам)
  Платёж OUT (Lead)   20% Profit of the Deal
  Платёж OUT (Pool)   Участие в 30% team pool, pro-rata
  Reserve             До 10% на 90--180 дней (страховой резерв до финализации proof of delivery)
  Digital-Only        Всё исполнение фиксируется в AITA Platform --- иначе считается неверифицируемым
  Договор             Project Lead Agreement
  Платформа           DoD registry; reserve logic; payout schedule; digital-only validation
  ------------------- ---------------------------------------------------------------------------------

**§3. Billing Events --- 21 код потока**

Каждый платёж в системе --- это событие: код потока → кто платит → когда начисляется → формула → договор → доказательство в AITA. Коды потоков сохраняются при переходе к токенизации.

**3.1 Developer (Cooperation Agreement)**

  ----------------------------------- ----------------- ------------------------------------------------------- -------------------------------- --------------------------------------------
  **Код**                             **Плательщик**    **Триггер**                                             **Формула**                      **Доказательство**
  DEV_FREE_LISTING                  Developer         Первые 2 проекта                                        0 (free)                         Project count + статус Listed
  DEV_COMMERCIAL_PACKAGE            Developer         3-й проект ИЛИ advanced-модули                          Фикс/подписка (Annex)            Feature activation + invoice
  DEV_SUCCESS_FEE_CAPEX            Developer / SPV   Definitive agreements signed / consideration received   2.7% × Total CapEx Deal Volume   LOI + SPA/EPC/Financing docs + deal record
  DEV_SUCCESS_FEE_DEVSTAGE         Developer         Аналогичный триггер                                     5% × Development Deal Value      Аналогично + dev rights docs
  DEV_INVESTOR_ADVERTISING_ORDER   Developer         Заказ кампании (опционально)                            По Order Form / SOW              Подписанный IO/SOW + lead rules
  ----------------------------------- ----------------- ------------------------------------------------------- -------------------------------- --------------------------------------------

**3.2 Investor (ISA)**

  --------------------------------- ---------------- -------------------------------------------------------------- -------------------------------- ------------------------------------------
  **Код**                           **Плательщик**   **Триггер**                                                    **Формула**                      **Доказательство**
  ISA_PKG_A_MATCHING_FEE        Investor         Earliest of: binding docs OR 1st capital transfer (pro-rata)   1.5% × Investment Amount         Подписанные binding docs / bank transfer
  ISA_PKG_B_RETAINER             Investor         Ежемесячно (до 20 часов)                                       €4 000 / month                   Ежемесячный invoice
  ISA_PKG_B_EXECUTION_FEE       Investor         Closing / tranche                                              1.0% × Investment Amount         Closing docs + transfer evidence
  ISA_PLATFORM_TRANSACTION_FEE   Investor         Платёж/закупка через AITA                                      0.4% × gross transaction value   Platform transaction record
  ISA_PKG_C_MANAGEMENT_FEE      Investor         По Term Sheet                                                  10% management fee               Term sheet + platform record
  ISA_PKG_D_SCREENING            Investor         Screening output delivery                                      \$15 / project                   Screening report + delivery log
  --------------------------------- ---------------- -------------------------------------------------------------- -------------------------------- ------------------------------------------

**3.3 Partner / EPC (Partnership Agreement)**

  --------------------------------- ---------------- -------------------------------- ------------------------------------ -----------------------------------------
  **Код**                           **Плательщик**   **Триггер**                      **Формула**                          **Доказательство**
  PARTNER_LEAD_VERTICAL_SHARE    Partner          Lead assigned in vertical        50% Partner Profit/Margin            Lead record + margin verification
  PARTNER_LEAD_NON_VERTICAL      Partner          Lead outside vertical            30% Partner Profit/Margin            Lead record + margin verification
  PARTNER_PROJECT_ONBOARDING      Partner          Partner registers own project    1.5% × Fee Base (CapEx/Investment)   Project registration + deal docs
  PARTNER_DIRECT_INVESTOR_RECO   Partner          Direct investor recommendation   3% × Fee Base                        Introduction record + deal docs
  PARTNER_IO_ADS_REDUCED         Partner          Подписан IO + бюджет кампании    10% Partner Profit/Margin            IO + payment confirmed
  PARTNER_MARKETPLACE_EQUIP       Partner          Equipment sold via Marketplace   30% Equipment Margin                 Sales order + delivery + margin docs
  PARTNER_EPC_SALES_SPLIT        Partner          Works/EPC delivered              50/50 Works Margin                   Works contract + payment + margin audit
  PARTNER_OPEN_BOOK_PROC         Partner          Verified cost-base procurement   +9% works / +4% equipment            Cost base docs + procurement record
  --------------------------------- ---------------- -------------------------------- ------------------------------------ -----------------------------------------

**3.4 Internal / Agent**

  -------------------------- ----------------------- --------------------------------------- ------------------------------------------- -----------------------------------
  **Код**                    **Плательщик**          **Триггер**                             **Формула**                                 **Доказательство**
  TEAM_POOL_30             AITA → Team             Profit realized (pro-rata + reserves)   30% Profit of the Deal                      Evidence ledger + profit formula
  PROJECT_LEAD_20          AITA → Lead             DoD / realized profit + Digital-Only    20% Profit of the Deal                      DoD registry + proof of delivery
  AGENT_MARGIN_SHARE       AITA → Agent            Confirmed Transaction                   Агент 30→45→60% маржи; Рекрутер 50→35→20%   Payment confirm + auto-payout log
  MKTG_POOL_CONTRIBUTION   Marketing Pool Member   Оплата взноса в пул                     pool_contribution (param per Order Form)   Order Form / IO signed + payment
  -------------------------- ----------------------- --------------------------------------- ------------------------------------------- -----------------------------------

*Все коды потоков сохраняются при переходе к токенизации. PayWithFiat() или BuyCreditsThenPay() --- лишь обёртка поверх тех же кодов.*

**§4. RBAC --- Ролевая модель и сущности платформы**

Минимальный набор ролей, чтобы Corp OS работала. Базовые сущности: User, Company Workspace, Project Workspace, Deal Context, Partner Dashboard, Investor Workspace, Internal Deal Team.

**4.1 Пользователь (User)**

  ------------ --------------------------------------------------------------- ----------------------------------------
  **Роль**     **Описание**                                                    **Требования**
  Individual   Обычный физик; базовый доступ к профилю, CRM, задачам           Регистрация + NDA
  Agent        Физик с BUSINESS_VERIFIED; может получать регулярные выплаты   ФОП / Autónomo + Agent Agreement
  Recruiter    Строит сеть агентов; получает пассивный доход                   BUSINESS_VERIFIED + Partner Agreement
  ------------ --------------------------------------------------------------- ----------------------------------------

**4.2 Компания (Company Workspace)**

  ------------------------ ------------------------------------------------------------------ -------------------------
  **Роль**                 **Описание**                                                       **Ключевое право**
  Company Owner / Signer   Подписывает договоры, управляет доступами, платит                  Единственный подписант
  Company Admin            Управляет пользователями и правами                                 Не подписывает договоры
  Manager                  Ведёт проекты, воронки, сделки; создаёт заявки на платные модули   Read/write на проекты
  Worker                   Исполняет задачи, загружает документы, обновляет статусы           Upload + task execution
  ------------------------ ------------------------------------------------------------------ -------------------------

**4.3 Сделка (Deal Context / Deal Room)**

  ---------------------- ---------------------------------------------------------------------- --------------------------
  **Роль**               **Описание**                                                           **Договор**
  Project Lead           Ведёт контекст/DoD, отвечает за Digital-Only, 20% Profit of the Deal   Deal Execution Agreement
  Delivery Team Member   Участник пула 30%; исполняет задачи digital-only                       Team Agreement
  Founder / CEO Gate     Approval gates --- цены / обязательства / изменение сплитов            Все договоры
  ---------------------- ---------------------------------------------------------------------- --------------------------

**4.4 Партнёры и Инвесторы**

  ------------------------- --------------------------------------------- -------------------------------
  **Роль**                  **Контекст**                                  **Основной инструмент**
  Partner Owner             Владелец партнёрского аккаунта                Partner Dashboard
  Partner Sales             Продажи через Partner Dashboard; ведёт лиды   Partner Dashboard
  Partner PM                Управление проектами и исполнением            Partner Dashboard + Deal Room
  Investor Owner / Signer   Подписывает ISA, управляет портфелем          Investor Workspace
  Investor Analyst          Baseline Audit / Tracking / Screening         Investor Workspace (read)
  ------------------------- --------------------------------------------- -------------------------------

**§5. Маршруты взаимодействия**

Три главных сценария, через которые группы пользователей взаимодействуют внутри экосистемы AITA.

**Маршрут 01 --- Project → Capital → Execution (основной конвейер)**

  --------- ---------------------- ---------------------------------------------------------------------------------------------
  **Шаг**   **Актор**              **Действие / Результат**
  1         Developer              Размещает проект в AITA, загружает датарум, получает статус и верификацию
  2         AITA                   Matchmaking: даёт доступ / introductions инвесторам и контрагентам через платформу
  3         Investor               Получает проект, проходит baseline audit / tracking по ISA-пакету, принимает инвест-решение
  4         LOI → AITA             При подписании LOI включается эксклюзивность и защита цепочки introductions
  5         Internal Team / Lead   Структурирование, переговоры, контракты, KPI / аналитика --- digital-only
  6         Partners / EPC         Подключаются на исполнение / закупки через Partner Dashboard / open-book
  7         Closing                Наступают триггеры оплат по Cooperation / ISA / Partnership / Team
  --------- ---------------------- ---------------------------------------------------------------------------------------------

**Маршрут 02 --- Lead → Triage → Назначение владельца обработки**

  --------- ---------------------------------------------- --------------------------------------------------------------------------------------------
  **Шаг**   **Актор**                                      **Действие**
  1         Marketing Pool / Agents / Events / Referrals   Создают Lead, который фиксируется в AITA OS
  2         AITA OS                                        Классифицирует Lead: инвесторский → ISA; проектный → Cooperation; исполнение → Partnership
  3         AITA OS                                        Назначает лид по готовности / пропускной способности / allocation policy экосистемы
  --------- ---------------------------------------------- --------------------------------------------------------------------------------------------

*Назначение происходит не \"по персонализации\", а по правилам платформы --- справедливо и предсказуемо.*

**Маршрут 03 --- Investor-first (капитал приходит первым)**

  --------- -------------- ----------------------------------------------------------------------------------
  **Шаг**   **Актор**      **Действие**
  1         Investor       Заходит на платформу, выбирает пакет ISA
  2         AITA           Подбирает проекты из пайплайна (Developer supply); baseline screening / tracking
  3         Deal Context   Запускается стандартный конвейер: Team/Lead + Partner execution
  --------- -------------- ----------------------------------------------------------------------------------

**§6. Управляющие правила (чтобы система не разваливалась)**

Пять принципов, которые обеспечивают работоспособность всей экосистемы AITA как единого организма.

  -------- -------------------------------- ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- -------------------------------------------
  **\#**   **Правило**                      **Описание**                                                                                                                                                                                          **Источник**
  1        Developer leads                  Девелопер по умолчанию ведёт проект операционно и коммерчески. AITA даёт платформу, верификацию, introductions и учёт доказательств --- но не перехватывает управление.                               Cooperation Agreement §Developer leads
  2        Exclusivity включается на LOI    До LOI риск \"увода\" инвестора есть. AITA фиксирует lead как AITA Lead и защищает non-circumvention (24 мес.). Эксклюзивность возникает только при подписании LOI с AITA Investor.                   Cooperation Agreement §Exclusivity
  3        Digital-Only + Evidence Ledger   Всё исполнение делается и фиксируется в AITA Platform. Если не в AITA --- \"неверифицируемо\" → может не оплачиваться. Логи + таймстемпы + approvals = юридическое доказательство.                    Deal Execution Agreement + Team Agreement
  4        Approval Gates                   Юридические и финансовые обязательства --- только через approvals Founder/CEO, записанные в AITA. Без gate нельзя: подписывать договоры, изменять сплиты, принимать новые финансовые обязательства.   Все договоры экосистемы
  5        Partner Dashboard                Партнёр обязан вести лиды и проекты через платформу. Если работа вне платформы --- обязателен upload summary и доказательств. Иначе комиссия не начисляется.                                          Partnership Agreement
  -------- -------------------------------- ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- -------------------------------------------

**§7. Revenue Matrix --- 22 источника дохода**

Полная карта всех revenue streams AITA. Каждая строка --- отдельный источник с уникальным кодом, триггером и договором.

  -------- ----------------------------------- ------------ ------------- ------------------------- ---------------------
  **\#**   **Billing Code**                    **IN/OUT**   **Ставка**    **База**                  **Договор**
  0        PRE_SALE_ACCESS                   IN           €500/место    Per seat                  Platform T&C
  1        DEV_FREE_LISTING                  ---          €0            2 проекта                 Cooperation Agr.
  2        DEV_COMMERCIAL_PACKAGE            IN           Annex/прайс   Subscription              Cooperation Agr.
  3        DEV_SUCCESS_FEE_CAPEX            IN           2.7%          Total CapEx Deal Volume   Cooperation Agr.
  4        DEV_SUCCESS_FEE_DEVSTAGE         IN           5.0%          Development Deal Value    Cooperation Agr.
  5        DEV_INVESTOR_ADVERTISING_ORDER   IN           SOW           Per Order Form            Cooperation Agr.
  6        ISA_PKG_A_MATCHING_FEE          IN           1.5%          Investment Amount         ISA
  7        ISA_PKG_B_RETAINER               IN           €4 000/мес    Monthly (20 hrs)          ISA
  8        ISA_PKG_B_EXECUTION_FEE         IN           1.0%          Investment Amount         ISA
  9        ISA_PLATFORM_TRANSACTION_FEE     IN           0.4%          Gross transaction value   ISA
  10       ISA_PKG_C_MANAGEMENT_FEE        IN           10%           Per Term Sheet            ISA
  11       ISA_PKG_D_SCREENING              IN           \$15/проект   Per project               ISA
  12       PARTNER_LEAD_VERTICAL_SHARE      IN           50%           Partner Profit/Margin     Partnership Agr.
  13       PARTNER_LEAD_NON_VERTICAL        IN           30%           Partner Profit/Margin     Partnership Agr.
  14       PARTNER_PROJECT_ONBOARDING        IN           1.5%          Fee Base (CapEx)          Partnership Agr.
  15       PARTNER_DIRECT_INVESTOR_RECO     IN           3.0%          Fee Base                  Partnership Agr.
  16       PARTNER_IO_ADS_REDUCED           IN           10%           Partner Profit/Margin     Partnership Agr.
  17       PARTNER_MARKETPLACE_EQUIP         IN           30%           Equipment Margin          Partnership Agr.
  18       PARTNER_EPC_SALES_SPLIT          IN           50/50         Works Margin              Partnership Agr.
  19       PARTNER_OPEN_BOOK_PROC           IN           +9%/+4%       Cost Base                 Partnership Agr.
  20       TEAM_POOL_30                      OUT          30%           Profit of the Deal        Team Agreement
  21       PROJECT_LEAD_20                   OUT          20%           Profit of the Deal        Lead Agreement
  ---      (AITA Retained)                     ---          50%           Profit of the Deal        Все договоры
  22       AGENT_MARGIN_SHARE (AITA side)    ---          20%           Маржа на сделке           Agent Agreement
  \+       MKTG_POOL_CONTRIBUTION            IN           param         Per Order Form/IO         POLICY / Order Form
  -------- ----------------------------------- ------------ ------------- ------------------------- ---------------------

*Marketing Pool: LaaS €30/лид и Landing Page €1 500 --- устарели (FF:disable_landing_pages). Текущая модель --- пайевой взнос в пул + allocation policy + опционально success fee 1.5%.*

**§8. Billing Policy**

**8.1 Waterfall (Profit of the Deal)**

  --------------------------- ---------- ----------------------------------------------
  **Участник**                **Доля**   **Правило**
  Project Lead                20%        Lead Success Fee --- за лидерство по сделке
  Team Pool (self-governed)   30%        Распределяется командой, pro-rata по участию
  AITA Retained               50%        Платформа + операционные расходы
  ИТОГО                       100%       20% + 30% + 50% = 100% Profit of the Deal
  --------------------------- ---------- ----------------------------------------------

**8.2 Reserve (Project Lead)**

До 10% выплаты Project Lead может удерживаться в резерве на 90--180 дней --- страховой резерв до финализации proof of delivery. Освобождается после подтверждения DoD в AITA Platform.

**8.3 Anti-Double Monetization**

  ----------------------- -------------------------------------------------------------------------------------------------------------------------------------------------
  **Правило**             **Описание**
  SaaS-only Mode          Workspace-only: success fees не применяются. Два режима взаимно исключают друг друга по умолчанию.
  Deal-enabled Mode       Если участник активирует deal-flow через платформу --- применяются % сборы. Переключение требует явного согласия.
  No Stacking (default)   Один сервис = один fee. Запрет применения нескольких fees к одной транзакции без раскрытия.
  Исключение              Стороны по разным договорам могут получать fees за одну сделку (Developer 2.7% + Investor ISA 1.5%) --- каждая является отдельным контрагентом.
  ----------------------- -------------------------------------------------------------------------------------------------------------------------------------------------

**8.4 Лимит выплат физическому лицу**

Не более 2 выплат физическому лицу без статуса BUSINESS_VERIFIED. После второй выплаты платформа авто-триггерит upgrade_to_business_required. Регулярная деятельность --- только через ФОП / Autónomo / юридическое лицо.

**§9. Token-Ready архитектура**

Без выпуска токена архитектура уже готова к конвертации. Единый Ledger: каждая оплата = Invoice + Payment + Evidence. Коды потоков остаются теми же при любом режиме оплаты.

  ---------- --------------- ---------------- -----------------------------------------------------------------------------------------------------------------------------------------------------------
  **Фаза**   **Название**    **Статус**       **Описание**
  Phase 0    Credits Layer   Текущая (2026)   Внутренняя единица. Credits начисляются за верифицированные действия. Используются для скидок, приоритета, распределения задач. Не финансовый инструмент.
  Phase 1    Token Wrapper   Планируется      Credits оборачиваются в utility token на блокчейне. Не ценная бумага. Требует юридической экспертизы в юрисдикции запуска.
  Phase 2    Utility Token   Будущее          Полноценный utility token: governance, льготный доступ к ликвидности, партнёрские программы. Secondary market --- при регуляторном статусе.
  ---------- --------------- ---------------- -----------------------------------------------------------------------------------------------------------------------------------------------------------

**Принцип токен-совместимости**

  ----------------------------------------------------- ---------------------------------------------------------------
  **Сейчас**                                            **После добавления токена**
  PayWithFiat(DEV_SUCCESS_FEE_CAPEX, 2.7%, amount)   PayWithFiat() ИЛИ BuyCreditsThenPay() --- код остаётся тем же
  Все billing codes зафиксированы                       Коды не меняются --- только добавляется слой оплаты
  ----------------------------------------------------- ---------------------------------------------------------------

*Credits НЕ являются токенами, криптовалютой или ценными бумагами. Переход к Phase 1--2 требует отдельного юридического решения.*

*AITA WORLD, S.L. · Монетизация v2.0 · Март 2026*

*Приоритет: Единая таблица монетизации AITA · Дополнение: Архитектура экосистемы v2 + договоры (Profiles 1--8)*


---

# ═══ ECOSYSTEM ARCHITECTURE (EN) ═══

**AITA WORLD, S.L.**

**АРХИТЕКТУРА ДОГОВОРНОЙ ЭКОСИСТЕМЫ**

*Цепочка услуг · Цепочка ценности · Монетизация · Собственные проекты · Анализ рисков*

*Подготовлено: март 2026 \| Версия: 2.0 \| Статус: рабочий документ*

**ОГЛАВЛЕНИЕ --- ВСЕ РАЗДЕЛЫ И УСЛУГИ**

**§0 ПРЕДПРОДАЖНЫЙ ДОСТУП К ПЛАТФОРМЕ**

> Ограниченный invite-only доступ \| €500 за место + фирменная футболка AITA

**ЧАСТЬ I --- ВНЕШНЯЯ (Коммерческие условия)**

**§1 ОБЗОР ДОГОВОРНОЙ ЭКОСИСТЕМЫ**

> 7 документов экосистемы: NDA · Cooperation · ISA · Partnership · Team · Deal Execution · Cooperation (Developer)

**§2 ЦЕПОЧКА УСЛУГ (SERVICE CHAIN) --- 6 этапов**

> 2.1 Sourcing & Listing · 2.2 Investor Onboarding · 2.3 Matching & Introduction
>
> 2.4 Deal Structuring & Negotiation · 2.5 Execution & Procurement · 2.6 Closing & Settlement

**§3 ЦЕПОЧКА ЦЕННОСТИ (VALUE CHAIN)**

> 3.1 Первичные активности: Project Sourcing · Capital Sourcing · Matching · Deal Execution · Procurement & EPC
>
> 3.2 Поддерживающие активности: Platform & Technology · Compliance · IP & Brand · Governance & Control

**§4 СВОДНАЯ МАТРИЦА МОНЕТИЗАЦИИ**

> 17 источников дохода: Success Fees · Advisory Retainer · Deal Execution Fee · Platform Transactions · Co-Invest · Compliance Screening · Leads · Marketplace · EPC Sales · Marketing Engine

**§5 СОБСТВЕННЫЕ ПРОЕКТЫ --- AITA КАК ИНИЦИАТОР**

> 5.1 Обзор модели · 5.2 Reality Gates · 5.3 Эксклюзивность и срок
>
> 5.4 Контрольные точки · 5.5 Экономика: Upside Sharing · 5.6 Водопад распределения · 5.7 Неокружение

**ЧАСТЬ II --- ВНУТРЕННЯЯ (Операционная база)**

**§6 COOPERATION AGREEMENT (DEVELOPER) --- АНАЛИЗ**

> 6.1 Позиционирование · 6.2 Ключевые условия (ставки, сроки, гарантии)

**§7 ЗОНЫ РИСКА ДЛЯ AITA**

> 7.1 Риски Cooperation Agreement · 7.2 Системные риски экосистемы

**§8 ПРОБЕЛЫ И РЕКОМЕНДАЦИИ**

> 8.1 Доработки Cooperation Agreement · 8.2 Рекомендации по экосистеме · 8.3 Двойная монетизация

**§9 АГЕНТСЬКА МЕРЕЖА (AGENT NETWORK ENGINE)**

> 9.1 Суть моделі · 9.2 Механіка розподілу маржі · 9.3 Рівні агента · 9.4 Ланцюжок послуг
>
> 9.5 Пасивний дохід рекрутера · 9.6 Договірна база · 9.7 Інтеграція з екосистемою

**§10 МАРКЕТИНГОВИЙ БЛОК (MARKETING ENGINE)**

> 10.1 Суть маркетингової моделі · 10.2 Склад послуг та цінова модель
>
> 10.3 Структура доходу · 10.4 Воронка клієнта · 10.5 Інтеграція з агентською мережею · 10.6 Договірна база

**§0 ПРЕДПРОДАЖНЫЙ ДОСТУП К ПЛАТФОРМЕ**

*Pre-Sale Access to AITA Platform \| Invite-Only \| Limited Cohort*

AITA работает по invite-only модели. Доступ к платформе ограничен верифицированными участниками, прошедшими квалификационный отбор. В связи с ограниченным количеством инвайтов AITA предлагает программу предпродажного доступа для приоритетной очереди.

  ------------------------ -------------------------------------------------------------------------------------------------------------
  **Параметр**             **Условия**
  **Стоимость доступа**    €500 за место (единоразово, невозвратно)
  **Включено**             Полный доступ к платформе (role-based) + фирменная футболка AITA + welcome pack
  **Модель приглашений**   Strictly invite-only; каждое место привязано к конкретному пользователю и компании
  **Активация**            Доступ активируется после подтверждения оплаты; действует на весь срок соглашения
  **Ограничение мест**     Ограниченное число мест на когорту --- AITA оставляет за собой право закрыть набор в любой момент
  **Возврат**              Не возвращается; плата за доступ покрывает онбординг, provisioning платформы и мерч
  **Приоритет**            Участники pre-sale получают приоритетный доступ к будущим раундам портфеля и расширенным функциям платформы
  ------------------------ -------------------------------------------------------------------------------------------------------------

0.1 Плата за предпродажный доступ является коммерческим взносом за доступ и не является инвестицией, депозитом или обязательством по какому-либо конкретному проекту. Она дает участнику право просматривать, оценивать и взаимодействовать с проектами на Платформе AITA в рамках ролевых разрешений.

0.2 AITA по своему усмотрению может предлагать рекламные цены, скидки для ранних пользователей или отменять плату за доступ для стратегических партнеров.

0.3 Фирменная футболка и welcome pack AITA отправляются в течение 15 рабочих дней после подтверждения доступа и являются частью процесса онбординга участника.

**ЧАСТЬ I**

**ВНЕШНЯЯ --- Коммерческие условия, цепочки, монетизация, собственные проекты**

**1. ОБЗОР ДОГОВОРНОЙ ЭКОСИСТЕМЫ**

Договорная база AITA охватывает 7 документов, каждый из которых регулирует отношения с определенным типом контрагента. Вместе они формируют замкнутую экосистему, в которой AITA выступает центральным узлом --- платформой, соединяющей проектных девелоперов, инвесторов, партнеров-исполнителей и внутренние команды.

  ------- ---------------------------------- ------------------------ -------------------------------------------------------------- ------------------------------------------------------------------------
  **№**   **Документ**                       **Контрагент**           **Роль в экосистеме**                                          **Ключевое обязательство AITA**
  **1**   **NDA (UA)**                       Любой (UA рынок)         Защита информации до входа в экосистему                        Конфиденциальность 3 года + бессрочно для know-how
  **2**   **Cooperation Agreement**          Девелопер проектов       Вход проектов в платформу; matchmaking с инвесторами           Листинг, верификация, matchmaking, маркетинг инвесторам
  **3**   **Investor Services Agreement**    Инвестор / Фонд          Вход капитала; sourcing проектов для инвестора                 Matching, baseline audit, deal tracking, legal coordination, co-invest
  **4**   **Partnership Agreement**          EPC / Поставщик          Исполнение проектов; оборудование; works/EPC через платформу   Lead distribution, marketplace, procurement, продажа works клиентам
  **5**   **Team Agreement**                 Delivery-команда         Исполнение сделок силами команды (30% profit pool)             Платформа, governance, advisory support, approval gates
  **6**   **Deal Execution Agreement**       Project Lead             Лидерство по конкретной сделке (20% + 30% pool)                Product-Only Exception, advisory 45 мин/день, next case
  **7**   **Cooperation Agr. (Developer)**   Девелопер (энергетика)   Листинг проектов, эксклюзивность, success fees                 Платформа, верификация, matchmaking, investor advertising
  ------- ---------------------------------- ------------------------ -------------------------------------------------------------- ------------------------------------------------------------------------

**2. ЦЕПОЧКА УСЛУГ (SERVICE CHAIN)**

Цепочка услуг AITA --- это последовательность сервисов, которые компания предоставляет на каждом этапе жизненного цикла энергетического проекта. Каждый этап связан с конкретным договором и конкретным контрагентом.

**Этап 1: Sourcing & Listing (Привлечение и листинг проектов)**

+------------------------------+----------------------------------------------------------------------------------------------------------------------+
| **Договор:**                 | **Контрагент:** Девелопер проектов (PV, BESS, hybrid, C&I, grid-scale)                                               |
|                              |                                                                                                                      |
| Cooperation Agreement        |                                                                                                                      |
+------------------------------+----------------------------------------------------------------------------------------------------------------------+
| **Услуги AITA:**             | -   Предоставление платформы и листинг-воркфлоу                                                                      |
|                              |                                                                                                                      |
|                              | -   Верификация, структурирование и скоринг данных проекта                                                           |
|                              |                                                                                                                      |
|                              | -   Присвоение статусов: Draft → Verified → Published → Restricted → Archived                                        |
|                              |                                                                                                                      |
|                              | -   2 бесплатных листинга (basic card, document upload, completeness checks)                                         |
|                              |                                                                                                                      |
|                              | -   Коммерческие пакеты: стратегия, tracking, advanced reporting, investor advertising (с 3-го проекта)              |
+------------------------------+----------------------------------------------------------------------------------------------------------------------+
| **Ценность для девелопера:** | Доступ к платформе с инвесторской базой; профессиональная упаковка проекта; повышение доверия через верификацию AITA |
+------------------------------+----------------------------------------------------------------------------------------------------------------------+

**Этап 2: Investor Onboarding (Подключение инвесторов)**

+-----------------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------+
| **Договор:**                      | **Контрагент:** Инвестор, фонд, family office, институциональный игрок                                                                                      |
|                                   |                                                                                                                                                             |
| ISA (Investor Services Agreement) |                                                                                                                                                             |
+-----------------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------+
| **Услуги AITA:**                  | -   Package A: Matching + Baseline Audit + Tracking + Legal Coordination (1.5%)                                                                             |
|                                   |                                                                                                                                                             |
|                                   | -   Package B: Advisory Retainer EUR 4,000/мес + Deal Execution + Platform Transactions (1% + 0.4%)                                                         |
|                                   |                                                                                                                                                             |
|                                   | -   Package C: Co-Investment в AITA-originated проекты (management fee 10%)                                                                                 |
|                                   |                                                                                                                                                             |
|                                   | -   Package D: Bank/Institutional Compliance Screening (\$15/проект)                                                                                        |
+-----------------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------+
| **Ценность для инвестора:**       | Доступ к верифицированным проектам; снижение risk exposure через baseline audit; deal tracking и legal coordination «под ключ»; co-investment opportunities |
+-----------------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------+

**Этап 3: Matching & Introduction (Сведение сторон)**

+---------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| **Договоры:**                   | **Функция платформы:** AITA соединяет проекты (supply) с капиталом (demand) и исполнителями (execution)                                                                                          |
|                                 |                                                                                                                                                                                                  |
| Cooperation + ISA + Partnership |                                                                                                                                                                                                  |
+---------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| **Услуги AITA:**                | -   Matchmaking: introductions, access к инвесторам, EPCs, suppliers, advisors                                                                                                                   |
|                                 |                                                                                                                                                                                                  |
|                                 | -   Investor advertising: campaigns, platform pools, roadshows, targeted intros                                                                                                                  |
|                                 |                                                                                                                                                                                                  |
|                                 | -   Lead generation и distribution (leads → партнерам / девелоперам)                                                                                                                             |
|                                 |                                                                                                                                                                                                  |
|                                 | -   Non-circumvention enforcement: защита цепочки introductions                                                                                                                                  |
+---------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| **Критическая точка:**          | Именно на этом этапе AITA создает основную ценность --- соединение сторон. Эксклюзивность по Cooperation Agreement возникает только при подписании LOI. До LOI девелопер может увести инвестора. |
+---------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+

**Этап 4: Deal Structuring & Negotiation (Структурирование сделки)**

+-----------------------------------------------+-------------------------------------------------------------------------------------------------------------------------------------------+
| **Договоры:**                                 | **Исполнители:** Внутренняя команда AITA (delivery team / project lead)                                                                   |
|                                               |                                                                                                                                           |
| Team + Project Lead + Cooperation (опция §10) |                                                                                                                                           |
+-----------------------------------------------+-------------------------------------------------------------------------------------------------------------------------------------------+
| **Услуги AITA:**                              | -   Подготовка negotiation materials, agendas, minutes, follow-ups                                                                        |
|                                               |                                                                                                                                           |
|                                               | -   Drafting и negotiating contract terms                                                                                                 |
|                                               |                                                                                                                                           |
|                                               | -   SPV structuring, financial model, PPA logic, tendering                                                                                |
|                                               |                                                                                                                                           |
|                                               | -   Permitting support, engineering concept, feasibility/TEO                                                                              |
|                                               |                                                                                                                                           |
|                                               | -   KPI dashboards, pilot evidence, analytics pack                                                                                        |
+-----------------------------------------------+-------------------------------------------------------------------------------------------------------------------------------------------+
| **Модель оплаты команды:**                    | Team Agreement: 30% от Profit of the Deal (self-governed pool). Project Lead: 20% Lead Success Fee + 30% team pool. AITA: оставшиеся 50%. |
+-----------------------------------------------+-------------------------------------------------------------------------------------------------------------------------------------------+

**Этап 5: Execution & Procurement (Исполнение и закупки)**

+-----------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------+
| **Договор:**          | **Контрагент:** EPC-подрядчик, поставщик оборудования (gas turbine, BESS, hybrid)                                                                              |
|                       |                                                                                                                                                                |
| Partnership Agreement |                                                                                                                                                                |
+-----------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------+
| **Услуги AITA:**      | -   Lead distribution: 50% profit/margin за leads в Partner Vertical, 30% за outside                                                                           |
|                       |                                                                                                                                                                |
|                       | -   Marketplace distribution оборудования партнера (30% Equipment Margin)                                                                                      |
|                       |                                                                                                                                                                |
|                       | -   Продажа Partner Works/EPC клиентам (50/50 profit split)                                                                                                    |
|                       |                                                                                                                                                                |
|                       | -   Open-Book procurement: Works +9%, Equipment +4% norm margin                                                                                                |
|                       |                                                                                                                                                                |
|                       | -   Advertising-funded leads (10% profit share при IO)                                                                                                         |
+-----------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------+
| **Контроль:**         | Partner Dashboard: lead assignment, status tracking, monetization reporting, commission calculations. Platform может менять conditions с уведомлением 50 дней. |
+-----------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------+

**Этап 6: Closing & Settlement (Закрытие сделки и расчеты)**

  ------------------ ----------------------------------------------------------------------------------------------------------------------------------------------------------------------
  **Все договоры**   **Триггеры оплаты AITA:**
  **Cooperation:**   Success fee при подписании definitive agreements или получении consideration. CapEx stage: 2.7% от Total CapEx Deal Volume. Dev stage: 5% от Development Deal Value.
  **ISA:**           Package A: 1.5% от Investment Amount при closing. Package B: EUR 4,000/мес retainer + 1% + 0.4% platform transactions. Package C: 10% management fee.
  **Partnership:**   Доля AITA от profit/margin: 50% (vertical leads), 30% (non-vertical), 30% (equipment), 50/50 (EPC sales). Open-Book: +9%/+4% norm margins.
  **Team / Lead:**   AITA удерживает 50% Profit of the Deal (после выплаты 20% Project Lead + 30% team pool). Выплаты pro-rata по мере реализации profit.
  ------------------ ----------------------------------------------------------------------------------------------------------------------------------------------------------------------

**3. ЦЕПОЧКА ЦЕННОСТИ (VALUE CHAIN)**

Цепочка ценности показывает, как AITA создает, аккумулирует и монетизирует ценность на каждом уровне экосистемы. AITA работает как двусторонняя платформа (two-sided marketplace): привлекает проекты со стороны предложения и капитал со стороны спроса, зарабатывая на каждой стороне транзакции.

**3.1 Первичные активности (Primary Activities)**

  ----------------------- --------------------------------------------------------------------------------- --------------------------------------------------------------------- --------------------------------------------------------------------
  **Активность**          **Что делает AITA**                                                               **Какую ценность создает**                                            **Как монетизирует**
  **Project Sourcing**    Привлекает девелоперов на платформу; принимает и верифицирует проекты             Формирует deal flow --- пайплайн верифицированных проектов            2 бесплатных листинга → Commercial Packages с 3-го проекта
  **Capital Sourcing**    Привлекает инвесторов; предлагает пакеты услуг (A/B/C/D); compliance screening    Формирует investor pool --- базу квалифицированных инвесторов         ISA fees: 1.5% matching + retainer EUR 4K/мес + 10% management fee
  **Matching**            Соединяет проекты с инвесторами, EPC, suppliers; ведет introductions и workflow   Снижает friction --- ускоряет сделки; создает trust через платформу   Coop: 2.7% CapEx / 5% Dev. Partnership: 1.5% или 3% Fee Base
  **Deal Execution**      Структурирует сделки; ведет переговоры; юридическая координация; SPV              Доводит сделки до closing; минимизирует execution risk                Team/Lead: AITA получает 50% Profit of the Deal
  **Procurement & EPC**   Организует закупки через платформу; продает works/EPC партнеров клиентам          Контролирует execution chain; обеспечивает качество через Open-Book   50/50 EPC margin; 30% Equipment; Open-Book +9%/+4%
  ----------------------- --------------------------------------------------------------------------------- --------------------------------------------------------------------- --------------------------------------------------------------------

**3.2 Поддерживающие активности**

  ---------------------------- -----------------------------------------------------------------------------------------------------------------------------------------------------------------------------
  **Активность**               **Описание**
  **Platform & Technology**    AITA Platform: листинг, верификация, data room, workflow, dashboards, analytics, KPI tracking. Является обязательным инструментом (Digital-Only principle) для всех сделок.
  **Compliance & Screening**   AML/KYC, sanctions screening, bank readiness checks (Package D ISA). GDPR/LOPDGDD data protection. NDA protection pre-engagement.
  **IP & Brand**               Платформенные методологии, scoring algorithms, workflow logic --- защищены через non-competition clauses во всех договорах. Бренд AITA как знак качества верификации.
  **Governance & Control**     Approval Gates (Founder/CEO) для всех финансовых/юридических обязательств. Версионирование в платформе = юридическое доказательство. Non-circumvention enforcement.
  ---------------------------- -----------------------------------------------------------------------------------------------------------------------------------------------------------------------------

**4. СВОДНАЯ МАТРИЦА МОНЕТИЗАЦИИ**

Ниже --- полная карта источников дохода AITA по всем договорам. Каждая строка = отдельный revenue stream.

  ------------------------------ ------------- ------------------------------------------------------ --------------- ------------------------------
  **Источник дохода**            **Договор**   **База расчета**                                       **Ставка**      **Триггер**
  Success Fee (CapEx stage)      Cooperation   Total CapEx Deal Volume (EPC, equipment, grid, etc.)   **2.7%**        Definitive agreements signed
  Success Fee (Dev stage)        Cooperation   Development Deal Value (rights/package)                **5%**          Definitive agreements signed
  Commercial Packages            Cooperation   Subscription / purchase                                **Annex 1/4**   С 3-го проекта
  Matching Fee (Pkg A)           ISA           Investment Amount                                      **1.5%**        Closing / first tranche
  Advisory Retainer (Pkg B)      ISA           Monthly (20 hrs cap)                                   **EUR 4,000**   Ежемесячно
  Deal Execution Fee (Pkg B)     ISA           Investment Amount                                      **1.0%**        Closing
  Platform Transaction Fee       ISA           Gross transaction value                                **0.4%**        Platform purchase
  Co-Invest Management (Pkg C)   ISA           Per Project Term Sheet                                 **10%**         Per term sheet
  Compliance Screening (Pkg D)   ISA           Per project                                            **\$15**        Report delivery
  Lead (in Vertical)             Partnership   Partner Profit/Margin                                  **50%**         Payment / binding agr.
  Lead (outside Vertical)        Partnership   Partner Profit/Margin                                  **30%**         Payment / binding agr.
  Project Matching Fee           Partnership   Fee Base (CAPEX/Investment/Contract)                   **1.5%**        Transaction close
  Investor Recommendation        Partnership   Fee Base                                               **3%**          Funding/transaction
  Equipment Marketplace          Partnership   Equipment Profit/Margin                                **30%**         Sale concluded
  EPC/Works Sales                Partnership   Works/EPC Profit/Margin                                **50/50**       Sale concluded
  Advertising Leads              Partnership   Partner Profit/Margin                                  **10%**         IO + budget paid
  AITA Retained Profit           Team / Lead   Profit of the Deal                                     **50%**         Profit realized
  ------------------------------ ------------- ------------------------------------------------------ --------------- ------------------------------

**5. СОБСТВЕННЫЕ ПРОЕКТЫ --- AITA КАК ИНИЦИАТОР**

Помимо роли платформы-посредника, AITA самостоятельно инициирует, разрабатывает и управляет собственными энергетическими проектами. В этой модели AITA выступает оригинатором --- привлекая внешних партнеров по капиталу (Capital Arranger) для финансирования пайплайна под управлением платформы. Все взаимодействие ведется исключительно через AITA Platform как единственный источник истины.

**5.1 Обзор модели и пайплайн**

  --------------------------- ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
  **Параметр**                **Описание**
  **Роль AITA**               Оригинатор + оператор платформы: AITA владеет правами на проекты, управляет верификацией, тендерингом, структурированием сделок
  **Роль Capital Arranger**   Привлечение финансирования: equity и debt, координация с банками, инвесторами, фондами. Работает строго через AITA Platform.
  **Приоритетный пайплайн**   Целевой объем: €120,000,000 стоимости проектов. Цель: обеспечить 20% equity. Горизонт: 2026--2027.
  **Условие запуска**         5 критериев цепочки исполнения: (а) права на проект; (б) техническая и юридическая верификация; (в) конкурентный тендер (min 3 подрядчика); (г) маршрут монетизации; (д) O&M оператор
  **Платформа**               AITA Platform --- единственная операционная среда и источник истины. Все логи, таймстемпы, одобрения образуют Evidence Ledger.
  --------------------------- ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

**5.2 Reality Gates --- обязательные фильтры**

Перед тем как проект переходит в фазу привлечения финансирования, Capital Arranger обязан пройти оба фильтра реальности. Без их прохождения проект не открывается для исполнения.

  -------------------------- ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
  **Gate**                   **Требование**
  **Proof of Funds (PoF)**   Документальное подтверждение реального капитала: исполненный мандат, обязывающее commitment letter, одобренный term sheet, одобрение кредитного комитета или подписка инвестора --- загружено в AITA Platform.
  **B2B Package**            Минимально банкируемая цепочка контрактов/условий (EPC/O&M/offtake/buyer/insurance/grid/land) или письменный план с доказательством финализации в сроки Digital Annex.
  **Важно**                  \"Мягкий интерес\", предварительные обсуждения или непроверенные индикации инвесторов НЕ считаются Proof of Funds. AITA вправе приостановить проект без обязательств, если Reality Gates не пройдены.
  -------------------------- ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

**5.3 Эксклюзивность и срок**

Срок соглашения: 24 месяца. В первые 6 месяцев Capital Arranger получает эксклюзивность по привлечению финансирования для проектов в Digital Annexes без retainer-fee --- при условии соблюдения Reality Gates и контрольных точек. Нарушение контрольных точек по 2 проектам за любые 90 дней влечет немедленное прекращение эксклюзивности для всего пайплайна.

**5.4 Контрольные точки исполнения (Performance Milestones)**

  ----------------------- ------------- --------------------------------------------------------------------------------------------------------------------------------------
  **Контрольная точка**   **Дедлайн**   **Требование**
  **Kick-off**            5 р.д.        Capital Arranger подтверждает стратегию финансирования, целевой пул инвесторов/кредиторов и ответственного ведущего в AITA Platform.
  **Proof of Funds**      30 дней       Capital Arranger загружает Proof of Funds в AITA Platform.
  **Term Sheet**          45 дней       Capital Arranger загружает минимум один actionable term sheet или binding commitment инвестора.
  **Closing Plan**        60 дней       Capital Arranger публикует реалистичный closing plan (условия закрытия, таймлайн, документы, ответственные) в AITA Platform.
  ----------------------- ------------- --------------------------------------------------------------------------------------------------------------------------------------

**5.5 Экономика: Upside Sharing**

Экономическая модель собственных проектов основана на разделении Upside Spread --- чистой ценности, образующейся между доходностью проекта и стоимостью капитала. Принцип: no closing --- no fee. Скрытые комиссии запрещены.

  ------------------------------ -----------------------------------------------------------------------------------------------------------------------------------------------------------------------
  **Параметр**                   **Условия**
  **Разделение Upside Spread**   50% AITA / 50% Capital Arranger --- рассчитывается по каждому проекту или портфелю, указывается в Digital Annex.
  **Нераскрытые комиссии**       Любая комиссия, не раскрытая и не зафиксированная в AITA Platform, НЕ включается в Cost of Funds и несется Capital Arranger.
  **Cost of Funds**              Полная эффективная стоимость капитала: base rate, margin, fees, commissions, hedging, OID, arranger/placement fees. Раскрывается в AITA Platform при каждом закрытии.
  **Споры по Cost of Funds**     При разногласиях назначается независимый финансовый эксперт (по взаимному согласию); расходы делятся поровну, если не выявлено существенного искажения.
  ------------------------------ -----------------------------------------------------------------------------------------------------------------------------------------------------------------------

**5.6 Водопад распределения (Portfolio Waterfall)**

Денежные потоки портфеля распределяются в следующей очередности, если Digital Annex не предусматривает иное в связи с требованиями банков:

  ------------- ----------------------------------------------------------------------------------------------
  **Уровень**   **Назначение**
  **(а)**       Обслуживание старшего долга и банковские ковенанты (проценты, основной долг, комиссии)
  **(б)**       Возврат инвестору / preferred return (по применимости)
  **(в)**       Операционные резервы, compliance и существенные проектные обязательства
  **(г)**       Реинвестирование в проекты и/или совместную инфраструктуру до достижения Phase 1 sufficiency
  **(д)**       После Phase 1: оставшийся распределяемый cash --- по правилам Upside Sharing и Digital Annex
  ------------- ----------------------------------------------------------------------------------------------

**5.7 Неокружение (Non-Circumvention)**

В течение срока соглашения и 24 месяцев после его окончания ни одна из сторон не вправе прямо или косвенно обходить другую сторону, вступая в отношения с Protected Parties (контрагентами, введенными через платформу) с целью избежать соглашения или лишить другую сторону экономической выгоды.

При нарушении нарушившая сторона уплачивает ликвидированные убытки в размере экономической выгоды, которую получила бы другая сторона (включая 50% Upside Spread), плюс расходы на enforcement. Применимое право: England & Wales.

**ЧАСТЬ II**

**ВНУТРЕННЯЯ --- Операционная база, риски, рекомендации, сетевые модели**

**6. COOPERATION AGREEMENT (DEVELOPER) --- АНАЛИЗ**

**6.1 Позиционирование в экосистеме**

Cooperation Agreement --- это «входные ворота» для проектов в экосистему AITA. Без этого договора платформа не получает deal flow. Это договор со стороны предложения (supply side), в то время как ISA работает со стороны спроса (demand side). Вместе они формируют two-sided marketplace.

**6.2 Ключевые условия**

  ------------------------- ------------------------------------------------------------------------------------------------------
  **Параметр**              **Условие**
  **Принцип**               \"Developer leads\" --- девелопер ведет проекты операционно и коммерчески
  **Free Listing**          2 проекта бесплатно (basic card, upload, completeness checks)
  **Эксклюзивность**        Начинается ТОЛЬКО при подписании LOI с AITA Investor. До LOI --- лишь good faith + non-circumvention
  **Success Fee (CapEx)**   2.7% от Total CapEx Deal Volume (EPC, equipment, grid, engineering, etc.)
  **Success Fee (Dev)**     5% от Development Deal Value (development rights/package)
  **Non-circumvention**     24 месяца после последнего introduction/contact по проекту
  **Срок**                  12 месяцев, auto-renew. Cure period: 15 дней. Tail: 24 месяца для introductions
  **Equity option (§10)**   AITA может получить equity/profit share за доп. работу (permitting, SPV, TEO, financial model)
  **Liability cap**         Fees actually received за последние 6 месяцев по конкретному проекту
  **Governing law**         Spain. Jurisdiction: \[Courts of Bilbao/Madrid\] или arbitration --- не выбрано
  ------------------------- ------------------------------------------------------------------------------------------------------

**7. ЗОНЫ РИСКА ДЛЯ AITA**

**7.1 Cooperation Agreement (Developer) --- критичные риски**

  ------- -------------------------------------- -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- -----------------------------------------------------------------------------------------------------------------------------------
  **№**   **Риск**                               **Описание**                                                                                                                                                                     **Рекомендация**
  **1**   **Pre-LOI circumvention**              До LOI эксклюзивности нет. Девелопер может познакомиться с инвестором через AITA и закрыть сделку напрямую. Non-circumvention (§9) работает, но доказать его нарушение сложно.   Добавить engagement fee или retainer за верификацию. Ввести \"AITA introduction notice\" = формальное подтверждение introduction.
  **2**   **Free listing = бесплатная работа**   2 проекта бесплатно --- AITA верифицирует, публикует, привлекает инвесторов, а платит только при success. Если сделка не закрылась --- AITA инвестировала ресурсы впустую.       Ограничить free listing минимальным scope. Или ввести listing fee (возвращаемый при success).
  **3**   **\"Developer leads\" principle**      Девелопер контролирует отношения с инвестором и ведет переговоры. AITA теряет контроль над процессом и зависит от добросовестности девелопера.                                   Закрепить обязательное участие AITA в ключевых встречах. Ввести co-lead модель для крупных сделок.
  **4**   **Liability cap слишком низкий**       Cap = fees received за 6 месяцев. Если AITA получила €5K fees, а девелопер нанес ущерб на €500K --- cap не покрывает.                                                            Увеличить до 12 месяцев. Исключить cap для circumvention и NDA breach.
  **5**   **Нет аннексов**                       Все 5 аннексов (Packages, Term Sheet, Data Room, Advertising, LOI template) --- referenced but not drafted. Без них договор не работает.                                         Приоритетно разработать Annex 1 (Packages) и Annex 5 (LOI template).
  **6**   **Jurisdiction не выбрана**            §16.2: \"\[Courts of Bilbao/Madrid\] or \[arbitration under ● rules\]\" --- не финализировано. В случае спора --- нет определенности.                                            Зафиксировать CAM Madrid (как в остальных договорах) для единообразия.
  ------- -------------------------------------- -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- -----------------------------------------------------------------------------------------------------------------------------------

**7.2 Системные риски по всей экосистеме**

  ------------------------------------------ ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
  **Зона риска**                             **Проблема и рекомендация**
  **Double-dipping на fee**                  Cooperation берет 2.7% с девелопера + ISA берет 1.5% с инвестора за одну и ту же сделку. Суммарная нагрузка 4.2% может оттолкнуть обе стороны. Рекомендация: четко прописать, что fees не стакаются, или объяснить value proposition для каждой стороны.
  **Non-circumvention сроки конфликтуют**    Cooperation: 24 мес. ISA: 12 мес. Partnership: 90 дней lead protection. Разный подход к одной проблеме. Рекомендация: унифицировать до 24 мес. для introductions.
  **Non-compete ассиметрия**                 Team/Lead: 5 лет non-compete. Partnership: ограничен сроком договора. Cooperation: нет explicit non-compete (только platform non-competition). Рекомендация: для Cooperation добавить limited non-compete как в Partnership.
  **Confidentiality сроки разные**           NDA UA: 3 года + бессрочно для know-how. ISA: 3 года. Partnership: 3 года. Cooperation: 5 лет. Team/Lead: не указан (material breach = termination). Рекомендация: унифицировать до 5 лет + бессрочно для trade secrets.
  **Нет dispute resolution в Cooperation**   Arbitration clause не заполнена. Если девелопер --- из другой юрисдикции (Латам, MENA, CEE), enforcement через испанский суд может быть затруднено. Рекомендация: CAM Madrid + ICC backup.
  **Нет Force Majeure в Cooperation**        ISA и Partnership имеют Force Majeure clause. Cooperation --- нет. При работе с девелоперами из зон конфликтов (UA, MENA) это критично. Рекомендация: добавить стандартную FM clause.
  ------------------------------------------ ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

**8. ПРОБЕЛЫ И РЕКОМЕНДАЦИИ**

**8.1 Что необходимо доработать в Cooperation Agreement**

-   Разработать все 5 аннексов (Packages, Term Sheet, Data Room, Advertising, LOI template)

-   Финализировать dispute resolution: CAM Madrid для единообразия

-   Добавить Force Majeure clause (стандартную, как в ISA/Partnership)

-   Добавить Data Protection clause (GDPR/LOPDGDD --- как в ISA/Partnership)

-   Добавить Language & Controlling Version clause

-   Уточнить payment terms: \[5/10/15\] business days --- выбрать конкретное

-   Уточнить exclusivity period: \[90/120/180\] days --- выбрать конкретное

-   Заполнить AITA реквизиты: address, NIF (B75859744)

**8.2 Рекомендации по экосистеме в целом**

-   Создать Master Agreement или Framework Agreement, объединяющий common clauses (governing law, GDPR, Force Majeure, confidentiality) и ссылающийся на individual agreements для специфики

-   Унифицировать non-circumvention period: 24 месяца для всех внешних контрагентов

-   Унифицировать confidentiality: 5 лет + бессрочно для trade secrets во всех договорах

-   Разработать onboarding checklist для каждого типа контрагента (Developer → Cooperation + NDA; Investor → ISA + NDA; Partner → Partnership + NDA)

-   Создать internal playbook: какой договор подписывается первым, в какой последовательности, кто подписант, какие аннексы обязательны

-   Добавить escalation matrix: кто принимает решение при конфликте между договорами

**8.3 Двойная монетизация: риск или feature?**

Текущая архитектура позволяет AITA зарабатывать на одной сделке одновременно с нескольких сторон: 2.7% с девелопера (Cooperation) + 1.5% с инвестора (ISA) + 50% от profit/margin с EPC-партнера (Partnership) + 50% Profit of the Deal через internal team. В совокупности это может превышать 10% от стоимости проекта.

Это не является проблемой, если каждый контрагент получает реальную ценность от AITA и осведомлен о структуре fees. Но если стороны узнают о суммарной нагрузке --- это может подорвать доверие. Рекомендация: быть transparent о fee structure в pitch materials и показывать net value для каждого участника отдельно.

**9. АГЕНТСЬКА МЕРЕЖА (AGENT NETWORK ENGINE)**

Паралельно з моделлю project-financing AITA розвиває B2B агентську мережу з продажу фізичних товарів: сонячне енергетичне обладнання, промислові електрокомплекси, кабельна продукція, будівельні та інженерні матеріали. Це друга комерційна модель AITA --- незалежна від першої, але така, що використовує ту саму юридичну особу та бренд.

**9.1 Суть агентської моделі**

AITA закуповує товари безпосередньо у виробників і великих імпортерів --- без регіональних дилерів і дистриб\'юторських надбавок. Агент знаходить B2B-покупця, передає запит в AITA, AITA виставляє рахунок, доставляє товар і бере на себе весь документообіг. Агент автоматично отримує частку маржі після підтвердження оплати.

+-----------------------------------------------------+--------------------------------------------------------------+
| **Класичний ланцюжок**                              | **Ланцюжок AITA**                                            |
|                                                     |                                                              |
| *Виробник → Дистриб\'ютор → Дилер → Агент → Клієнт* | Виробник → AITA → Агент → Клієнт                             |
|                                                     |                                                              |
|                                                     | *Страйк прайс = закупівельна ціна + логістика + AITA сервіс* |
+-----------------------------------------------------+--------------------------------------------------------------+

**9.2 Три числа: механіка розподілу маржі**

На кожній угоді маржа (Client Price − Strike Price) ділиться за однією формулою:

+----------+------------------------------------+----------------------------------+
| **AITA** | **Агент**                          | **Рекрутер**                     |
|          |                                    |                                  |
| **20%**  | **30% → 45% → 60%**                | **50% → 35% → 20%**              |
|          |                                    |                                  |
| *завжди* | *зростає з оборотом (Level 1→2→3)* | *максимум; він регулює % агенту* |
+----------+------------------------------------+----------------------------------+

**9.3 Рівні агента**

  ------------- -------------------- -------------------------- ------------------------------ ---------------------- -------------
  **Рівень**    **Оборот агента**    **Агент мін. (від 80%)**   **Рекрутер макс. (від 80%)**   **AITA (від маржі)**   **Перехід**
  **Level 1**   €0 -- €15 000        30%                        50%                            20%                    авто
  **Level 2**   €15 001 -- €50 000   45%                        35%                            20%                    авто
  **Level 3**   €50 001+             60%                        20%                            20%                    авто
  ------------- -------------------- -------------------------- ------------------------------ ---------------------- -------------

**9.4 Ланцюжок послуг --- агентська модель**

  ---------- ----------- -------------------------------------------------------------------------------------
  **Етап**   **Актор**   **Дія**
  **1**      Агент       Знаходить B2B-покупця з потребою у товарі з каталогу AITA
  2          Агент       Передає запит в AITA через Telegram-бот або менеджера
  3          AITA        Готує комерційну пропозицію зі страйк-прайсом і умовами постачання; надсилає Агенту
  4          Агент       Узгоджує фінальну Client Price з покупцем (≥ Strike Price); підтверджує замовлення
  5          AITA        Виставляє рахунок покупцю; контролює оплату, логістику, документи, гарантію
  6          AITA        Confirmed Transaction → автоматична виплата Агенту (і Рекрутеру)
  ---------- ----------- -------------------------------------------------------------------------------------

**9.5 Пасивний дохід рекрутера**

Рекрутер (Partner) будує мережу агентів і заробляє на кожній угоді своїх агентів без особистої участі. Приклад: 10 активних агентів у мережі (mix рівнів 1/2/3) генерують рекрутеру €5 265 пасивно на місяць. Рекрутер сам регулює % агенту --- чим щедріший %, тим вища мотивація мережі, але нижчий особистий дохід рекрутера.

**9.6 Договірна база агентської моделі**

  ------------------- ----------------- -----------------------------------------------------------------------------------------------
  **Документ**        **Сторони**       **Ключові умови**
  Агентська угода     AITA ↔ Агент      Невиключна; розподіл 80/20; автовиплата; рівні; Telegram-бот; антиобхід 12 міс.
  Партнерська угода   AITA ↔ Рекрутер   Пасивний дохід з мережі; статус Team Builder; заборона переманювання; 1 рік + автопролонгація
  ------------------- ----------------- -----------------------------------------------------------------------------------------------

**9.7 Інтеграція з основною екосистемою**

Агентська модель --- окремий P&L всередині AITA, незалежний від project-financing. Проте можливий синергічний ефект: агент з мережі (продає обладнання) може одночасно бути девелопером на платформі (лістингує проект) або познайомити AITA з інвестором через свій B2B-контакт. Ключовий принцип обох моделей: AITA заробляє лише при Successful Closing / Confirmed Transaction. Немає угоди --- немає комісії.

**10. МАРКЕТИНГОВИЙ БЛОК (MARKETING ENGINE)**

Третя комерційна модель AITA --- цифровий маркетинг та генерація лідів для компаній у сфері відновлюваної енергетики. На відміну від project-financing (Моделі 1) та агентської мережі (Моделі 2), Маркетинговий блок генерує передбачуваний recurring revenue: депозити + щомісячний потік лідів + Success Fee при закритті угоди. Клієнт --- будь-яка компанія (EPC, дистриб\'ютор, девелопер), якій потрібен керований потік кваліфікованих B2B-лідів.

**10.1 Суть маркетингової моделі**

AITA не є класичним рекламним агентством. Це інтегрований маркетинговий оператор, що поєднує AI-таргетинг, Telegram-автоматизацію, CRM-інфраструктуру та мережу агентів в одному контракті. Клієнт отримує не \"клік\" --- а Кваліфікований лід, що пройшов автоматичну воронку і підтвердив готовність до покупки.

+-------------------------------------------------------------------------+-------------------------------------------------------------------------------------------+
| **Класичне агентство**                                                  | **AITA Marketing Engine**                                                                 |
|                                                                         |                                                                                           |
| *Бюджет → Рекламна платформа → Кліки → Ліди (вхідні) → Відділ продажів* | *Депозит → AI-кампанія → Telegram Bot (кваліфікація) → Кваліфікований лід → CRM Deal_ID* |
|                                                                         |                                                                                           |
| Оплата за покази / кліки --- без гарантії якості                        | Оплата лише за Кваліфікований лід (€30) + Success Fee 1,5% після угоди                    |
+-------------------------------------------------------------------------+-------------------------------------------------------------------------------------------+

**10.2 Склад послуг та цінова модель**

Повний каталог послуг AITA Marketing. Клієнт обирає пакет послуг в Ордері; базові опції (Sales Node, Network Support) включені в LaaS-контракт автоматично.

  ---------- ----------------------------------- ------------------------------------------------------------------------------------------------------------------------------------------------------ -----------------------------------
  **№**      **Послуга**                         **Склад**                                                                                                                                              **Вартість**
  **10.1**   LaaS Lead-as-a-Service              Рекламні кампанії (Google, Facebook, Instagram); AI-таргетинг; автокваліфікація через Telegram-бот; дашборд лідів; A/B-тестування                      €30 / кваліф. лід +депозит €2 000
  **10.2**   Sales Node Telegram-бот-мережа      Автозбір даних покупця + Deal_ID у CRM; автогенерація PDF-пропозицій з 3 рівнями цін; до 7 ботів; онбординг агентів і скрипти продажів                Включено в LaaS
  **10.3**   Інтегрована Landing Page            Висококонверсійна сторінка, синхронізована з CRM; mobile-first; Quick SKU --- каталог з актуальними цінами (Deye, JinKO, HUAWEI); шаблони документів   €1 500 одноразово
  **10.4**   Network Support (Масштабування)     Автоматичний розрахунок комісій агентам мережі; Lot Aggregation --- об\'єднання дрібних замовлень у партії зі знижкою до 7%; дашборди конверсії        Включено в LaaS
  **10.5**   AITA Workspace AI-CRM + Телефонія   IP-телефонія, інтегрована у платформу; AI-транскрипція дзвінків; автостворення завдань у CRM після дзвінка; AITA Assist --- AI-асистент                €25 / користувач / міс.
  **10.6**   Success Fee Платформова комісія     Безперервна оптимізація лід-кампаній; контроль якості лідів; доступ до AITA Marketplace з цінами виробників Tier-1; технічна підтримка                 1,5% від угоди після оплати
  ---------- ----------------------------------- ------------------------------------------------------------------------------------------------------------------------------------------------------ -----------------------------------

**10.3 Структура доходу AITA від маркетингу**

Маркетингова модель генерує три типи доходу: авансовий (передбачуваний), потоковий (масштабований) і транзакційний (performance-based). Це дозволяє AITA балансувати cashflow незалежно від циклічності проектного фінансування.

  ---------------- -------------------------------------------------------- ------------- ------------------------------------------
  **Тип доходу**   **Джерело**                                              **Частота**   **Рівень передбачуваності**
  Авансовий        Рекламний депозит €2 000 при старті LaaS                 Один раз      Висока --- 100% передоплата
  Потоковий        €30 × N лідів / місяць; €25 × K користувачів Workspace   Щомісяця      Середня --- залежить від обсягу кампанії
  Разовий          Landing Page €1 500 (10%+30%+60% за етапами)             Проектний     Висока --- фіксований
  Транзакційний    Success Fee 1,5% від вартості закритої угоди клієнта     Після угоди   Низька --- performance-based
  ---------------- -------------------------------------------------------- ------------- ------------------------------------------

**10.4 Воронка клієнта (Customer Journey)**

  ---------- -------------------- -----------------------------------------------------------------------------------------------------------------------------------------------------------------------
  **Етап**   **Актор**            **Дія / Результат**
  **1**      AITA                 Запуск таргетованих кампаній (Google / Facebook / Instagram) на власників будівель, EPC-компанії, девелоперів; геотаргетинг + AI-сегментація за інтересами (PV, BESS)
  **2**      Потенційний клієнт   Бачить рекламу → переходить на Landing Page або вступає у Sales Node (Telegram-бот)
  **3**      Telegram Bot         Автокваліфікація: збір місцезнаходження, тип об\'єкта, потужність, готовність до покупки; призначення Deal_ID у CRM
  **4**      AITA / Агент         Кваліфікований лід передається Клієнту; генерується PDF-пропозиція з 3 рівнями цін автоматично
  **5**      Клієнт               Обробляє лід у власному відділі продажів або через агента AITA; веде переговори
  **6**      Клієнт + AITA        Закрита угода → Клієнт сповіщає AITA про оплату → AITA нараховує Success Fee 1,5%
  ---------- -------------------- -----------------------------------------------------------------------------------------------------------------------------------------------------------------------

**10.5 Інтеграція маркетингового блоку з агентською мережею**

Маркетинговий блок та агентська мережа не є ізольованими: кожен агент з мережі (§9) може одночасно бути Sales Node Клієнта маркетингової моделі. Агент отримує ліди через LaaS-кампанії AITA і закриває угоди, що автоматично генерує комісію агента + Success Fee для AITA. Таким чином один і той самий суб\'єкт може брати участь в обох моделях одночасно --- без конфлікту інтересів.

  -------------------------- -------------------------------------------------------- ---------------------------------------------------------------- --------------------------
  **Модель**                 **Роль AITA**                                            **Роль агента / партнера**                                       **Синергія**
  Агентська мережа (§9)      Постачальник товару; 20% від маржі                       Знаходить покупця; отримує 30--60%                               Агент продає товари AITA
  Маркетинговий блок (§10)   Генератор лідів; 1,5% Success Fee                        Закриває ліди як Sales Node Клієнта                              Агент = Sales Node
  Синергія                   Агент = Sales Node для лідів клієнтів Marketing Engine   AITA: подвійний дохід --- комісія агента + Success Fee клієнта   Crossover
  -------------------------- -------------------------------------------------------- ---------------------------------------------------------------- --------------------------

**10.6 Договірна база маркетингового блоку**

  --------------------------------- --------------- ------------------------------------------------------------------------------------------------------------------------------------------------
  **Документ**                      **Сторони**     **Ключові умови**
  Маркетинговий договір (Послуги)   AITA ↔ Клієнт   LaaS €30/лід + депозит €2 000; Landing Page €1 500; Workspace €25/user/міс.; Success Fee 1,5%; 3 місяці + автопролонгація; арбітраж CAM Мадрид
  Агентська угода (§9)              AITA ↔ Агент    Агент = Sales Node для лідів Marketing Engine; комісія за угоду агента окрема від Success Fee клієнта
  Ордер на послуги                  AITA ↔ Клієнт   Додаток до Маркетингового договору; фіксує ринок, пакет послуг, кількість лідів, бюджет депозиту, строк кампанії
  --------------------------------- --------------- ------------------------------------------------------------------------------------------------------------------------------------------------

*Документ подготовлен для внутреннего использования AITA WORLD, S.L. Март 2026. Версия 2.0*


---

# ═══ АРХІТЕКТУРА ЕКОСИСТЕМИ (UA) ═══

**AITA WORLD, S.L.**

**АРХИТЕКТУРА ДОГОВОРНОЙ ЭКОСИСТЕМЫ**

*Цепочка услуг · Цепочка ценности · Монетизация · Анализ рисков*

*Подготовлено: март 2026 \| Версия: 1.0 \| Статус: рабочий документ*

**1. ОБЗОР ДОГОВОРНОЙ ЭКОСИСТЕМЫ**

Договорная база AITA охватывает 7 документов, каждый из которых регулирует отношения с определенным типом контрагента. Вместе они формируют замкнутую экосистему, в которой AITA выступает центральным узлом --- платформой, соединяющей проектных девелоперов, инвесторов, партнеров-исполнителей и внутренние команды.

  ------- ---------------------------------- ------------------------ -------------------------------------------------------------- ------------------------------------------------------------------------
  **№**   **Документ**                       **Контрагент**           **Роль в экосистеме**                                          **Ключевое обязательство AITA**
  **1**   **NDA (UA)**                       Любой (UA рынок)         Защита информации до входа в экосистему                        Конфиденциальность 3 года + бессрочно для know-how
  **2**   **Cooperation Agreement**          Девелопер проектов       Вход проектов в платформу; matchmaking с инвесторами           Листинг, верификация, matchmaking, маркетинг инвесторам
  **3**   **Investor Services Agreement**    Инвестор / Фонд          Вход капитала; sourcing проектов для инвестора                 Matching, baseline audit, deal tracking, legal coordination, co-invest
  **4**   **Partnership Agreement**          EPC / Поставщик          Исполнение проектов; оборудование; works/EPC через платформу   Lead distribution, marketplace, procurement, продажа works клиентам
  **5**   **Team Agreement**                 Delivery-команда         Исполнение сделок силами команды (30% profit pool)             Платформа, governance, advisory support, approval gates
  **6**   **Deal Execution Agreement**       Project Lead             Лидерство по конкретной сделке (20% + 30% pool)                Product-Only Exception, advisory 45 мин/день, next case
  **7**   **Cooperation Agr. (Developer)**   Девелопер (энергетика)   Листинг проектов, эксклюзивность, success fees                 Платформа, верификация, matchmaking, investor advertising
  ------- ---------------------------------- ------------------------ -------------------------------------------------------------- ------------------------------------------------------------------------

**2. ЦЕПОЧКА УСЛУГ (SERVICE CHAIN)**

Цепочка услуг AITA --- это последовательность сервисов, которые компания предоставляет на каждом этапе жизненного цикла энергетического проекта. Каждый этап связан с конкретным договором и конкретным контрагентом.

**Этап 1: Sourcing & Listing (Привлечение и листинг проектов)**

+------------------------------+----------------------------------------------------------------------------------------------------------------------+
| **Договор:**                 | **Контрагент:** Девелопер проектов (PV, BESS, hybrid, C&I, grid-scale)                                               |
|                              |                                                                                                                      |
| Cooperation Agreement        |                                                                                                                      |
+------------------------------+----------------------------------------------------------------------------------------------------------------------+
| **Услуги AITA:**             | -   Предоставление платформы и листинг-воркфлоу                                                                      |
|                              |                                                                                                                      |
|                              | -   Верификация, структурирование и скоринг данных проекта                                                           |
|                              |                                                                                                                      |
|                              | -   Присвоение статусов: Draft → Verified → Published → Restricted → Archived                                        |
|                              |                                                                                                                      |
|                              | -   2 бесплатных листинга (basic card, document upload, completeness checks)                                         |
|                              |                                                                                                                      |
|                              | -   Коммерческие пакеты: стратегия, tracking, advanced reporting, investor advertising (с 3-го проекта)              |
+------------------------------+----------------------------------------------------------------------------------------------------------------------+
| **Ценность для девелопера:** | Доступ к платформе с инвесторской базой; профессиональная упаковка проекта; повышение доверия через верификацию AITA |
+------------------------------+----------------------------------------------------------------------------------------------------------------------+

**Этап 2: Investor Onboarding (Подключение инвесторов)**

+-----------------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------+
| **Договор:**                      | **Контрагент:** Инвестор, фонд, family office, институциональный игрок                                                                                      |
|                                   |                                                                                                                                                             |
| ISA (Investor Services Agreement) |                                                                                                                                                             |
+-----------------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------+
| **Услуги AITA:**                  | -   Package A: Matching + Baseline Audit + Tracking + Legal Coordination (1.5%)                                                                             |
|                                   |                                                                                                                                                             |
|                                   | -   Package B: Advisory Retainer EUR 4,000/мес + Deal Execution + Platform Transactions (1% + 0.4%)                                                         |
|                                   |                                                                                                                                                             |
|                                   | -   Package C: Co-Investment в AITA-originated проекты (management fee 10%)                                                                                 |
|                                   |                                                                                                                                                             |
|                                   | -   Package D: Bank/Institutional Compliance Screening (\$15/проект)                                                                                        |
+-----------------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------+
| **Ценность для инвестора:**       | Доступ к верифицированным проектам; снижение risk exposure через baseline audit; deal tracking и legal coordination «под ключ»; co-investment opportunities |
+-----------------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------+

**Этап 3: Matching & Introduction (Сведение сторон)**

+---------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| **Договоры:**                   | **Функция платформы:** AITA соединяет проекты (supply) с капиталом (demand) и исполнителями (execution)                                                                                          |
|                                 |                                                                                                                                                                                                  |
| Cooperation + ISA + Partnership |                                                                                                                                                                                                  |
+---------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| **Услуги AITA:**                | -   Matchmaking: introductions, access к инвесторам, EPCs, suppliers, advisors                                                                                                                   |
|                                 |                                                                                                                                                                                                  |
|                                 | -   Investor advertising: campaigns, platform pools, roadshows, targeted intros                                                                                                                  |
|                                 |                                                                                                                                                                                                  |
|                                 | -   Lead generation и distribution (leads → партнерам / девелоперам)                                                                                                                             |
|                                 |                                                                                                                                                                                                  |
|                                 | -   Non-circumvention enforcement: защита цепочки introductions                                                                                                                                  |
+---------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| **Критическая точка:**          | Именно на этом этапе AITA создает основную ценность --- соединение сторон. Эксклюзивность по Cooperation Agreement возникает только при подписании LOI. До LOI девелопер может увести инвестора. |
+---------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+

**Этап 4: Deal Structuring & Negotiation (Структурирование сделки)**

+-----------------------------------------------+-------------------------------------------------------------------------------------------------------------------------------------------+
| **Договоры:**                                 | **Исполнители:** Внутренняя команда AITA (delivery team / project lead)                                                                   |
|                                               |                                                                                                                                           |
| Team + Project Lead + Cooperation (опция §10) |                                                                                                                                           |
+-----------------------------------------------+-------------------------------------------------------------------------------------------------------------------------------------------+
| **Услуги AITA:**                              | -   Подготовка negotiation materials, agendas, minutes, follow-ups                                                                        |
|                                               |                                                                                                                                           |
|                                               | -   Drafting и negotiating contract terms                                                                                                 |
|                                               |                                                                                                                                           |
|                                               | -   SPV structuring, financial model, PPA logic, tendering                                                                                |
|                                               |                                                                                                                                           |
|                                               | -   Permitting support, engineering concept, feasibility/TEO                                                                              |
|                                               |                                                                                                                                           |
|                                               | -   KPI dashboards, pilot evidence, analytics pack                                                                                        |
+-----------------------------------------------+-------------------------------------------------------------------------------------------------------------------------------------------+
| **Модель оплаты команды:**                    | Team Agreement: 30% от Profit of the Deal (self-governed pool). Project Lead: 20% Lead Success Fee + 30% team pool. AITA: оставшиеся 50%. |
+-----------------------------------------------+-------------------------------------------------------------------------------------------------------------------------------------------+

**Этап 5: Execution & Procurement (Исполнение и закупки)**

+-----------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------+
| **Договор:**          | **Контрагент:** EPC-подрядчик, поставщик оборудования (gas turbine, BESS, hybrid)                                                                              |
|                       |                                                                                                                                                                |
| Partnership Agreement |                                                                                                                                                                |
+-----------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------+
| **Услуги AITA:**      | -   Lead distribution: 50% profit/margin за leads в Partner Vertical, 30% за outside                                                                           |
|                       |                                                                                                                                                                |
|                       | -   Marketplace distribution оборудования партнера (30% Equipment Margin)                                                                                      |
|                       |                                                                                                                                                                |
|                       | -   Продажа Partner Works/EPC клиентам (50/50 profit split)                                                                                                    |
|                       |                                                                                                                                                                |
|                       | -   Open-Book procurement: Works +9%, Equipment +4% norm margin                                                                                                |
|                       |                                                                                                                                                                |
|                       | -   Advertising-funded leads (10% profit share при IO)                                                                                                         |
+-----------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------+
| **Контроль:**         | Partner Dashboard: lead assignment, status tracking, monetization reporting, commission calculations. Platform может менять conditions с уведомлением 50 дней. |
+-----------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------+

**Этап 6: Closing & Settlement (Закрытие сделки и расчеты)**

  ------------------ ----------------------------------------------------------------------------------------------------------------------------------------------------------------------
  **Все договоры**   **Триггеры оплаты AITA:**
  **Cooperation:**   Success fee при подписании definitive agreements или получении consideration. CapEx stage: 2.7% от Total CapEx Deal Volume. Dev stage: 5% от Development Deal Value.
  **ISA:**           Package A: 1.5% от Investment Amount при closing. Package B: EUR 4,000/мес retainer + 1% + 0.4% platform transactions. Package C: 10% management fee.
  **Partnership:**   Доля AITA от profit/margin: 50% (vertical leads), 30% (non-vertical), 30% (equipment), 50/50 (EPC sales). Open-Book: +9%/+4% norm margins.
  **Team / Lead:**   AITA удерживает 50% Profit of the Deal (после выплаты 20% Project Lead + 30% team pool). Выплаты pro-rata по мере реализации profit.
  ------------------ ----------------------------------------------------------------------------------------------------------------------------------------------------------------------

**3. ЦЕПОЧКА ЦЕННОСТИ (VALUE CHAIN)**

Цепочка ценности показывает, как AITA создает, аккумулирует и монетизирует ценность на каждом уровне экосистемы. AITA работает как двусторонняя платформа (two-sided marketplace): привлекает проекты со стороны предложения и капитал со стороны спроса, зарабатывая на каждой стороне транзакции.

**3.1 Первичные активности (Primary Activities)**

  ----------------------- --------------------------------------------------------------------------------- --------------------------------------------------------------------- --------------------------------------------------------------------
  **Активность**          **Что делает AITA**                                                               **Какую ценность создает**                                            **Как монетизирует**
  **Project Sourcing**    Привлекает девелоперов на платформу; принимает и верифицирует проекты             Формирует deal flow --- пайплайн верифицированных проектов            2 бесплатных листинга → Commercial Packages с 3-го проекта
  **Capital Sourcing**    Привлекает инвесторов; предлагает пакеты услуг (A/B/C/D); compliance screening    Формирует investor pool --- базу квалифицированных инвесторов         ISA fees: 1.5% matching + retainer EUR 4K/мес + 10% management fee
  **Matching**            Соединяет проекты с инвесторами, EPC, suppliers; ведет introductions и workflow   Снижает friction --- ускоряет сделки; создает trust через платформу   Coop: 2.7% CapEx / 5% Dev. Partnership: 1.5% или 3% Fee Base
  **Deal Execution**      Структурирует сделки; ведет переговоры; юридическая координация; SPV              Доводит сделки до closing; минимизирует execution risk                Team/Lead: AITA получает 50% Profit of the Deal
  **Procurement & EPC**   Организует закупки через платформу; продает works/EPC партнеров клиентам          Контролирует execution chain; обеспечивает качество через Open-Book   50/50 EPC margin; 30% Equipment; Open-Book +9%/+4%
  ----------------------- --------------------------------------------------------------------------------- --------------------------------------------------------------------- --------------------------------------------------------------------

**3.2 Поддерживающие активности**

  ---------------------------- -----------------------------------------------------------------------------------------------------------------------------------------------------------------------------
  **Активность**               **Описание**
  **Platform & Technology**    AITA Platform: листинг, верификация, data room, workflow, dashboards, analytics, KPI tracking. Является обязательным инструментом (Digital-Only principle) для всех сделок.
  **Compliance & Screening**   AML/KYC, sanctions screening, bank readiness checks (Package D ISA). GDPR/LOPDGDD data protection. NDA protection pre-engagement.
  **IP & Brand**               Платформенные методологии, scoring algorithms, workflow logic --- защищены через non-competition clauses во всех договорах. Бренд AITA как знак качества верификации.
  **Governance & Control**     Approval Gates (Founder/CEO) для всех финансовых/юридических обязательств. Версионирование в платформе = юридическое доказательство. Non-circumvention enforcement.
  ---------------------------- -----------------------------------------------------------------------------------------------------------------------------------------------------------------------------

**4. СВОДНАЯ МАТРИЦА МОНЕТИЗАЦИИ**

Ниже --- полная карта источников дохода AITA по всем договорам. Каждая строка = отдельный revenue stream.

  ------------------------------ ------------- ------------------------------------------------------ --------------- ------------------------------
  **Источник дохода**            **Договор**   **База расчета**                                       **Ставка**      **Триггер**
  Success Fee (CapEx stage)      Cooperation   Total CapEx Deal Volume (EPC, equipment, grid, etc.)   **2.7%**        Definitive agreements signed
  Success Fee (Dev stage)        Cooperation   Development Deal Value (rights/package)                **5%**          Definitive agreements signed
  Commercial Packages            Cooperation   Subscription / purchase                                **Annex 1/4**   С 3-го проекта
  Matching Fee (Pkg A)           ISA           Investment Amount                                      **1.5%**        Closing / first tranche
  Advisory Retainer (Pkg B)      ISA           Monthly (20 hrs cap)                                   **EUR 4,000**   Ежемесячно
  Deal Execution Fee (Pkg B)     ISA           Investment Amount                                      **1.0%**        Closing
  Platform Transaction Fee       ISA           Gross transaction value                                **0.4%**        Platform purchase
  Co-Invest Management (Pkg C)   ISA           Per Project Term Sheet                                 **10%**         Per term sheet
  Compliance Screening (Pkg D)   ISA           Per project                                            **\$15**        Report delivery
  Lead (in Vertical)             Partnership   Partner Profit/Margin                                  **50%**         Payment / binding agr.
  Lead (outside Vertical)        Partnership   Partner Profit/Margin                                  **30%**         Payment / binding agr.
  Project Matching Fee           Partnership   Fee Base (CAPEX/Investment/Contract)                   **1.5%**        Transaction close
  Investor Recommendation        Partnership   Fee Base                                               **3%**          Funding/transaction
  Equipment Marketplace          Partnership   Equipment Profit/Margin                                **30%**         Sale concluded
  EPC/Works Sales                Partnership   Works/EPC Profit/Margin                                **50/50**       Sale concluded
  Advertising Leads              Partnership   Partner Profit/Margin                                  **10%**         IO + budget paid
  AITA Retained Profit           Team / Lead   Profit of the Deal                                     **50%**         Profit realized
  ------------------------------ ------------- ------------------------------------------------------ --------------- ------------------------------

**5. COOPERATION AGREEMENT (DEVELOPER) --- АНАЛИЗ**

**5.1 Позиционирование в экосистеме**

Cooperation Agreement --- это «входные ворота» для проектов в экосистему AITA. Без этого договора платформа не получает deal flow. Это договор со стороны предложения (supply side), в то время как ISA работает со стороны спроса (demand side). Вместе они формируют two-sided marketplace.

**5.2 Ключевые условия**

  ------------------------- ------------------------------------------------------------------------------------------------------
  **Параметр**              **Условие**
  **Принцип**               \"Developer leads\" --- девелопер ведет проекты операционно и коммерчески
  **Free Listing**          2 проекта бесплатно (basic card, upload, completeness checks)
  **Эксклюзивность**        Начинается ТОЛЬКО при подписании LOI с AITA Investor. До LOI --- лишь good faith + non-circumvention
  **Success Fee (CapEx)**   2.7% от Total CapEx Deal Volume (EPC, equipment, grid, engineering, etc.)
  **Success Fee (Dev)**     5% от Development Deal Value (development rights/package)
  **Non-circumvention**     24 месяца после последнего introduction/contact по проекту
  **Срок**                  12 месяцев, auto-renew. Cure period: 15 дней. Tail: 24 месяца для introductions
  **Equity option (§10)**   AITA может получить equity/profit share за доп. работу (permitting, SPV, TEO, financial model)
  **Liability cap**         Fees actually received за последние 6 месяцев по конкретному проекту
  **Governing law**         Spain. Jurisdiction: \[Courts of Bilbao/Madrid\] или arbitration --- не выбрано
  ------------------------- ------------------------------------------------------------------------------------------------------

**6. ЗОНЫ РИСКА ДЛЯ AITA**

**6.1 Cooperation Agreement (Developer) --- критичные риски**

  ------- -------------------------------------- -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- -----------------------------------------------------------------------------------------------------------------------------------
  **№**   **Риск**                               **Описание**                                                                                                                                                                     **Рекомендация**
  **1**   **Pre-LOI circumvention**              До LOI эксклюзивности нет. Девелопер может познакомиться с инвестором через AITA и закрыть сделку напрямую. Non-circumvention (§9) работает, но доказать его нарушение сложно.   Добавить engagement fee или retainer за верификацию. Ввести \"AITA introduction notice\" = формальное подтверждение introduction.
  **2**   **Free listing = бесплатная работа**   2 проекта бесплатно --- AITA верифицирует, публикует, привлекает инвесторов, а платит только при success. Если сделка не закрылась --- AITA инвестировала ресурсы впустую.       Ограничить free listing минимальным scope. Или ввести listing fee (возвращаемый при success).
  **3**   **\"Developer leads\" principle**      Девелопер контролирует отношения с инвестором и ведет переговоры. AITA теряет контроль над процессом и зависит от добросовестности девелопера.                                   Закрепить обязательное участие AITA в ключевых встречах. Ввести co-lead модель для крупных сделок.
  **4**   **Liability cap слишком низкий**       Cap = fees received за 6 месяцев. Если AITA получила €5K fees, а девелопер нанес ущерб на €500K --- cap не покрывает.                                                            Увеличить до 12 месяцев. Исключить cap для circumvention и NDA breach.
  **5**   **Нет аннексов**                       Все 5 аннексов (Packages, Term Sheet, Data Room, Advertising, LOI template) --- referenced but not drafted. Без них договор не работает.                                         Приоритетно разработать Annex 1 (Packages) и Annex 5 (LOI template).
  **6**   **Jurisdiction не выбрана**            §16.2: \"\[Courts of Bilbao/Madrid\] or \[arbitration under ● rules\]\" --- не финализировано. В случае спора --- нет определенности.                                            Зафиксировать CAM Madrid (как в остальных договорах) для единообразия.
  ------- -------------------------------------- -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- -----------------------------------------------------------------------------------------------------------------------------------

**6.2 Системные риски по всей экосистеме**

  ------------------------------------------ ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
  **Зона риска**                             **Проблема и рекомендация**
  **Double-dipping на fee**                  Cooperation берет 2.7% с девелопера + ISA берет 1.5% с инвестора за одну и ту же сделку. Суммарная нагрузка 4.2% может оттолкнуть обе стороны. Рекомендация: четко прописать, что fees не стакаются, или объяснить value proposition для каждой стороны.
  **Non-circumvention сроки конфликтуют**    Cooperation: 24 мес. ISA: 12 мес. Partnership: 90 дней lead protection. Разный подход к одной проблеме. Рекомендация: унифицировать до 24 мес. для introductions.
  **Non-compete ассиметрия**                 Team/Lead: 5 лет non-compete. Partnership: ограничен сроком договора. Cooperation: нет explicit non-compete (только platform non-competition). Рекомендация: для Cooperation добавить limited non-compete как в Partnership.
  **Confidentiality сроки разные**           NDA UA: 3 года + бессрочно для know-how. ISA: 3 года. Partnership: 3 года. Cooperation: 5 лет. Team/Lead: не указан (material breach = termination). Рекомендация: унифицировать до 5 лет + бессрочно для trade secrets.
  **Нет dispute resolution в Cooperation**   Arbitration clause не заполнена. Если девелопер --- из другой юрисдикции (Латам, MENA, CEE), enforcement через испанский суд может быть затруднено. Рекомендация: CAM Madrid + ICC backup.
  **Нет Force Majeure в Cooperation**        ISA и Partnership имеют Force Majeure clause. Cooperation --- нет. При работе с девелоперами из зон конфликтов (UA, MENA) это критично. Рекомендация: добавить стандартную FM clause.
  ------------------------------------------ ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

**7. ПРОБЕЛЫ И РЕКОМЕНДАЦИИ**

**7.1 Что необходимо доработать в Cooperation Agreement**

-   Разработать все 5 аннексов (Packages, Term Sheet, Data Room, Advertising, LOI template)

-   Финализировать dispute resolution: CAM Madrid для единообразия

-   Добавить Force Majeure clause (стандартную, как в ISA/Partnership)

-   Добавить Data Protection clause (GDPR/LOPDGDD --- как в ISA/Partnership)

-   Добавить Language & Controlling Version clause

-   Уточнить payment terms: \[5/10/15\] business days --- выбрать конкретное

-   Уточнить exclusivity period: \[90/120/180\] days --- выбрать конкретное

-   Заполнить AITA реквизиты: address, NIF (B75859744)

**7.2 Рекомендации по экосистеме в целом**

-   Создать Master Agreement или Framework Agreement, объединяющий common clauses (governing law, GDPR, Force Majeure, confidentiality) и ссылающийся на individual agreements для специфики

-   Унифицировать non-circumvention period: 24 месяца для всех внешних контрагентов

-   Унифицировать confidentiality: 5 лет + бессрочно для trade secrets во всех договорах

-   Разработать onboarding checklist для каждого типа контрагента (Developer → Cooperation + NDA; Investor → ISA + NDA; Partner → Partnership + NDA)

-   Создать internal playbook: какой договор подписывается первым, в какой последовательности, кто подписант, какие аннексы обязательны

-   Добавить escalation matrix: кто принимает решение при конфликте между договорами (например, Developer хочет привести своего инвестора, а ISA investor претендует на тот же проект)

**7.3 Двойная монетизация: риск или feature?**

Текущая архитектура позволяет AITA зарабатывать на одной сделке одновременно с нескольких сторон: 2.7% с девелопера (Cooperation) + 1.5% с инвестора (ISA) + 50% от profit/margin с EPC-партнера (Partnership) + 50% Profit of the Deal через internal team. В совокупности это может превышать 10% от стоимости проекта.

Это не является проблемой, если каждый контрагент получает реальную ценность от AITA и осведомлен о структуре fees. Но если стороны узнают о суммарной нагрузке --- это может подорвать доверие. Рекомендация: быть transparent о fee structure в pitch materials и показывать net value для каждого участника отдельно.

**8. АГЕНТСЬКА МЕРЕЖА (AGENT NETWORK ENGINE)**

Паралельно з моделлю project-financing AITA розвиває B2B агентську мережу з продажу фізичних товарів: сонячне енергетичне обладнання, промислові електрокомплекси, кабельна продукція, будівельні та інженерні матеріали. Це друга комерційна модель AITA --- незалежна від першої, але така, що використовує ту саму юридичну особу та бренд.

**8.1 Суть агентської моделі**

AITA закуповує товари безпосередньо у виробників і великих імпортерів --- без регіональних дилерів і дистрибуторських надбавок. Агент знаходить B2B-покупця, передає запит в AITA, AITA виставляє рахунок, доставляє товар і бере на себе весь документообіг. Агент автоматично отримує частку маржі після підтвердження оплати.

+----------------------------------------------------+--------------------------------------------------------------+
| **Класичний ланцюжок**                             | **Ланцюжок AITA**                                            |
|                                                    |                                                              |
| *Виробник → Дистриб'ютор → Дилер → Агент → Клієнт* | Виробник → AITA → Агент → Клієнт                             |
|                                                    |                                                              |
|                                                    | *Страйк прайс = закупівельна ціна + логістика + AITA сервіс* |
+----------------------------------------------------+--------------------------------------------------------------+

**8.2 Три числа: механіка розподілу маржі**

На кожній угоді маржа (Client Price − Strike Price) ділиться за однією формулою:

+----------+------------------------------------+----------------------------------+
| **AITA** | **Агент**                          | **Рекрутер**                     |
|          |                                    |                                  |
| **20%**  | **30% → 45% → 60%**                | **50% → 35% → 20%**              |
|          |                                    |                                  |
| *завжди* | *зростає з оборотом (Level 1→2→3)* | *максимум; він регулює % агенту* |
+----------+------------------------------------+----------------------------------+

**8.3 Рівні агента**

  ------------- -------------------- -------------------------- ------------------------------ ---------------------- -------------
  **Рівень**    **Оборот агента**    **Агент мін. (від 80%)**   **Рекрутер макс. (від 80%)**   **AITA (від маржі)**   **Перехід**
  **Level 1**   €0 -- €15 000        30%                        50%                            20%                    авто
  **Level 2**   €15 001 -- €50 000   45%                        35%                            20%                    авто
  **Level 3**   €50 001+             60%                        20%                            20%                    авто
  ------------- -------------------- -------------------------- ------------------------------ ---------------------- -------------

**8.4 Ланцюжок послуг --- агентська модель**

  ---------- ----------- -------------------------------------------------------------------------------------
  **Етап**   **Актор**   **Дія**
  **1**      Агент       Знаходить B2B-покупця з потребою у товарі з каталогу AITA
  2          Агент       Передає запит в AITA через Telegram-бот або менеджера
  3          AITA        Готує комерційну пропозицію зі страйк-прайсом і умовами постачання; надсилає Агенту
  4          Агент       Узгоджує фінальну Client Price з покупцем (≥ Strike Price); підтверджує замовлення
  5          AITA        Виставляє рахунок покупцю; контролює оплату, логістику, документи, гарантію
  6          AITA        Confirmed Transaction → автоматична виплата Агенту (і Рекрутеру)
  ---------- ----------- -------------------------------------------------------------------------------------

**8.5 Пасивний дохід рекрутера**

Рекрутер (Partner) будує мережу агентів і заробляє на кожній угоді своїх агентів без особистої участі. Приклад: 10 активних агентів у мережі (mix рівнів 1/2/3) генерують рекрутеру €5 265 пасивно на місяць. Рекрутер сам регулює % агенту --- чим щедріший %, тим вища мотивація мережі, але нижчий особистий дохід рекрутера.

**8.6 Договірна база агентської моделі**

  ------------------- ----------------- -----------------------------------------------------------------------------------------------
  **Документ**        **Сторони**       **Ключові умови**
  Агентська угода     AITA ↔ Агент      Невиключна; розподіл 80/20; автовиплата; рівні; Telegram-бот; антиобхід 12 міс.
  Партнерська угода   AITA ↔ Рекрутер   Пасивний дохід з мережі; статус Team Builder; заборона переманювання; 1 рік + автопролонгація
  ------------------- ----------------- -----------------------------------------------------------------------------------------------

**8.7 Інтеграція з основною екосистемою**

Агентська модель --- окремий P&L всередині AITA, незалежний від project-financing. Проте можливий синергічний ефект: агент з мережі (продає обладнання) може одночасно бути девелопером на Platform (лістингує проект) або познайомити AITA з інвестором через свій B2B-контакт. AITA свідомо не обмежує ці перетини --- кожний договір регулює свій контекст.

Ключовий принцип обох моделей: AITA заробляє лише при Successful Closing / Confirmed Transaction. Немає угоди --- немає комісії. Це створює довіру з обох боків і робить incentive structure повністю узгодженою між AITA та її партнерами.

**9. МАРКЕТИНГОВИЙ БЛОК (MARKETING ENGINE)**

Третя комерційна модель AITA --- цифровий маркетинг та генерація лідів для компаній у сфері відновлюваної енергетики. На відміну від project-financing (Моделі 1) та агентської мережі (Моделі 2), Маркетинговий блок генерує передбачуваний recurring revenue: депозити + щомісячний потік лідів + Success Fee при закритті угоди. Клієнт --- будь-яка компанія (EPC, дистриб'ютор, девелопер), якій потрібен керований потік кваліфікованих B2B-лідів на ринку відновлюваної енергетики.

**9.1 Суть маркетингової моделі**

AITA не є класичним рекламним агентством. Це інтегрований маркетинговий оператор, що поєднує AI-таргетинг, Telegram-автоматизацію, CRM-інфраструктуру та мережу агентів в одному контракті. Клієнт отримує не \"клік\" --- а Кваліфікований лід, що пройшов автоматичну воронку і підтвердив готовність до покупки.

+-------------------------------------------------------------------------+-------------------------------------------------------------------------------------------+
| **Класичне агентство**                                                  | **AITA Marketing Engine**                                                                 |
|                                                                         |                                                                                           |
| *Бюджет → Рекламна платформа → Кліки → Ліди (вхідні) → Відділ продажів* | *Депозит → AI-кампанія → Telegram Bot (кваліфікація) → Кваліфікований лід → CRM Deal_ID* |
|                                                                         |                                                                                           |
| Оплата за покази / кліки --- без гарантії якості                        | Оплата лише за Кваліфікований лід (€30) + Success Fee 1,5% після угоди                    |
+-------------------------------------------------------------------------+-------------------------------------------------------------------------------------------+

**9.2 Склад послуг та цінова модель**

Повний каталог послуг AITA Marketing. Клієнт обирає пакет послуг в Ордері; базові опції (Sales Node, Network Support) включені в LaaS-контракт автоматично.

  --------- ----------------------------------- -------------------------------------------------------------------------------------------------------------------------------------------------------------------------- -----------------------------------
  **№**     **Послуга**                         **Склад**                                                                                                                                                                  **Вартість**
  **9.1**   LaaS Lead-as-a-Service              Рекламні кампанії (Google, Facebook, Instagram); AI-таргетинг власників будівель; автокваліфікація через Telegram-бот; дашборд лідів у реальному часі; A/B-тестування      €30 / кваліф. лід +депозит €2 000
  **9.2**   Sales Node Telegram-бот-мережа      Автозбір даних покупця + Deal_ID у CRM; автогенерація PDF-пропозицій з 3 рівнями цін; до 7 ботів; онбординг агентів і скрипти продажів                                    Включено в LaaS
  **9.3**   Інтегрована Landing Page            Висококонверсійна сторінка, синхронізована з CRM; адаптивний дизайн (mobile-first); Quick SKU --- каталог з актуальними цінами (Deye, JinKO, HUAWEI); шаблони документів   €1 500 одноразово
  **9.4**   Network Support (Масштабування)     Автоматичний розрахунок комісій агентам мережі; Lot Aggregation --- об\'єднання дрібних замовлень у партії зі знижкою до 7%; дашборди продуктивності агентів і конверсії   Включено в LaaS
  **9.5**   AITA Workspace AI-CRM + Телефонія   IP-телефонія, інтегрована у платформу; AI-транскрипція дзвінків + витяг ключових пунктів; автостворення завдань у CRM після дзвінка; AITA Assist --- AI-асистент           €25 / користувач / міс.
  **9.6**   Success Fee Платформова комісія     Безперервна оптимізація лід-кампаній; контроль якості лідів і фільтрація; доступ до AITA Marketplace з цінами виробників Tier-1; технічна підтримка                        1,5% від угоди після оплати
  --------- ----------------------------------- -------------------------------------------------------------------------------------------------------------------------------------------------------------------------- -----------------------------------

**9.3 Структура доходу AITA від маркетингу**

Маркетингова модель генерує три типи доходу: авансовий (передбачуваний), потоковий (масштабований) і транзакційний (performance-based). Це дозволяє AITA балансувати cashflow незалежно від циклічності проектного фінансування.

  ---------------- -------------------------------------------------------- ------------- ------------------------------------------
  **Тип доходу**   **Джерело**                                              **Частота**   **Рівень передбачуваності**
  Авансовий        Рекламний депозит €2 000 при старті LaaS                 Один раз      Висока --- 100% передоплата
  Потоковий        €30 × N лідів / місяць; €25 × K користувачів Workspace   Щомісяця      Середня --- залежить від обсягу кампанії
  Разовий          Landing Page €1 500 (10%+30%+60% за етапами)             Проектний     Висока --- фіксований
  Транзакційний    Success Fee 1,5% від вартості закритої угоди клієнта     Після угоди   Низька --- performance-based
  ---------------- -------------------------------------------------------- ------------- ------------------------------------------

**9.4 Воронка клієнта (Customer Journey)**

  ---------- -------------------- -----------------------------------------------------------------------------------------------------------------------------------------------------------------------
  **Етап**   **Актор**            **Дія / Результат**
  **1**      AITA                 Запуск таргетованих кампаній (Google / Facebook / Instagram) на власників будівель, EPC-компанії, девелоперів; геотаргетинг + AI-сегментація за інтересами (PV, BESS)
  **2**      Потенційний клієнт   Бачить рекламу → переходить на Landing Page або вступає у Sales Node (Telegram-бот)
  **3**      Telegram Bot         Автокваліфікація: збір місцезнаходження, тип об\'єкта, потужність, готовність до покупки; призначення Deal_ID у CRM
  **4**      AITA / Агент         Кваліфікований лід передається Клієнту; генерується PDF-пропозиція з 3 рівнями цін автоматично
  **5**      Клієнт               Обробляє лід у власному відділі продажів або через агента AITA; веде переговори
  **6**      Клієнт + AITA        Закрита угода → Клієнт сповіщає AITA про оплату → AITA нараховує Success Fee 1,5%
  ---------- -------------------- -----------------------------------------------------------------------------------------------------------------------------------------------------------------------

**9.5 Інтеграція маркетингового блоку з агентською мережею**

Маркетинговий блок та агентська мережа не є ізольованими: кожен агент з мережі (§8) може одночасно бути Sales Node Клієнта маркетингової моделі. Агент отримує ліди через LaaS-кампанії AITA і закриває угоди, що автоматично генерує комісію агента + Success Fee для AITA. Таким чином один і той самий суб\'єкт може брати участь в обох моделях одночасно --- без конфлікту інтересів.

  ------------------------- -------------------------------------------------------- ---------------------------------------------------------------- --------------------------
  **Модель**                **Роль AITA**                                            **Роль агента / партнера**                                       **Синергія**
  Агентська мережа (§8)     Постачальник товару; 20% від маржі                       Знаходить покупця; отримує 30--60%                               Агент продає товари AITA
  Маркетинговий блок (§9)   Генератор лідів; 1,5% Success Fee                        Закриває ліди як Sales Node Клієнта                              Агент = Sales Node
  Синергія                  Агент = Sales Node для лідів клієнтів Marketing Engine   AITA: подвійний дохід --- комісія агента + Success Fee клієнта   Crossover
  ------------------------- -------------------------------------------------------- ---------------------------------------------------------------- --------------------------

**9.6 Договірна база маркетингового блоку**

  --------------------------------- --------------- ------------------------------------------------------------------------------------------------------------------------------------------------
  **Документ**                      **Сторони**     **Ключові умови**
  Маркетинговий договір (Послуги)   AITA ↔ Клієнт   LaaS €30/лід + депозит €2 000; Landing Page €1 500; Workspace €25/user/міс.; Success Fee 1,5%; 3 місяці + автопролонгація; арбітраж CAM Мадрид
  Агентська угода (§8)              AITA ↔ Агент    Агент = Sales Node для лідів Marketing Engine; комісія за угоду агента окрема від Success Fee клієнта
  Ордер на послуги                  AITA ↔ Клієнт   Додаток до Маркетингового договору; фіксує ринок, пакет послуг, кількість лідів, бюджет депозиту, строк кампанії
  --------------------------------- --------------- ------------------------------------------------------------------------------------------------------------------------------------------------

*Документ підготовлено для внутрішнього використання AITA WORLD, S.L. Березень 2026.*


---

# ═══ NDA (EN) ═══

_______________, «___» ________________ 2026

**NON-DISCLOSURE AGREEMENT**

*(NDA --- Confidentiality Agreement)*

This Non-Disclosure Agreement (hereinafter --- the \"**Agreement**\") is entered into between:

  ---------- ---------------------------------------------------------------------------------------
  **AITA**   **AITA WORLD, S.L.**
             **CIF:** B75859744 \| company incorporated under the laws of Spain
             **Address:** Sabino Arana, 8-2, 48013 Bilbao, Bizkaia, España
             **Represented by:** Dmytro Mekhed, Director, acting under the Articles of Association
             **e-mail:** d.mekhed\@aita.world \| **web:** aita.world
             (hereinafter --- \"**Party 1**\" or \"**AITA**\")
  ---------- ---------------------------------------------------------------------------------------

**and**

+-------+-------------------------------------------------------------------------------------------------------------+
| **2** |                                                                                                             |
|       |                                                                                                             |
|       | *Full legal name of the organization / FOP name*                                                            |
+-------+-------------------------------------------------------------------------------------------------------------+
|       | **Registration / Tax No.:** [                    ]                                              |
+-------+-------------------------------------------------------------------------------------------------------------+
|       | **Legal / registered address:**                                                                             |
|       |                                                                                                             |
|       |                                                                                                             |
|       |                                                                                                             |
|       | *street, city, postal code, country*                                                                        |
+-------+-------------------------------------------------------------------------------------------------------------+
|       | **Represented by:**                                                                                         |
|       |                                                                                                             |
|       |                                                                                                             |
|       |                                                                                                             |
|       | *Full name, title --- authority basis: Articles of Association / Power of Attorney No. ___ dated ___* |
+-------+-------------------------------------------------------------------------------------------------------------+
|       | **e-mail:** [                            ]  tel.: [                      ]          |
+-------+-------------------------------------------------------------------------------------------------------------+
|       | (hereinafter --- \"**Party 2**\" or \"**Client**\")                                                         |
+-------+-------------------------------------------------------------------------------------------------------------+

Party 1 and Party 2 are collectively referred to as the \"**Parties**\", and each individually as a \"**Party**\".\
Legal basis: **Civil Code of Ukraine** (Articles 505--508, 626--648), Commercial Code of Ukraine, Law of Ukraine \"**On Information**\", Law of Ukraine \"**On Personal Data Protection**\".

**1. DEFINITIONS**

**1.1 **\"Confidential Information\" means any information disclosed by one Party (the \"Disclosing Party\") to the other (the \"Receiving Party\") in written, oral, or electronic form, including: business plans, financial data, technical solutions, client lists, deal terms, trade secrets, know-how, IT architecture, algorithms, reports, price lists, and personal data.

**1.2 **\"Representatives\" means directors, employees, consultants, and contractors of a Party to whom Confidential Information is disclosed solely to the extent necessary for the Purpose (§2.1).

**1.3 **\"Purpose\" means the evaluation, negotiation, and/or execution of a potential or existing business collaboration between the Parties in AITA\'s field of activity (energy projects, investment facilitation, technology platform).

**1.4 **\"Public Information\" means information that has lawfully become generally available without breach of this Agreement.

**2. OBLIGATIONS OF THE PARTIES**

**2.1 **Each Party undertakes to: (a) maintain confidentiality of all received Confidential Information; (b) not disclose it to third parties without prior written consent of the other Party; (c) use it solely within the Purpose; (d) ensure a level of protection no less than that applied to its own confidential information, but not less than \"reasonable care\".

**2.2 **The Receiving Party may disclose Confidential Information to its Representatives only to the extent necessary for the Purpose. The Party bears full responsibility for its Representatives\' actions.

**2.3 **Confidential Information in written or electronic form shall be marked \"Confidential\" / \"CONFIDENTIAL\". The absence of such marking does not negate the confidential nature of information that is obvious from context.

**3. EXCEPTIONS**

Confidentiality obligations do not apply to information that the Receiving Party can document as:

-   a\) was publicly available prior to disclosure or became so without breach of this Agreement;

-   b\) was already known to the Receiving Party prior to disclosure without any confidentiality restriction;

-   c\) was received from a third party without that party breaching any confidentiality obligation;

-   d\) was independently developed by the Receiving Party without use of the Confidential Information;

-   e\) is required to be disclosed by law or a competent authority --- provided the other Party is notified in advance in writing and only the minimum necessary information is disclosed.

**4. TERM OF THE AGREEMENT**

**4.1 **This Agreement enters into force upon signature by both Parties and remains in effect for 3 (three) years, unless the Parties agree otherwise in writing.

**4.2 **Confidentiality obligations regarding trade secrets and know-how survive indefinitely --- even after the Agreement\'s expiry.

**4.3 **Either Party may terminate this Agreement early by providing written notice to the other Party 30 (thirty) calendar days in advance. Termination does not release either Party from obligations regarding Confidential Information already received.

**5. RETURN AND DESTRUCTION OF INFORMATION**

**5.1 **Upon first request of the Disclosing Party or upon Agreement expiry, the Receiving Party shall: (a) return all physical media containing Confidential Information, or (b) destroy them (including electronic copies) and provide written confirmation of destruction within 5 (five) business days.

**5.2 **Copies required to be retained under applicable law or internal compliance procedures may be kept, provided confidentiality is maintained.

**6. INTELLECTUAL PROPERTY RIGHTS**

**6.1 **This Agreement does not transfer or grant any rights to intellectual property, trademarks, patents, or licenses of either Party. Disclosure of Confidential Information does not constitute a public offer or an obligation to enter into any other agreement.

**6.2 **All rights to the Confidential Information remain with the Disclosing Party.

**7. LIABILITY**

**7.1 **In the event of a breach of this Agreement, the breaching Party shall indemnify the other Party for all documented losses (including lost profits) in accordance with applicable law.

**7.2 **A breach of confidentiality may cause irreparable harm; therefore, the aggrieved Party is entitled to seek injunctive relief without proving the extent of damages.

**Limitation of Liability:**

  ------------------------------------- ---------------------------------------------------------------------
  **Type of Loss**                      **Compensation Condition**
  **Direct documented losses**          Compensated in full
  **Lost profits**                      Compensated upon documentary proof
  **Indirect / consequential losses**   Excluded, except in cases of willful misconduct or gross negligence
  ------------------------------------- ---------------------------------------------------------------------

**8. PERSONAL DATA PROTECTION**

**8.1 **Processing of personal data in connection with this Agreement shall be carried out in accordance with applicable data protection legislation, including GDPR (Regulation (EU) 2016/679) where applicable. Each Party acts as an independent controller of its own personal data.

**8.2 **The Parties shall not transfer personal data of individuals to third countries without appropriate legal grounds and shall apply technical and organizational measures to protect such data.

**9. GOVERNING LAW AND DISPUTE RESOLUTION**

**9.1 **This Agreement is governed by the laws of the Kingdom of Spain. Matters not addressed in the Agreement shall be resolved in accordance with applicable Spanish civil law.

**9.2 **All disputes shall be resolved through negotiations within 15 (fifteen) calendar days from the date of written notification of the dispute.

**9.3 **If no agreement is reached, the dispute shall be referred to (the Parties select one option at signing):

> **□ ICC Arbitration:** International Court of Arbitration, ICC Rules, seat --- Madrid, language --- English;
>
> **□ CAM Arbitration:** Corte de Arbitraje de Madrid, seat --- Madrid, language --- English.

**10. GENERAL PROVISIONS**

**10.1 **Language. This Agreement is executed in English. Any translations are for informational purposes only; in case of discrepancy, the English version prevails.

**10.2 **Amendments. All amendments and additions are valid only in written form and signed by authorized representatives of both Parties.

**10.3 **Assignment. Neither Party may assign rights or obligations under this Agreement without the prior written consent of the other Party.

**10.4 **Severability. The invalidity of any provision does not affect the validity of the remaining provisions of this Agreement.

**10.5 **Entire Agreement. This Agreement constitutes the entire and final expression of the Parties\' intentions regarding its subject matter and supersedes all prior oral and written understandings.

**10.6 **Counterparts. This Agreement is executed in two (2) equally valid originals. A signed scan copy or electronic document (qualified e-signature) has the same legal force as a paper original.

**10.7 **Notices. Official correspondence shall be conducted at the contact details set out in Section 11. A notice is deemed received: by post --- on the 3rd day after dispatch; by e-mail --- on the day of dispatch with delivery confirmation.

**11. PARTIES\' DETAILS AND SIGNATURES**

+----------------------------------------------------+-----------------------------------------------------------------------+
| **PARTY 1**                                        | **PARTY 2 (CLIENT)**                                                  |
+----------------------------------------------------+-----------------------------------------------------------------------+
| **AITA WORLD, S.L.**                               |                                                                       |
|                                                    |                                                                       |
|                                                    | *full legal name*                                                     |
+----------------------------------------------------+-----------------------------------------------------------------------+
| **CIF:** B75859744                                 | **Reg. / Tax No.:** [                  ]                  |
+----------------------------------------------------+-----------------------------------------------------------------------+
| **Address:** Sabino Arana, 8-2, 48013\             | **Address:**                                                          |
| Bilbao, Bizkaia, España                            |                                                                       |
|                                                    |                                                                       |
|                                                    |                                                                       |
|                                                    | *street, city, postal code, country*                                  |
+----------------------------------------------------+-----------------------------------------------------------------------+
| **Bank:** *Banco Sabadell, IBAN ES__*            | **Bank / IBAN:**                                                      |
|                                                    |                                                                       |
|                                                    |                                                                       |
|                                                    |                                                                       |
|                                                    | *bank name, account or IBAN*                                          |
+----------------------------------------------------+-----------------------------------------------------------------------+
| **e-mail:** d.mekhed\@aita.world                   | **e-mail:**                                                           |
|                                                    |                                                                       |
|                                                    |                                                                       |
|                                                    |                                                                       |
|                                                    | **tel.:**                                                             |
|                                                    |                                                                       |
|                                                    |                                                                       |
+----------------------------------------------------+-----------------------------------------------------------------------+
| **Represented by:** Dmytro Mekhed, Director        | **Represented by:**                                                   |
|                                                    |                                                                       |
|                                                    |                                                                       |
|                                                    |                                                                       |
|                                                    | *Full name, title*                                                    |
+----------------------------------------------------+-----------------------------------------------------------------------+
| Basis: Articles of Association of AITA WORLD, S.L. | **Basis:**                                                            |
|                                                    |                                                                       |
|                                                    |                                                                       |
|                                                    |                                                                       |
|                                                    | *Articles of Association / Power of Attorney No. ___ dated ___* |
+----------------------------------------------------+-----------------------------------------------------------------------+

**SIGNATURES:**

+------------------------------------------+----------------------------------------------+
| **Party 1: AITA WORLD, S.L.**            | **Party 2:**                                 |
+------------------------------------------+----------------------------------------------+
|                                          |                                              |
|                                          |                                              |
| *signature*                              | *signature*                                  |
+------------------------------------------+----------------------------------------------+
| Dmytro Mekhed                            |                                              |
|                                          |                                              |
| *full name*                              | *full name*                                  |
+------------------------------------------+----------------------------------------------+
| \"___\" ____________ 2026 | \"___\" ____________ 20___ |
|                                          |                                              |
| *date*                                   | *date*                                       |
+------------------------------------------+----------------------------------------------+
| *Stamp (if applicable)*                  | *Stamp (if applicable)*                      |
+------------------------------------------+----------------------------------------------+

*This Agreement is executed in 2 (two) original copies. A signed scan copy or electronic document (qualified e-signature) has the same legal force as a paper original.*


---

# ═══ NDA (UA) ═══

м. ____________, «___» ________________ 2026 р.

**ДОГОВІР ПРО НЕРОЗГОЛОШЕННЯ КОНФІДЕНЦІЙНОЇ ІНФОРМАЦІЇ**

*(NDA --- Non-Disclosure Agreement)*

Цей Договір про нерозголошення конфіденційної інформації (надалі --- «**Договір**») укладено між:

  ---------- -------------------------------------------------------------------------
  **AITA**   **AITA WORLD, S.L.**
             **CIF:** B75859744 \| компанія, зареєстрована за законодавством Іспанії
             **Адреса:** Sabino Arana, 8-2, 48013 Bilbao, Bizkaia, España
             **В особі:** Dmytro Mekhed, Director, що діє на підставі Статуту
             **e-mail:** d.mekhed\@aita.world \| **web:** aita.world
             (надалі --- «**Сторона 1**» або «**AITA**»)
  ---------- -------------------------------------------------------------------------

**та**

+-------+----------------------------------------------------------------------------------------------------+
| **2** |                                                                                                    |
|       |                                                                                                    |
|       | *Повне найменування організації / ПІБ фізичної особи-підприємця*                                   |
+-------+----------------------------------------------------------------------------------------------------+
|       | **Код ЄДРПОУ / РНОКПП:** [                    ]                                        |
+-------+----------------------------------------------------------------------------------------------------+
|       | **Юридична / фактична адреса:**                                                                    |
|       |                                                                                                    |
|       |                                                                                                    |
|       |                                                                                                    |
|       | *вулиця, місто, поштовий індекс, країна*                                                           |
+-------+----------------------------------------------------------------------------------------------------+
|       | **В особі:**                                                                                       |
|       |                                                                                                    |
|       |                                                                                                    |
|       |                                                                                                    |
|       | *ПІБ, посада --- підстава повноважень: Статут / Довіреність № ___ від ___*                   |
+-------+----------------------------------------------------------------------------------------------------+
|       | **e-mail:** [                            ]  тел.: [                      ] |
+-------+----------------------------------------------------------------------------------------------------+
|       | (надалі --- «**Сторона 2**» або «**Замовник**»)                                                    |
+-------+----------------------------------------------------------------------------------------------------+

Сторона 1 та Сторона 2 разом іменуються «**Сторони**», а кожна окремо --- «**Сторона**».\
Підстава: **Цивільний кодекс України** (статті 505--508, 626--648), Господарський кодекс України, Закон України «**Про інформацію**», Закон України «**Про захист персональних даних**».

**1. ВИЗНАЧЕННЯ ТЕРМІНІВ**

**1.1 **«Конфіденційна інформація» --- будь-яка інформація, що передається однією Стороною («Сторона, що розкриває») іншій («Сторона, що отримує») у письмовій, усній або електронній формі, включаючи: ділові плани, фінансові дані, технічні рішення, клієнтські списки, умови угод, комерційні таємниці, know-how, IT-архітектуру, алгоритми, звіти, прайс-листи, персональні дані.

**1.2 **«Представники» --- керівники, працівники, консультанти та підрядники Сторони, яким Конфіденційна інформація розкривається виключно в обсязі, необхідному для Мети (п. 2.1).

**1.3 **«Мета» --- оцінка, переговори та/або реалізація можливої або наявної ділової співпраці між Сторонами у сфері діяльності AITA (енергетичні проєкти, інвестиційне залучення, технологічна платформа).

**1.4 **«Публічна інформація» --- інформація, що законно стала загальнодоступною без порушення цього Договору.

**2. ЗОБОВ\'ЯЗАННЯ СТОРІН**

**2.1 **Кожна Сторона зобов\'язується: (а) зберігати конфіденційність усієї отриманої Конфіденційної інформації; (б) не розкривати її третім особам без попередньої письмової згоди іншої Сторони; (в) використовувати виключно в рамках Мети; (г) забезпечувати захист не нижчий, ніж для власної конфіденційної інформації, але не менше «розумної обережності».

**2.2 **Сторона, що отримує, може розкривати Конфіденційну інформацію своїм Представникам лише в обсязі, необхідному для Мети. Сторона несе повну відповідальність за дії своїх Представників.

**2.3 **Конфіденційна інформація у письмовій або електронній формі повинна позначатися «Конфіденційно» / «CONFIDENTIAL». Відсутність позначки не скасовує конфіденційного характеру інформації, якщо він є очевидним з контексту.

**3. ВИКЛЮЧЕННЯ**

Зобов\'язання щодо конфіденційності не поширюються на інформацію, яку Сторона, що отримує, може документально довести:

-   а) була загальнодоступною до передачі або стала такою без порушення Договору;

-   б) була відома Стороні, що отримує, до розкриття без обмеження конфіденційністю;

-   в) отримана від третьої особи без порушення нею зобов\'язань конфіденційності;

-   г) розроблена Стороною, що отримує, незалежно та без використання Конфіденційної інформації;

-   ґ) підлягає розкриттю на вимогу закону або компетентного органу --- за умови завчасного письмового повідомлення іншої Сторони та мінімального обсягу розкриття.

**4. СТРОК ДІЇ ДОГОВОРУ**

**4.1 **Цей Договір набирає чинності з дати підписання Сторонами та діє протягом 3 (трьох) років, якщо Сторони письмово не домовляться про інший строк.

**4.2 **Зобов\'язання щодо конфіденційності комерційної таємниці та know-how діють безстроково --- навіть після закінчення строку Договору.

**4.3 **Кожна Сторона вправі достроково розірвати Договір, письмово повідомивши іншу Сторону за 30 (тридцять) календарних днів. Розірвання не звільняє від зобов\'язань щодо вже отриманої Конфіденційної інформації.

**5. ПОВЕРНЕННЯ ТА ЗНИЩЕННЯ ІНФОРМАЦІЇ**

**5.1 **На першу вимогу Сторони, що розкриває, або після закінчення Договору Сторона, що отримує, зобов\'язана: (а) повернути всі матеріальні носії з Конфіденційною інформацією, або (б) знищити їх (включно з електронними копіями) та надати письмове підтвердження знищення протягом 5 (п\'яти) робочих днів.

**5.2 **Допускається зберігання копій, що підлягають зберіганню відповідно до вимог законодавства або внутрішніх комплаєнс-процедур, за умови збереження режиму конфіденційності.

**6. ПРАВА ІНТЕЛЕКТУАЛЬНОЇ ВЛАСНОСТІ**

**6.1 **Цей Договір не передає та не надає будь-яких прав на об\'єкти інтелектуальної власності, торгові марки, патенти або ліцензії Сторін. Розкриття Конфіденційної інформації не є публічною офертою або зобов\'язанням укласти будь-який інший договір.

**6.2 **Усі права на Конфіденційну інформацію залишаються за Стороною, що розкриває.

**7. ВІДПОВІДАЛЬНІСТЬ**

**7.1 **У разі порушення цього Договору Сторона, що порушила, зобов\'язана відшкодувати іншій Стороні всі документально підтверджені збитки (включно з упущеною вигодою) відповідно до чинного законодавства України.

**7.2 **Порушення режиму конфіденційності може завдати невідшкодовних збитків, тому постраждала Сторона вправі звертатись до суду із заявою про вжиття забезпечувальних заходів без доведення розміру збитків.

**Обмеження відповідальності:**

  --------------------------------------------- ------------------------------------------------------------
  **Вид збитків**                               **Умова відшкодування**
  **Прямі документально підтверджені збитки**   Відшкодовуються в повному обсязі
  **Упущена вигода**                            Відшкодовується за наявності документального підтвердження
  **Непрямі / побічні збитки**                  Виключені, крім випадків умислу або грубої недбалості
  --------------------------------------------- ------------------------------------------------------------

**8. ЗАХИСТ ПЕРСОНАЛЬНИХ ДАНИХ**

**8.1 **Обробка персональних даних у зв\'язку з цим Договором здійснюється відповідно до Закону України «Про захист персональних даних» та, у разі передачі даних до/з ЄС, --- Регламенту (ЄС) 2016/679 (GDPR). Кожна Сторона є незалежним контролером власних баз персональних даних.

**8.2 **Сторони не передають персональні дані фізичних осіб третім країнам без відповідних правових підстав та вживають технічних і організаційних заходів для захисту таких даних.

**9. ЗАСТОСОВНЕ ПРАВО ТА ВИРІШЕННЯ СПОРІВ**

**9.1 **Цей Договір регулюється законодавством України. Питання, не врегульовані Договором, вирішуються відповідно до норм Цивільного кодексу України.

**9.2 **Усі спори Сторони намагаються врегулювати шляхом переговорів протягом 15 (п\'ятнадцяти) календарних днів з дати отримання письмового повідомлення про спір.

**9.3 **У разі недосягнення згоди спір передається до (Сторони обирають один варіант при підписанні):

> **□ МКАС:** Міжнародний комерційний арбітражний суд при ТПП України, м. Київ, 1 арбітр, мова --- укр./англ.;
>
> **□ Господарський суд:** за місцем реєстрації відповідача (Господарський суд відповідної області).

**10. ЗАГАЛЬНІ ПОЛОЖЕННЯ**

**10.1 **Мова. Цей Договір складено українською мовою. Переклад надається виключно для інформаційних цілей; у разі розбіжностей --- переважає українська мова.

**10.2 **Зміни. Усі зміни та доповнення дійсні лише у письмовій формі та підписані уповноваженими представниками обох Сторін.

**10.3 **Відступлення. Жодна зі Сторін не вправі відступити права чи обов\'язки за цим Договором без письмової згоди іншої Сторони.

**10.4 **Роздільність. Недійсність будь-якого положення не впливає на дійсність інших положень цього Договору.

**10.5 **Повнота. Цей Договір є повним та остаточним виразом волі Сторін щодо предмету Договору та замінює всі попередні усні й письмові домовленості.

**10.6 **Примірники. Договір укладається у двох рівнозначних примірниках. Договір, підписаний електронним підписом (КЕП/ПЕП), має таку ж юридичну силу, як паперовий оригінал.

**10.7 **Повідомлення. Офіційне листування здійснюється за реквізитами, зазначеними у Розділі 11. Повідомлення вважається отриманим: поштою --- на 3-й день після відправлення, e-mail --- у день відправлення з підтвердженням доставки.

**11. РЕКВІЗИТИ ТА ПІДПИСИ СТОРІН**

+-----------------------------------------+-----------------------------------------------------------+
| **СТОРОНА 1**                           | **СТОРОНА 2 (ЗАМОВНИК)**                                  |
+-----------------------------------------+-----------------------------------------------------------+
| **AITA WORLD, S.L.**                    |                                                           |
|                                         |                                                           |
|                                         | *повне найменування*                                      |
+-----------------------------------------+-----------------------------------------------------------+
| **CIF:** B75859744                      | **Код ЄДРПОУ / РНОКПП:** [                  ] |
+-----------------------------------------+-----------------------------------------------------------+
| **Адреса:** Sabino Arana, 8-2, 48013\   | **Адреса:**                                               |
| Bilbao, Bizkaia, España                 |                                                           |
|                                         |                                                           |
|                                         |                                                           |
|                                         | *вулиця, місто, індекс, країна*                           |
+-----------------------------------------+-----------------------------------------------------------+
| **Банк:** *Banco Sabadell, IBAN ES__* | **Банк / IBAN:**                                          |
|                                         |                                                           |
|                                         |                                                           |
|                                         |                                                           |
|                                         | *назва банку, р/р або IBAN*                               |
+-----------------------------------------+-----------------------------------------------------------+
| **e-mail:** d.mekhed\@aita.world        | **e-mail:**                                               |
|                                         |                                                           |
|                                         |                                                           |
|                                         |                                                           |
|                                         | **тел.:**                                                 |
|                                         |                                                           |
|                                         |                                                           |
+-----------------------------------------+-----------------------------------------------------------+
| **В особі:** Dmytro Mekhed, Director    | **В особі:**                                              |
|                                         |                                                           |
|                                         |                                                           |
|                                         |                                                           |
|                                         | *ПІБ, посада*                                             |
+-----------------------------------------+-----------------------------------------------------------+
| Підстава: Статут AITA WORLD, S.L.       | **Підстава:**                                             |
|                                         |                                                           |
|                                         |                                                           |
|                                         |                                                           |
|                                         | *Статут / Довіреність № ___ від ___*                |
+-----------------------------------------+-----------------------------------------------------------+

**ПІДПИСИ СТОРІН:**

+-------------------------------------------+-----------------------------------------------+
| **Сторона 1: AITA WORLD, S.L.**           | **Сторона 2:**                                |
+-------------------------------------------+-----------------------------------------------+
|                                           |                                               |
|                                           |                                               |
| *підпис*                                  | *підпис*                                      |
+-------------------------------------------+-----------------------------------------------+
| Dmytro Mekhed                             |                                               |
|                                           |                                               |
| *ПІБ*                                     | *ПІБ*                                         |
+-------------------------------------------+-----------------------------------------------+
| «___» ____________ 2026 р. | «___» ____________ 20___ р. |
|                                           |                                               |
| *дата*                                    | *дата*                                        |
+-------------------------------------------+-----------------------------------------------+
| *М.П. (за наявності)*                     | *М.П. (за наявності)*                         |
+-------------------------------------------+-----------------------------------------------+

*Договір складено у 2 (двох) оригінальних примірниках. Підписаний скан-копія або електронний документ (КЕП) мають таку ж юридичну силу, як паперовий оригінал.*


---

# ═══ INVESTMENT OWN PROJECTS v2 ═══

**AITA × CLIMATE CAPITAL**

**UK Project Capital & Portfolio Framework Agreement**

*(AITA Own Projects --- Platform-Governed Execution)*

Effective Date: \[●\]

+-----------------------------------------------------------------------------+
| **Parties:**                                                                |
|                                                                             |
| **(1)** AITA World S.L. *--- Spain, Bilbao (originator, platform operator)* |
|                                                                             |
| **(2)** Climate Capital \[●\] *--- England & Wales (capital arranger)*      |
+-----------------------------------------------------------------------------+

**TABLE OF CONTENTS --- ALL SERVICES & SECTIONS**

**0. PRE-SALE ACCESS TO AITA PLATFORM**

> Limited invite-only access \| €500 per seat + AITA branded merchandise

**PART I --- EXTERNAL (Commercial Terms & Project Conditions)**

> **1. Background and Intent** --- Purpose, pipeline origin, reality-first approach
>
> **2. Definitions** --- Key terms: Platform, Digital Annex, Disposition Rights, Proof of Funds, B2B Package, Cost of Funds, Upside Spread
>
> **3. Scope and Priority Pipeline** --- €120M pipeline, 20% equity, 2026--2027 deployment, 5-criteria execution chain
>
> **4. Reality Gates and Execution Discipline** --- Proof of Funds + B2B Package mandatory before fundraising
>
> **5. Term and Exclusivity** --- 24-month term, 6-month zero-fee exclusivity, milestone-linked
>
> **6. Performance Milestones** --- Kick-off 5 days, PoF 30 days, Term Sheet 45 days, Closing Plan 60 days
>
> **7. Economics: Upside Sharing** --- 50/50 split on Upside Spread, no hidden fees
>
> **8. Cost of Funds: Disclosure & Auditability** --- Full breakdown required, independent expert for disputes
>
> **9. Portfolio Waterfall & Residual Cash** --- 5-tier: debt → investor return → reserves → reinvestment → distribution
>
> **10. Non-Circumvention / Non-Bypass** --- 24-month post-term, liquidated damages, pre-existing relationship exception
>
> **11. Injunctive Relief and Specific Performance** --- Court remedies for NDA/non-circumvention breaches
>
> **12. Termination and Project Continuity** --- 15 business days to cure, accrued rights survive
>
> **13. Representations and Disclaimers** --- No financial advice, regulatory responsibility on CC
>
> **14. Governing Law and Jurisdiction** --- England & Wales

**PART II --- INTERNAL (Operational Framework & Platform Governance)**

> **15. AITA Platform as Single Source of Truth** --- Exclusive environment, Evidence Ledger, conflict priority rules
>
> **16. Digital Annexes** --- Project-level schedules, binding once approved, 12-point minimum
>
> **17. AITA Obligations (Operational)** --- Disposition Rights, Audit Pack, tendering, platform workflow
>
> **18. Climate Capital Obligations (Operational)** --- Financing process, Proof of Funds upload, documentation
>
> **19. Competitive Tendering** --- Minimum 3 bids, evaluation matrix, Evidence Ledger
>
> **20. Confidentiality and Data Controls** --- 5-year NDA, trade secrets indefinite, UK GDPR compliance
>
> **21. IP and Platform Rights** --- AITA IP, limited CC licence, joint-ownership rules
>
> **22. Notices** --- Platform notice + email, deemed receipt rules
>
> **23. Miscellaneous** --- Entire agreement, amendments, assignment, severability

**ANNEXES**

> **A.** Digital Annex Template (Project Schedule) --- 12-point minimum checklist

**SECTION 0**

**PRE-SALE ACCESS TO AITA PLATFORM**

**Context:** AITA operates on an invite-only model. Platform access is limited to verified participants who meet qualification criteria. To manage demand and ensure quality of the participant pool, AITA offers a Pre-Sale Access programme.

  ------------------- --------------------------------------------------------------------------------------------------
  **Parameter**       **Details**
  **Access Fee**      €500 per seat (one-time, non-refundable)
  **Includes**        Full platform access (role-based) + AITA branded merchandise (t-shirt, welcome pack)
  **Invite Model**    Strictly invite-only; each seat linked to a named user and company entity
  **Validity**        Access activated upon payment confirmation; valid for the Term of this Agreement
  **Capacity**        Limited seats per cohort --- AITA reserves the right to cap the number of participants per round
  **Refund Policy**   Non-refundable; access fee covers onboarding, platform provisioning, and merchandise
  **Upgrade Path**    Pre-Sale participants receive priority access to future portfolio rounds and expanded features
  ------------------- --------------------------------------------------------------------------------------------------

**0.1 **The Pre-Sale Access Fee is a commercial access charge and does not constitute an investment, deposit, or commitment to any specific Project. It grants the participant the right to view, evaluate, and interact with Projects on the AITA Platform under role-based permissions.

**0.2 **AITA may, at its discretion, offer promotional pricing, early-bird discounts, or waive the access fee for strategic partners. Any such variation shall be recorded in the AITA Platform.

**0.3 **The branded merchandise (AITA t-shirt and welcome pack) is dispatched within 15 business days of access confirmation and is provided as part of the participant onboarding experience.

**PART I**

**EXTERNAL --- Commercial Terms & Project Conditions**

**1. Background and Intent**

**1.1 **AITA originates and controls a pipeline of renewable energy projects and related assets (\"Projects\"), and operates a proprietary digital platform (\"AITA Platform\") designed to govern verification, audit, tendering, deal structuring, and portfolio execution.

**1.2 **CC has relationships and capability to arrange and secure financing for Projects, including equity and debt, and to coordinate closing with banks, investors, and other capital providers.

**1.3 **The Parties wish to enter into this Agreement as a binding operational framework under which Projects are executed through the AITA Platform, and CC is granted a defined right to raise funds subject to strict reality gates (Proof of Funds + back-to-back deliverability).

**2. Definitions**

In this Agreement:

> **\"AITA Platform\"** means AITA\'s proprietary system (including dashboards, task workflows, project pages, data rooms, audit packs, evidence logs, chat, and exports), as updated from time to time.
>
> **\"Digital Annex\"** means a Project Page / Project Schedule / Portfolio Schedule created inside the AITA Platform and incorporated into this Agreement by reference in accordance with Section 16.
>
> **\"Disposition Rights\"** means AITA\'s legal and/or contractual authority to develop, assign, sell, transfer, or otherwise dispose of rights relating to a Project (including land rights, permits, exclusivity, SPV control, development agreements, grid position, or other enforceable rights), evidenced in the AITA Platform.
>
> **\"Internal Audit Pack\"** means AITA\'s audit and verification materials for a Project including technical, legal, commercial, and financial documentation, baseline models and assumptions, risk register, and deal plan.
>
> **\"Proof of Funds\"** means documentary evidence reasonably acceptable to AITA that CC has secured real capital capacity for the relevant Project or portfolio, such as an executed mandate, binding commitment letter, approved term sheet, credit committee approval, or investor subscription commitment (as applicable), posted in the AITA Platform.
>
> **\"Back-to-Back Package\" (\"B2B Package\")** means the minimum bankable chain of deliverable contracts/terms required to execute the Project economics (EPC/O&M/offtake/buyer/insurance/grid/land) or a written plan evidencing how such chain will be finalised, as recorded in the AITA Platform.
>
> **\"Cost of Funds\"** means the all-in effective cost of capital arranged by CC including interest, fees, commissions, arrangement and placement fees, OID, hedging, and any third-party charges, computed and disclosed per Section 8.
>
> **\"Upside Spread\"** means the net economic value attributable to the delta between Project returns and Cost of Funds and/or financing efficiency and commercial optimisation, calculated per Digital Annex.
>
> **\"Protected Parties\"** means investors, lenders, banks, brokers, contractors, EPCs, O&M providers, off-takers, buyers, landowners, grid entities, SPVs, advisors, and any other material counterparties first identified, introduced, or materially enabled through the AITA Platform or through the Parties\' cooperation under this Agreement.

**3. Scope and Priority Pipeline**

**3.1 **This Agreement governs AITA\'s own Projects introduced to CC via the AITA Platform and confirmed under a Digital Annex.

**3.2 **The first collaboration priority is a pipeline targeted at €120,000,000 total Project value, with the objective to secure 20% equity for deployment in 2026--2027, limited to markets where AITA confirms the full execution chain:

-   \(a\) Project rights and data;

-   \(b\) technical and legal verification;

-   \(c\) competitive tender (minimum three contractors);

-   \(d\) monetisation route (asset sale and/or offtake/merchant strategy);

-   \(e\) O&M / asset management capability (or validated third-party operator).

**4. Reality Gates and Execution Discipline**

**4.1 **The Parties explicitly agree that AITA is granting CC the opportunity to raise capital, but only on a reality-first basis. No Project shall move into fundraising execution unless:

-   \(a\) Proof of Funds has been provided by CC and recorded in the AITA Platform; and

-   \(b\) the B2B Package has been initiated and deemed deliverable within the timeline in the Digital Annex.

**4.2 **CC acknowledges that \"soft interest\", non-committal discussions, or unverified investor indications do not qualify as Proof of Funds.

**4.3 **AITA may pause or remove a Project from execution if the Reality Gates are not met, without liability, subject to Section 12.

**5. Term and Exclusivity**

**5.1 **Term: This Agreement begins on the Effective Date and continues for 24 months, unless terminated earlier under Section 12.

**5.2 **Six-Month Exclusivity (Zero-Fee): For six (6) months from the Effective Date, AITA grants CC exclusivity to arrange financing for Projects added to Digital Annexes during the exclusivity period without any retainer/management fee payable to CC, subject to:

-   \(a\) CC meeting the Reality Gates per Section 4 for each Project; and

-   \(b\) CC meeting the performance milestones in Section 6 and any additional milestones defined in a Digital Annex.

**5.3 **If CC fails to meet milestones for a Project, exclusivity for that Project may be removed by AITA immediately via platform notice.

**6. Performance Milestones (Binding Execution Standards)**

**6.1 **The Parties agree that the purpose of exclusivity is rapid execution. Accordingly, for each Project added under exclusivity, CC shall meet the following minimum milestones unless a Digital Annex specifies different dates:

  -------------------- -------------- ------------------------------------------------------------------------------------------------------------------
  **Milestone**        **Deadline**   **Requirement**
  **Kick-off**         5 BD           CC confirms financing strategy, target investor/lender set, and responsible CC lead(s) inside the AITA Platform.
  **Proof of Funds**   30 days        CC uploads Proof of Funds to the AITA Platform.
  **Term Sheet**       45 days        CC uploads at least one actionable financing term sheet or binding investor commitment.
  **Closing Plan**     60 days        CC publishes a realistic closing plan (CPs, timeline, docs, responsible parties) inside the AITA Platform.
  -------------------- -------------- ------------------------------------------------------------------------------------------------------------------

**6.2 **If CC fails to meet any milestone for a Project, AITA may, at its sole discretion and via AITA Platform notice: (a) remove exclusivity for that Project immediately; (b) pause the Project until readiness is restored; and/or (c) reassign fundraising execution for that Project to another party, without liability to CC.

**6.3 **If CC fails to meet milestones for two (2) Projects in any rolling ninety (90) day period, AITA may terminate the exclusivity arrangement for the remaining pipeline with immediate effect.

**6.4 **Milestones are measured from the date the Project is marked \"Activated\" in the AITA Platform Evidence Ledger.

**7. Economics: Upside Sharing**

  ------------------------- --------------------------------------------------------------------------------------------------------------------------------------
  **Parameter**             **Terms**
  **Upside Spread Split**   50% AITA / 50% CC --- calculated per Project or portfolio, specified in Digital Annex.
  **Undisclosed Fees**      Any fee/commission not disclosed and recorded in the AITA Platform shall NOT be included in Cost of Funds, and shall be borne by CC.
  **Additional Fees**       Performance fees, carry, or success fees must be explicitly stated in the Digital Annex; otherwise none apply.
  ------------------------- --------------------------------------------------------------------------------------------------------------------------------------

**8. Cost of Funds: Disclosure and Auditability**

**8.1 **For each financing close, CC shall provide a Cost of Funds Statement in the AITA Platform describing: base rate, margin, fees, commissions, hedging, OID, arranger/placement fees, legal/structuring costs, and an effective annualised cost.

**8.2 **AITA may request evidence reasonably necessary to verify Cost of Funds (fee letters, invoices, mandate terms), subject to confidentiality protections in Section 20.

**8.3 **If AITA reasonably disputes the Cost of Funds calculation, the Parties shall appoint an independent financial expert (mutually agreed) to determine the correct calculation; cost shared equally unless the expert finds a material misstatement by one Party.

**9. Portfolio Waterfall and Use of Residual Cash**

**9.1 **Portfolio cashflows are applied in the following order, unless a Digital Annex states otherwise due to bank requirements:

  ---------- -------------------------------------------------------------------------------------------------
  **Tier**   **Application**
  **(a)**    Senior debt service and bank covenants (interest, principal, fees)
  **(b)**    Investor repayment / preferred return (as applicable)
  **(c)**    Operating reserves, compliance, and essential project obligations
  **(d)**    Reinvestment into Projects and/or joint infrastructure until Phase 1 infrastructure sufficiency
  **(e)**    After Phase 1, remaining distributable cash per Upside Sharing and Digital Annex rules
  ---------- -------------------------------------------------------------------------------------------------

**9.2 **AITA Platform shall provide transparent, near real-time reporting of the waterfall, with access rights defined in the Digital Annex.

**9.3 **Phase 1 Infrastructure Sufficiency means the agreed level of shared infrastructure that enables continuous execution/construction (e.g., legal, technical, procurement, operations capacity), defined and tracked in the AITA Platform.

**10. Non-Circumvention / Non-Bypass**

**10.1 **Each Party agrees that, during the Term and for twenty-four (24) months thereafter, it shall not directly or indirectly circumvent the other Party by engaging, soliciting, contracting, or transacting outside the AITA Platform with any Protected Parties introduced or made available through this cooperation, for the purpose of avoiding this Agreement or depriving the other Party of its economic benefit.

**10.2 **If a breach occurs, the breaching Party shall (without prejudice to other remedies) pay the non-breaching Party liquidated damages equal to the economic benefit the non-breaching Party would reasonably have received under the applicable Digital Annex (including its 50% share of Upside Spread), plus reasonable enforcement costs.

**10.3 **This Section does not prevent a Party from engaging with third parties already known and evidenced as pre-existing relationships before introduction through the platform, provided such evidence is recorded in the AITA Platform within ten (10) Business Days of adding the relevant Project/party.

**11. Injunctive Relief and Specific Performance**

**11.1 **The Parties acknowledge that breaches of Sections 10 (Non-Circumvention) and 20 (Confidentiality) may cause irreparable harm for which damages may be inadequate.

**11.2 **Accordingly, in addition to any other remedies, the non-breaching Party shall be entitled to seek and obtain injunctive relief, specific performance, and any other equitable relief from any court of competent jurisdiction (including the courts of England and Wales) without the requirement to prove special damage.

**11.3 **The Parties agree that the court may order expedited relief where necessary to prevent ongoing or threatened breaches, and that the Evidence Ledger may be used to support such applications.

**12. Termination and Project Continuity**

**12.1 **Either Party may terminate this Agreement on written notice if the other Party commits a material breach and fails to remedy within 15 Business Days of notice.

**12.2 **AITA may remove a Project from execution immediately if CC fails to meet Reality Gates or milestones for that Project as defined in this Agreement or the Digital Annex.

**12.3 **Termination does not affect rights accrued for Projects already financed/closed, and existing Digital Annex obligations survive insofar as required to unwind properly and respect confidentiality and non-circumvention.

**12.4 **For Projects in active closing at the time of termination, the Parties shall cooperate in good faith to avoid value destruction, consistent with investor/bank requirements.

**13. Representations and Disclaimers**

**13.1 **Each Party represents it has full power and authority to enter into this Agreement.

**13.2 **Forecasts, predictions, scenario outputs, and analytics generated through the AITA Platform are decision-support tools, not guarantees.

**13.3 **Nothing in this Agreement constitutes regulated financial advice by AITA. CC is responsible for ensuring compliance with any applicable financial promotion / placement / regulatory obligations in the UK and any other relevant jurisdictions, as specified per Project in the Digital Annex.

**14. Governing Law and Jurisdiction**

**14.1 **This Agreement and any dispute or claim arising out of or in connection with it shall be governed by the laws of England and Wales.

**14.2 **The courts of England and Wales shall have exclusive jurisdiction, except that either Party may seek injunctive relief for breaches of confidentiality or non-circumvention in any competent court.

**PART II**

**INTERNAL --- Operational Framework & Platform Governance**

**15. AITA Platform as Single Source of Truth**

**15.1 **The Parties agree the AITA Platform is the exclusive operational environment and single source of truth for execution, reporting, forecasting, audit evidence, contact management, milestones, approvals, and governance.

**15.2 **Platform logs, timestamps, approvals, access records, task histories and document registers constitute an Evidence Ledger usable for governance and dispute resolution.

**16. Digital Annexes**

**16.1 **Each Project is governed by a Digital Annex inside the AITA Platform, which is incorporated by reference into this Agreement and is legally binding once approved by authorised representatives of both Parties within the platform.

**16.2 **Digital Annexes may include: scope, roles, milestones, financing parameters, Cost of Funds statement, tender rules, verification gates, portfolio formation rules, cash waterfall, reporting cadence, and authorised signatories.

**16.3 **In the event of conflict: (a) this Agreement prevails for legal framework and core principles; (b) the relevant Digital Annex prevails for Project-specific commercial and operational terms; (c) platform policies referenced in a Digital Annex apply where consistent with (a) and (b).

**17. AITA Obligations (Operational)**

AITA shall:

**17.1 **Provide and maintain in the AITA Platform evidence of Disposition Rights for each Project.

**17.2 **Deliver an Internal Audit Pack, including baseline models, assumptions, risk register, and the first-stage calculations required for financeability.

**17.3 **Operate the platform workflow as the execution backbone: verification steps, stakeholder roles, audit trail, and project governance.

**17.4 **Run and document competitive tendering in accordance with Section 19.

**17.5 **Support contract negotiation and closing for the B2B Package and overall deal optimisation.

**17.6 **Provide CC with controlled access to Projects and relevant data within the AITA Platform under role-based permissions.

**18. Climate Capital Obligations (Operational)**

CC shall:

**18.1 **Arrange financing for Projects at the lowest feasible Cost of Funds consistent with bankability and the agreed timeline.

**18.2 **Provide Proof of Funds prior to Project \"Open for Fundraising Execution\" status as defined in the Digital Annex.

**18.3 **Lead the financing process (term sheets, negotiations, coordination with investors/lenders), and upload/link the full financing documentation to the AITA Platform.

**18.4 **Disclose all fees, commissions, and third-party payments included in Cost of Funds, and provide supporting documentation upon reasonable request.

**18.5 **Act in good faith and not misrepresent capital availability, commitments, or conditions.

**19. Competitive Tendering**

**19.1 **Unless waived in writing via the AITA Platform for a specific Project, AITA shall run a competitive tender for EPC (and, where relevant, key suppliers) with no fewer than three (3) bona fide bids.

**19.2 **Tender rules, evaluation matrix, bid comparisons, and selection rationale shall be recorded in the AITA Platform as part of the Evidence Ledger.

**19.3 **CC may propose contractors, but final selection must follow the tender procedure unless waived.

**19.4 **Any deviation from the tender procedure must be explicitly approved in the Digital Annex and justified (e.g., emergency, unique technology, bank requirement).

**20. Confidentiality and Data Controls**

**20.1 **Each Party shall keep confidential all non-public information received from the other Party, including all content within the AITA Platform (data, contacts, audit packs, models, term sheets, negotiations, forecasts, and logs) (\"Confidential Information\").

**20.2 **Confidential Information may be used solely for the purposes of this Agreement and only disclosed to representatives who need to know and are bound by confidentiality obligations at least as strict as this Section.

**20.3 **Confidentiality survives for five (5) years after termination, and indefinitely for trade secrets.

**20.4 **Each Party shall implement reasonable security controls and comply with applicable data protection laws (including UK GDPR where applicable).

**20.5 **No public announcement or marketing reference to the other Party or the Projects shall be made without prior written approval, except where required by law or investor disclosure rules, in which case prior notice shall be given where legally permitted.

**21. IP and Platform Rights**

**21.1 **The AITA Platform, workflows, templates, data structures, and software are and remain AITA\'s intellectual property.

**21.2 **CC receives a limited, non-transferable, revocable licence to access the AITA Platform solely for executing this Agreement, subject to role-based permissions and compliance with platform policies.

**21.3 **Each Party retains ownership of its pre-existing IP. Any jointly developed templates or methodologies shall be treated as jointly owned only if explicitly stated in a Digital Annex.

**22. Notices**

**22.1 **Formal notices under this Agreement shall be delivered through: (a) the AITA Platform notice function (where available) and additionally by email to the addresses recorded in the AITA Platform; or (b) as otherwise specified in a Digital Annex.

**22.2 **Notices are deemed received when acknowledged in the platform or, if by email, on the next Business Day after sending (provided no bounce-back is received).

**23. Miscellaneous**

**23.1 **This Agreement constitutes the entire agreement between the Parties on its subject matter and supersedes prior discussions.

**23.2 **Amendments must be made either: (a) in writing signed by both Parties; or (b) via Digital Annex approval inside the AITA Platform where explicitly permitted by Section 16 and the relevant Annex.

**23.3 **Neither Party may assign this Agreement without the other Party\'s written consent, except to an affiliate controlling or controlled by that Party, provided the assigning Party remains liable.

**23.4 **If any provision is held invalid, the remaining provisions continue in full force.

**SIGNATURES**

+-------------------------------------------------------------------+-------------------------------------------------------------------+
| **For and on behalf of AITA World S.L.**                          | **For and on behalf of Climate Capital \[●\]**                    |
|                                                                   |                                                                   |
| Name: \[●\]                                                       | Name: \[●\]                                                       |
|                                                                   |                                                                   |
| Title: \[●\]                                                      | Title: \[●\]                                                      |
|                                                                   |                                                                   |
| Signature: ___________________________ | Signature: ___________________________ |
|                                                                   |                                                                   |
| Date: \[●\]                                                       | Date: \[●\]                                                       |
+-------------------------------------------------------------------+-------------------------------------------------------------------+

**ANNEX A --- Digital Annex (Project Schedule) Template**

Each Project added under this Agreement shall have a Digital Annex including, at minimum:

> **1.** Project name / ID / jurisdiction
>
> **2.** Disposition Rights evidence checklist
>
> **3.** Audit pack status and verification gate status
>
> **4.** Tender rules (3 bids minimum) and evaluation matrix
>
> **5.** Financing target (equity %, debt %, instruments)
>
> **6.** Proof of Funds requirement and deadline
>
> **7.** B2B Package checklist and timeline
>
> **8.** Cost of Funds statement format
>
> **9.** Portfolio waterfall parameters (if applicable)
>
> **10.** Upside Spread calculation basis and distribution mechanics
>
> **11.** Authorised Users and approval rights
>
> **12.** Reporting cadence and dashboards


---

# ═══ PROFILE 1 — DEVELOPER: Cooperation Agreement (EN) ═══

**COOPERATION AGREEMENT FOR PROJECT LISTING,**

**EXCLUSIVITY AND INVESTMENT SOURCING**

***v1.0***

This Cooperation Agreement (\"Agreement\") is entered into as of _____________ (the \"Effective Date\"), between:

+-------------------------------+-------------------------------------------------------------------------------------+
| **AITA WORLD, S.L.**          | **DEVELOPER**                                                                       |
|                               |                                                                                     |
| CIF: B75859744                | [Legal Name:                                                   ]        |
|                               |                                                                                     |
| Address: Sabino Arana, 8-2    | [Country:                                                             ] |
|                               |                                                                                     |
| 48013 Bilbao, Bizkaia, España | [Legal Form:                                                        ]   |
|                               |                                                                                     |
| Email: d.mekhed\@aita.world   | [Contact Email:                                                   ]     |
+-------------------------------+-------------------------------------------------------------------------------------+

**(collectively, the \"Parties\")**

**1. Purpose and Scope**

**1.1 **AITA provides a digital platform (\"Platform\") to facilitate the sourcing, listing, verification, and investment matching of renewable energy and infrastructure projects. The Developer seeks to list, verify, and market projects on the Platform to attract investors, strategic partners, and financing.

**1.2 **This Agreement establishes the terms under which Developer may list Projects, access Platform features, benefit from AITA\'s investor network and marketing services, and compensate AITA through success-based fees upon successful transaction closure.

**2. Definitions**

**2.1 **Project: Any renewable energy, infrastructure, technology, or related commercial development initiative that Developer seeks to list on the Platform for investment, partnership, or financing.

**2.2 **Platform: AITA\'s proprietary web-based and mobile application ecosystem for project sourcing, listing, investor matching, and deal management.

**2.3 **Confidential Information: All non-public, technical, financial, legal, or strategic information relating to Projects, Parties\' business operations, and proprietary methodologies.

**2.4 **LOI: Letter of Intent expressing mutual interest in a specific transaction, executed between AITA, Developer, and an Investor.

**2.5 **Successful Closing: Completion of a binding transaction---including equity investment, debt financing, M&A, PPP, or other material economic arrangement---where AITA\'s introduction or sourcing directly contributed to deal closure.

**3. Roles and Responsibilities**

**3.1 **AITA shall: (a) maintain and enhance the Platform; (b) source, vet, and present potential Investors to Developer; (c) provide listing, marketing, and matchmaking services; (d) facilitate due diligence workflows; (e) support deal negotiation and closure; (f) invoice and collect success fees upon Successful Closing.

**3.2 **Developer shall: (a) provide accurate, complete project data; (b) promptly respond to investor inquiries; (c) maintain confidentiality per §9; (d) pay AITA success fees on agreed timeline (§8.6); (e) designate a primary contact; (f) not circumvent AITA during exclusivity window (§7.4).

**4. Listing, Verification and Access Levels**

**4.1 **Upon signup, Developer may submit Projects for listing under one of five access levels (Annex 1, Part D): Draft \| Verified \| Published \| Restricted \| Archived. AITA reserves the right to review and verify project data before advancement to Published or Restricted status.

**4.2 **Verification includes automated completeness checks (legal, financial, technical documentation) and manual review to ensure material accuracy and Platform compliance.

**5. Free Listing Limit and Commercial Functionality**

**5.1 **Developer may list up to two (2) Projects under Free Listing tier (Annex 1, Part A). Free Listing includes basic project card, document upload (up to 10 documents), automated completeness check, and publication to limited investor pool, with no investor advertising or advanced analytics.

**5.2 **From the 3rd Project onwards, Developer must select a Commercial Package (Annex 1, Part B): Listing Plus, Active, or Full Service. Commercial Packages include enhanced functionality, investor advertising, deal tracking, and account support.

**6. Investor Advertising and Lead Generation (Optional)**

**6.1 **AITA may, at Developer\'s election and per applicable Commercial Package (Annex 1, Part B), run targeted advertising campaigns within its investor network, roadshows, and curated lead generation services.

**6.2 **Lead generation shall cover qualified investor prospects identified per the Project stage (Development vs CapEx, Annex 1, Part C). AITA shall provide monthly reporting on investor engagement metrics.

**7. Exclusivity Triggered at LOI**

**7.1 **Exclusivity is not triggered at signup or listing. Instead, Exclusivity begins upon execution of a Letter of Intent (LOI) between AITA, Developer, and a prospective Investor (Annex 5).

**7.2 **Once an LOI is signed, Developer grants AITA exclusive rights to source, structure, and negotiate that specific Project transaction with the identified Investor(s) referenced in the LOI.

**7.3 **The Exclusivity period runs for one hundred twenty (120) calendar days from the LOI Effective Date.

**7.4 **During the Exclusivity period, Developer shall not (a) negotiate or finalize any competing offer for the same Project with other investors; (b) propose materially better economic terms off-Platform; (c) use AITA materials, data, or investor introductions to complete an off-Platform transaction; (d) engage third-party intermediaries to circumvent the LOI.

**7.5 **AITA shall exercise good faith efforts to advance the transaction. If a Successful Closing is achieved within or after the Exclusivity period, AITA success fees apply per §8.

**8. AITA Success Fees (Stage-Based)**

**8.1 **Developer\'s fee obligation is contingent on Successful Closing. AITA does not charge fees for listings, listings without deal closure, or investor introductions that do not result in binding transaction documents.

**8.2 **Fee Structure by Transaction Stage (per Annex 1, Part C):

**8.2.1 **Development Stage (permits, pre-FID, rights packages): 5% of total transaction value (equity + debt raised, or monetized rights).

**8.2.2 **CapEx / Investment Stage (RTB, FID-ready, EPC/financing): 2.7% of total transaction value.

**8.3 **Transaction value is calculated as follows: (a) for equity investment or capital raise, the total amount funded; (b) for debt financing, the principal amount; (c) for M&A or asset sale, the purchase price; (d) for PPP or hybrid structures, the net present value of payments/equity equivalent.

**8.4 **AITA shall issue an invoice upon Successful Closing with supporting transaction documentation. Developer and Investor (or financing counterparty) must mutually confirm the transaction amount to be reported to AITA.

**8.5 **Disputes over transaction valuation or fee calculation must be raised within thirty (30) days of invoice. AITA and Developer shall attempt good faith resolution; if unresolved, dispute resolution per §16 shall apply.

**8.6 **Payment of success fees shall be made within ten (10) business days of invoice receipt.

**9. Non-Circumvention, Confidentiality, Platform Non-Competition**

**9.1 **Non-Circumvention: During the term of this Agreement and for twelve (12) months thereafter, Developer shall not, directly or indirectly, (a) solicit, contact, negotiate, or transact with any Investor introduced or sourced by AITA for the same or substantially similar Project, outside the Platform or AITA\'s involvement; (b) use AITA\'s proprietary data, investor lists, or methodology to complete transactions with Investors other than those formally introduced by AITA; (c) disclose AITA\'s Confidential Information to competitors or third parties to circumvent AITA\'s role.

**9.2 **Confidentiality: Each Party shall maintain strict confidentiality of the other Party\'s Confidential Information and shall not disclose it to third parties except (a) to advisors, legal counsel, and accountants on a need-to-know basis (under written NDA); (b) as required by law or court order (with prior notice to the disclosing Party, except where legally prohibited); (c) to Investors or financing partners directly involved in transaction negotiations, under confidentiality obligations.

**9.3 **Platform Non-Competition: Developer shall not, during the term of this Agreement, launch, invest in, or promote a competing investor-matching or project-listing platform in renewable energy or infrastructure, nor shall it encourage Investors to use competing platforms in lieu of AITA\'s services.

**10. Optional: Complete/Upgrade the Project for Equity or Value Share**

**10.1 **At AITA\'s discretion, AITA may propose to co-invest, complete, or upgrade a Project in exchange for an equity stake, management rights, or revenue share, rather than a one-time success fee.

**10.2 **Such arrangements shall be negotiated separately from this Agreement and documented in a side letter or amendment, specifying AITA\'s equity percentage, governance rights, exit terms, and any continuing operational roles.

**11. External Contracting and Representation**

**11.1 **Developer remains solely responsible for engagement with EPC contractors, technology suppliers, financial advisors, and other third parties. AITA does not guarantee supplier performance or vouch for third-party quality unless explicitly stated in writing.

**11.2 **Developer authorizes AITA to represent Developer\'s Project in marketing materials, investor pitches, and Platform listings, using Project data, photos, and financial summaries provided by Developer (or with Developer\'s approval).

**12. Publicity and Marketing Rights**

**12.1 **Developer grants AITA a non-exclusive, royalty-free license to use Project name, description, renderings, and non-sensitive metrics in AITA marketing, investor roadshows, case studies, and press releases (unless Developer opts out in writing).

**12.2 **AITA shall respect Developer\'s confidentiality requirements and shall not disclose Project technical details, financial models, or investor negotiations without Developer\'s written consent.

**13. Warranties and Compliance**

**13.1 **Each Party warrants that: (a) it has full authority to enter into this Agreement; (b) it will comply with all applicable laws (environmental, labor, anti-corruption, data protection, sanctions, etc.); (c) Project information provided is accurate and complete to the best of its knowledge; (d) it is not subject to trade sanctions or export restrictions.

**13.2 **Developer warrants that all Project data, documents, and representations are original, non-infringing, and legally permitted for AITA\'s use per §12.

**13.3 **AITA makes no warranty regarding Investor creditworthiness, transaction outcomes, or the suitability of any Investor for Developer\'s Project.

**14. Limitation of Liability**

**14.1 **NEITHER PARTY SHALL BE LIABLE FOR INDIRECT, INCIDENTAL, CONSEQUENTIAL, SPECIAL, OR PUNITIVE DAMAGES, INCLUDING LOST PROFITS OR LOST REVENUE, EVEN IF ADVISED OF THE POSSIBILITY OF SUCH DAMAGES.

**14.2 **EXCEPT FOR BREACHES OF CONFIDENTIALITY (§9), IP INFRINGEMENT, OR PAYMENT OBLIGATIONS, THE TOTAL LIABILITY OF EITHER PARTY FOR ANY CLAIM ARISING UNDER THIS AGREEMENT SHALL NOT EXCEED THE GREATER OF (A) TOTAL FEES PAID BY DEVELOPER IN THE 12 MONTHS PRECEDING THE CLAIM, OR (B) USD 50,000.

**15. Term and Termination**

**15.1 **Term: This Agreement is effective as of the Effective Date and shall continue for a period of three (3) years, unless earlier terminated.

**15.2 **Termination for Convenience: Either Party may terminate this Agreement upon ninety (90) days\' written notice, except that any active LOI or ongoing Exclusivity period shall survive termination and continue to bind Developer per §7.

**15.3 **Termination for Cause: Either Party may terminate immediately if the other Party materially breaches this Agreement and fails to cure within thirty (30) days of written notice.

**15.4 **Effect of Termination: Upon termination, (a) Developer may no longer list new Projects; (b) existing Projects shall be archived; (c) obligations re: Confidentiality (§9), Non-Circumvention (§9), and payment of accrued fees (§8) shall survive; (d) AITA retains the right to collect success fees on Successful Closings of Projects listed during the term, even if closure occurs post-termination.

**16. Governing Law and Dispute Resolution**

**16.1 **This Agreement shall be governed by and construed in accordance with the laws of the Kingdom of Spain, without regard to its conflicts-of-law provisions.

**16.2 **Dispute Resolution: Any dispute or disagreement arising out of or relating to this Agreement or its breach shall be resolved by binding arbitration under the Rules of the Corte de Arbitraje de Madrid (CAM). The arbitration shall be seated in Madrid, Spain, and conducted in English.

**16.3 **The arbitral tribunal shall consist of a single arbitrator (for claims \< EUR 100,000) or three arbitrators (for claims \>= EUR 100,000), to be appointed per CAM Rules.

**17. Force Majeure**

**17.1 **Neither Party shall be liable for any failure or delay in performance under this Agreement to the extent caused by events beyond its reasonable control, including acts of God, war, terrorism, pandemics, government actions, natural disasters, or major infrastructure failures (\"Force Majeure Event\").

**17.2 **Upon occurrence of a Force Majeure Event, the affected Party shall notify the other Party in writing as soon as practicable. If the Force Majeure Event continues for more than ninety (90) days, either Party may terminate this Agreement.

**17.3 **Force Majeure shall not excuse payment of amounts already due or circumvent confidentiality obligations.

**18. Language and Controlling Version**

**18.1 **This Agreement is executed in English. Any translations into other languages are for convenience only. In the event of any conflict between the English version and any translation, the English version shall prevail.

**19. Personal Data Protection**

**19.1 **Each Party shall comply with applicable data protection laws, including the General Data Protection Regulation (GDPR) and Spain\'s Organic Law 3/2018 (LOPDGDD), when processing personal data of the other Party\'s employees, representatives, or contacts.

**19.2 **AITA shall use Developer contact information solely for performance of this Agreement and shall not sell, share, or use such data for unrelated marketing without consent.

**20. Notices**

**20.1 **All notices under this Agreement shall be in writing and shall be deemed given when delivered personally, sent by registered email, or by courier to the addresses below:

**For AITA World, S.L.:**

Sabino Arana, 8-2, 48013 Bilbao, Bizkaia, España

Email: d.mekhed\@aita.world

**For Developer:**

Email:                                                             

**21. Annexes**

**21.1 **The following Annexes are integral parts of this Agreement:

-   Annex 1: Packages and Stage Qualification Criteria

-   Annex 2: Developer Onboarding Checklist

-   Annex 3: Invoice and Payment Terms Template

-   Annex 4: Commercial Package Order Form

-   Annex 5: Letter of Intent and Exclusivity Agreement

**22. Signature Block**

**IN WITNESS WHEREOF, the Parties have executed this Agreement as of the date first written above.**

+--------------------------------------------------------------------------+--------------------------------------------------------------------------+
| **AITA WORLD, S.L.**                                                     | **DEVELOPER**                                                            |
|                                                                          |                                                                          |
| By: _________________________________   | By: _________________________________   |
|                                                                          |                                                                          |
| Name: Dmytro Mekhed                                                      | Name:                                                                    |
|                                                                          |                                                                          |
| Title: Director                                                          | Title:                                                                   |
|                                                                          |                                                                          |
| Date: _________________________________ | Date: _________________________________ |
+--------------------------------------------------------------------------+--------------------------------------------------------------------------+


---

# ═══ PROFILE 1 — DEVELOPER: Договір співпраці (UA) ═══

**ДОГОВІР ПРО СПІВПРАЦЮ ЩОДО РОЗМІЩЕННЯ ПРОЕКТІВ,**

**ЕКСКЛЮЗИВНОСТІ ТА ЗАЛУЧЕННЯ ІНВЕСТИЦІЙ**

***v1.0***

Цей Договір про співпрацю («Договір») укладено станом на _____________ («Дата набрання чинності») між:

+--------------------------------+--------------------------------------------------------------------------------------+
| **AITA WORLD, S.L.**           | **РОЗРОБНИК**                                                                        |
|                                |                                                                                      |
| КІФ: B75859744                 | [Юридична назва:                                           ]             |
|                                |                                                                                      |
| Адреса: Sabino Arana, 8-2      | [Країна:                                                               ] |
|                                |                                                                                      |
| 48013 Bilbao, Bizkaia, Іспанія | [Правова форма:                                                 ]        |
|                                |                                                                                      |
| Email: d.mekhed\@aita.world    | [Контактний Email:                                             ]         |
+--------------------------------+--------------------------------------------------------------------------------------+

**(разом --- «Сторони»)**

**1. Предмет і сфера застосування**

**1.1 **AITA надає цифрову платформу («Платформа») для полегшення пошуку, розміщення, верифікації та інвестиційного підбору проектів у сфері відновлюваної енергетики та інфраструктури. Розробник прагне розміщувати, верифікувати та просувати проекти на Платформі з метою залучення інвесторів, стратегічних партнерів і фінансування.

**1.2 **Цей Договір встановлює умови, на яких Розробник може розміщувати Проекти, користуватися функціями Платформи, отримувати переваги від інвесторської мережі та маркетингових послуг AITA, а також сплачувати AITA комісію за успішне закриття угод.

**2. Визначення**

**2.1 **Проект: будь-яка ініціатива у сфері відновлюваної енергетики, інфраструктури, технологій або суміжного комерційного розвитку, яку Розробник прагне розмістити на Платформі з метою інвестування, партнерства або фінансування.

**2.2 **Платформа: власна веб- та мобільна екосистема AITA для пошуку проектів, їхнього розміщення, підбору інвесторів та управління угодами.

**2.3 **Конфіденційна інформація: будь-яка непублічна технічна, фінансова, юридична або стратегічна інформація, що стосується Проектів, ділової діяльності Сторін та пропрієтарних методологій.

**2.4 **ЛНН: Лист про наміри, що виражає взаємний інтерес до конкретної операції та підписується між AITA, Розробником та Інвестором.

**2.5 **Успішне закриття: завершення юридично обов\'язкової операції --- включаючи акціонерне інвестування, боргове фінансування, M&A, ДПП або іншу суттєву економічну угоду, --- де залучення або пошук AITA безпосередньо сприяли закриттю угоди.

**3. Ролі та обов\'язки**

**3.1 **AITA зобов\'язується: (а) підтримувати та вдосконалювати Платформу; (б) шукати, перевіряти та представляти потенційних Інвесторів Розробнику; (в) надавати послуги з розміщення, маркетингу та підбору партнерів; (г) супроводжувати процеси due diligence; (д) підтримувати переговори та закриття угод; (е) виставляти рахунки та стягувати комісію за успішне закриття.

**3.2 **Розробник зобов\'язується: (а) надавати точні та повні дані про проект; (б) оперативно відповідати на запити інвесторів; (в) дотримуватися конфіденційності згідно з §9; (г) сплачувати AITA комісію за успішне закриття у погоджені строки (§8.6); (д) призначити основного контактного представника; (е) не обходити AITA протягом ексклюзивного вікна (§7.4).

**4. Розміщення, верифікація та рівні доступу**

**4.1 **Після реєстрації Розробник може подавати Проекти для розміщення на одному з п\'яти рівнів доступу (Додаток 1, Частина D): Чернетка \| Верифіковано \| Опубліковано \| Обмежено \| Архівовано. AITA залишає за собою право перевіряти дані проекту перед переходом до статусу «Опубліковано» або «Обмежено».

**4.2 **Верифікація включає автоматизовані перевірки повноти документів (юридичних, фінансових, технічних) та ручний огляд для забезпечення суттєвої точності та відповідності вимогам Платформи.

**5. Безкоштовне розміщення та комерційний функціонал**

**5.1 **Розробник може розмістити до двох (2) Проектів у рамках тарифу «Безкоштовне розміщення» (Додаток 1, Частина A). Безкоштовне розміщення включає базову картку проекту, завантаження документів (до 10 документів), автоматизовану перевірку повноти та публікацію для обмеженого кола інвесторів, без реклами для інвесторів і розширеної аналітики.

**5.2 **Починаючи з 3-го Проекту, Розробник повинен обрати Комерційний пакет (Додаток 1, Частина B): Listing Plus, Active або Full Service. Комерційні пакети включають розширений функціонал, рекламу для інвесторів, відстеження угод та підтримку акаунт-менеджера.

**6. Реклама для інвесторів та лідогенерація (опціонально)**

**6.1 **AITA може, за вибором Розробника та відповідно до застосовного Комерційного пакету (Додаток 1, Частина B), проводити цільові рекламні кампанії у своїй інвесторській мережі, роадшоу та послуги курованої лідогенерації.

**6.2 **Лідогенерація охоплюватиме кваліфікованих потенційних інвесторів, визначених відповідно до стадії Проекту (Розробка vs CapEx, Додаток 1, Частина C). AITA надаватиме щомісячну звітність про показники залученості інвесторів.

**7. Ексклюзивність, що починається з підписання ЛНН**

**7.1 **Ексклюзивність не починається з моменту реєстрації або розміщення. Ексклюзивність починається після підписання Листа про наміри (ЛНН) між AITA, Розробником та потенційним Інвестором (Додаток 5).

**7.2 **Після підписання ЛНН Розробник надає AITA ексклюзивне право щодо пошуку, структурування та переговорів по конкретній угоді з ідентифікованим(и) Інвестором(ами), зазначеними в ЛНН.

**7.3 **Ексклюзивний період тривалістю сто двадцять (120) календарних днів починається з Дати набрання чинності ЛНН.

**7.4 **Протягом ексклюзивного періоду Розробник не має права: (а) вести переговори або укладати конкуруючі пропозиції щодо того ж Проекту з іншими інвесторами; (б) пропонувати суттєво кращі економічні умови поза межами Платформи; (в) використовувати матеріали, дані AITA або представлення інвесторів для завершення позаплатформних угод; (г) залучати сторонніх посередників для обходу ЛНН.

**7.5 **AITA докладатиме добросовісних зусиль для просування угоди. У разі Успішного закриття в межах або після ексклюзивного періоду комісія AITA застосовується згідно з §8.

**8. Комісія AITA за успішне закриття (поетапна)**

**8.1 **Зобов\'язання Розробника зі сплати комісії залежить від Успішного закриття. AITA не стягує комісії за розміщення, розміщення без закриття угоди або за представлення інвесторів, які не призвели до підписання обов\'язкових документів по угоді.

**8.2 **Структура комісії за стадіями угоди (відповідно до Додатку 1, Частина C):

**8.2.1 **Стадія розробки (дозволи, до FID, пакети прав): 5% від загальної вартості угоди (залучений капітал + борг або монетизовані права).

**8.2.2 **Стадія CapEx / Інвестування (RTB, готовий до FID, EPC/фінансування): 2,7% від загальної вартості угоди.

**8.3 **Вартість угоди розраховується наступним чином: (а) для акціонерних інвестицій або залучення капіталу --- загальна профінансована сума; (б) для боргового фінансування --- сума основного боргу; (в) для M&A або продажу активів --- ціна придбання; (г) для ДПП або гібридних структур --- чиста приведена вартість платежів/еквівалент акціонерного капіталу.

**8.4 **AITA виставляє рахунок-фактуру після Успішного закриття з підтверджуючою документацією по угоді. Розробник та Інвестор (або фінансуючий контрагент) повинні взаємно підтвердити суму угоди, що підлягає звітуванню до AITA.

**8.5 **Суперечки щодо оцінки угоди або розрахунку комісії повинні бути порушені протягом тридцяти (30) днів з моменту виставлення рахунку. AITA та Розробник прагнуть до врегулювання шляхом добросовісних переговорів; у разі невирішення --- вирішення спорів згідно з §16.

**8.6 **Сплата комісії за успішне закриття здійснюється протягом десяти (10) робочих днів після отримання рахунку-фактури.

**9. Незалучення третіх сторін, конфіденційність, некомпетиція на Платформі**

**9.1 **Незалучення третіх сторін: Протягом строку дії цього Договору та дванадцять (12) місяців після його закінчення Розробник не має права прямо або непрямо: (а) залучати, зв\'язуватися, вести переговори або укладати угоди з будь-яким Інвестором, представленим або залученим AITA щодо того ж або аналогічного Проекту поза Платформою або без участі AITA; (б) використовувати пропрієтарні дані, списки інвесторів або методологію AITA для завершення угод з Інвесторами, крім тих, що офіційно представлені AITA; (в) розкривати Конфіденційну інформацію AITA конкурентам або третім особам з метою обходу ролі AITA.

**9.2 **Конфіденційність: Кожна Сторона зобов\'язана зберігати суворої конфіденційності Конфіденційну інформацію іншої Сторони та не розкривати її третім особам, за винятком: (а) консультантів, юридичних радників та бухгалтерів на умовах необхідності знати (під письмовим NDA); (б) якщо цього вимагає закон або постанова суду (з попереднім повідомленням Сторони, що розкриває інформацію, крім випадків, коли це заборонено законом); (в) Інвесторів або фінансуючих партнерів, безпосередньо залучених до переговорів по угоді, на умовах конфіденційності.

**9.3 **Некомпетиція на Платформі: Протягом строку дії цього Договору Розробник не має права запускати, інвестувати або просувати конкуруючу платформу для підбору інвесторів або розміщення проектів у сфері відновлюваної енергетики або інфраструктури, а також заохочувати Інвесторів до використання конкуруючих платформ замість послуг AITA.

**10. Опціонально: завершення/вдосконалення Проекту в обмін на частку або частковий дохід**

**10.1 **На розсуд AITA, AITA може запропонувати спільне інвестування, завершення або вдосконалення Проекту в обмін на частку у власному капіталі, права управління або частку доходу замість одноразової комісії за успішне закриття.

**10.2 **Такі домовленості узгоджуються окремо від цього Договору і документуються в додатковому листі або поправці, в яких зазначаються відсоток участі AITA у капіталі, права управління, умови виходу та будь-які поточні операційні ролі.

**11. Зовнішні контракти та представництво**

**11.1 **Розробник несе виключну відповідальність за взаємодію з EPC-підрядниками, постачальниками технологій, фінансовими консультантами та іншими третіми особами. AITA не гарантує якість роботи постачальників і не ручається за третіх осіб, якщо інше прямо не зазначено в письмовій формі.

**11.2 **Розробник уповноважує AITA представляти Проект Розробника у маркетингових матеріалах, презентаціях для інвесторів та розміщеннях на Платформі, використовуючи дані, фотографії та фінансові показники Проекту, надані Розробником (або з його схвалення).

**12. Права на публічність та маркетинг**

**12.1 **Розробник надає AITA невиключну безоплатну ліцензію на використання назви, опису, візуалізацій та несуттєвих показників Проекту у маркетингу AITA, роадшоу для інвесторів, кейс-стаді та прес-релізах (якщо Розробник не відмовився від цього в письмовій формі).

**12.2 **AITA поважатиме вимоги Розробника щодо конфіденційності та не розкриватиме технічні деталі Проекту, фінансові моделі або переговори з інвесторами без письмової згоди Розробника.

**13. Гарантії та відповідність**

**13.1 **Кожна Сторона гарантує, що: (а) має повні повноваження на укладення цього Договору; (б) дотримуватиметься всіх застосовних законів (екологічних, трудових, антикорупційних, захисту даних, санкцій тощо); (в) надана інформація про Проект є точною та повною за найкращими знаннями Сторони; (г) не підпадає під торговельні санкції або експортні обмеження.

**13.2 **Розробник гарантує, що всі дані, документи та заяви щодо Проекту є оригінальними, не порушують прав інтелектуальної власності третіх осіб і юридично дозволені для використання AITA згідно з §12.

**13.3 **AITA не надає жодних гарантій щодо кредитоспроможності Інвесторів, результатів угод або придатності будь-якого Інвестора для Проекту Розробника.

**14. Обмеження відповідальності**

**14.1 **ЖОДНА ЗІ СТОРІН НЕ НЕСЕ ВІДПОВІДАЛЬНОСТІ ЗА НЕПРЯМІ, ВИПАДКОВІ, НАСЛІДКОВІ, ОСОБЛИВІ АБО ШТРАФНІ ЗБИТКИ, ВКЛЮЧАЮЧИ УПУЩЕНУ ВИГОДУ АБО ВТРАЧЕНИЙ ДОХІД, НАВІТЬ ЯКЩО СТОРОНУ БУЛО ПОВІДОМЛЕНО ПРО МОЖЛИВІСТЬ ТАКИХ ЗБИТКІВ.

**14.2 **ЗА ВИНЯТКОМ ПОРУШЕНЬ КОНФІДЕНЦІЙНОСТІ (§9), ПОРУШЕНЬ ПРАВ ІНТЕЛЕКТУАЛЬНОЇ ВЛАСНОСТІ АБО ЗОБОВ\'ЯЗАНЬ ЩОДО ОПЛАТИ, ЗАГАЛЬНА ВІДПОВІДАЛЬНІСТЬ БУДЬ-ЯКОЇ ЗІ СТОРІН ЗА БУДЬ-ЯКОЮ ПРЕТЕНЗІЄЮ ВІДПОВІДНО ДО ЦЬОГО ДОГОВОРУ НЕ ПЕРЕВИЩУВАТИМЕ БІЛЬШЕ ЗА: (А) ЗАГАЛЬНИЙ РОЗМІР КОМІСІЙ, СПЛАЧЕНИХ РОЗРОБНИКОМ ЗА 12 МІСЯЦІВ, ЩО ПЕРЕДУЮТЬ ПРЕТЕНЗІЇ, АБО (Б) 50 000 ДОЛАРІВ США.

**15. Строк та припинення**

**15.1 **Строк: Цей Договір набирає чинності з Дати набрання чинності та діє протягом трьох (3) років, якщо не буде достроково розірваний.

**15.2 **Розірвання на власний розсуд: Будь-яка Сторона може розірвати цей Договір, надіславши дев\'яносто (90) днів письмового повідомлення, за умови що будь-який чинний ЛНН або поточний ексклюзивний період пережиє розірвання і продовжуватиме зобов\'язувати Розробника відповідно до §7.

**15.3 **Розірвання за порушенням: Будь-яка Сторона може негайно розірвати Договір, якщо інша Сторона суттєво порушила його умови та не виправила порушення протягом тридцяти (30) днів після письмового повідомлення.

**15.4 **Наслідки розірвання: Після розірвання: (а) Розробник більше не має права розміщувати нові Проекти; (б) існуючі Проекти архівуються; (в) зобов\'язання щодо конфіденційності (§9), незалучення третіх сторін (§9) та сплати нарахованих комісій (§8) залишаються чинними; (г) AITA зберігає право стягувати комісії за Успішне закриття Проектів, розміщених протягом строку дії Договору, навіть якщо закриття відбувається після його припинення.

**16. Застосовне право та вирішення спорів**

**16.1 **Цей Договір регулюється та тлумачиться відповідно до законодавства Королівства Іспанія, без урахування його колізійних норм.

**16.2 **Вирішення спорів: Будь-який спір або розбіжність, що виникає з цього Договору або пов\'язана з його порушенням, вирішується шляхом обов\'язкового арбітражу відповідно до Регламенту Мадридського арбітражного суду (CAM). Арбітраж проводиться в Мадриді, Іспанія, мовою провадження є іспанська або англійська.

**16.3 **Склад арбітражного трибуналу: один арбітр (для вимог \< 100 000 євро) або три арбітри (для вимог \>= 100 000 євро), що призначаються відповідно до Регламенту CAM.

**17. Форс-мажор**

**17.1 **Жодна зі Сторін не несе відповідальності за невиконання або затримку виконання зобов\'язань за цим Договором тією мірою, в якій це спричинено обставинами поза її розумним контролем, включаючи стихійні лиха, війну, тероризм, пандемії, дії уряду, природні катастрофи або серйозні збої в інфраструктурі («Форс-мажорна обставина»).

**17.2 **При виникненні Форс-мажорної обставини постраждала Сторона зобов\'язана якомога швидше повідомити іншу Сторону в письмовій формі. Якщо Форс-мажорна обставина тривалістю понад дев\'яносто (90) днів, будь-яка Сторона може розірвати цей Договір.

**17.3 **Форс-мажор не звільняє від оплати вже нарахованих сум або від виконання зобов\'язань щодо конфіденційності.

**18. Мова та визначальна версія**

**18.1 **Цей Договір складено англійською мовою. Будь-які переклади іншими мовами мають виключно ознайомчий характер. У разі будь-яких суперечностей між англійською версією та будь-яким перекладом превалює англійська версія.

**19. Захист персональних даних**

**19.1 **Кожна Сторона зобов\'язана дотримуватися застосовного законодавства про захист даних, включаючи Загальний регламент захисту даних (GDPR) та Органічний закон Іспанії 3/2018 (LOPDGDD), при обробці персональних даних працівників, представників або контактних осіб іншої Сторони.

**19.2 **AITA використовуватиме контактну інформацію Розробника виключно для виконання цього Договору та не продаватиме, не передаватиме та не використовуватиме такі дані для сторонньої маркетингової діяльності без згоди.

**20. Повідомлення**

**20.1 **Усі повідомлення за цим Договором надаються в письмовій формі та вважаються надісланими з моменту особистого вручення, відправлення рекомендованим електронним листом або кур\'єром на адреси, зазначені нижче:

**Для AITA World, S.L.:**

Sabino Arana, 8-2, 48013 Bilbao, Bizkaia, Іспанія

Email: d.mekhed\@aita.world

**Для Розробника:**

Email:                                                             

**21. Додатки**

**21.1 **Наступні Додатки є невід\'ємними частинами цього Договору:

-   Додаток 1: Пакети та критерії відбору за стадіями

-   Додаток 2: Контрольний список для онбордингу Розробника

-   Додаток 3: Шаблон рахунку-фактури та умов оплати

-   Додаток 4: Форма замовлення комерційного пакету

-   Додаток 5: Лист про наміри та угода про ексклюзивність

**22. Підписи**

**НА ПІДТВЕРДЖЕННЯ ЧОГО Сторони підписали цей Договір на дату, зазначену в преамбулі.**

+----------------------------------------------------------------------------+----------------------------------------------------------------------------+
| **AITA WORLD, S.L.**                                                       | **РОЗРОБНИК**                                                              |
|                                                                            |                                                                            |
| Підпис: ________________________________   | Підпис: ________________________________   |
|                                                                            |                                                                            |
| Ім\'я: Dmytro Mekhed                                                       | Ім\'я:                                                                     |
|                                                                            |                                                                            |
| Посада: Директор                                                           | Посада:                                                                    |
|                                                                            |                                                                            |
| Дата: __________________________________ | Дата: __________________________________ |
+----------------------------------------------------------------------------+----------------------------------------------------------------------------+


---

# ═══ PROFILE 1 — Annex 1: Packages & Criteria (EN) ═══

**ANNEX 1**

**Packages and Stage Qualification Criteria**

This Annex 1 specifies the Free Listing tier, three Commercial Packages, stage qualification criteria, and project access levels available under the Cooperation Agreement.

**A. Free Listing (up to 2 Projects)**

Developers may list up to two (2) Projects at no cost under the Free Listing tier. The table below outlines included features:

  ------------------------------------------------------------ --------------
  **Feature**                                                  **Included**
  Basic Project Card (name, location, type, capacity, stage)   ✓
  Document Upload (up to 10 documents)                         ✓
  Automated Completeness Check                                 ✓
  Publication under Basic Access Settings                      ✓
  Limited Investor Pool Visibility                             ✓
  Investor Advertising Campaigns                               ✗
  Advanced Analytics & Reporting                               ✗
  Strategy & Tracking Modules                                  ✗
  Basic Platform Workflow Only                                 ✓
  **Cost**                                                     **FREE**
  ------------------------------------------------------------ --------------

**B. Commercial Packages (from 3rd Project onwards)**

From the third (3rd) Project onwards, Developers must select a Commercial Package. Three tiers are available:

  ----------------------------------- ------------------------- ----------------------- -------------------------
  **Feature**                         **Tier 1 Listing Plus**   **Tier 2 Active**       **Tier 3 Full Service**
  Full Project Card                   ✓                         ✓                       ✓
  Extended Document Upload            ✓                         ✓                       ✓
  Completeness Scoring                ✓                         ✓                       ✓
  Standard Investor Pool Access       ✓                         ✓                       ✓
  Basic Analytics                     ✓                         ✓                       ✓
  Investor Advertising Campaigns      ✗                         ✓                       ✓
  Targeted Investor Introductions     ✗                         ✓                       ✓
  Roadshow Inclusion                  ✗                         ✓                       ✓
  Lead Tracking Module                ✗                         ✓                       ✓
  Advanced Reporting & Analytics      ✗                         ✓                       ✓
  Deal Tracking Module                ✗                         ✓                       ✓
  Strategy & Financial Model Review   ✗                         ✗                       ✓
  SPV Structuring Assistance          ✗                         ✗                       ✓
  Priority Matchmaking                ✗                         ✗                       ✓
  Dedicated Account Support           ✗                         ✗                       ✓
  **Fee**                             **Per Annex 4 Order**     **Per Annex 4 Order**   **Per Project SOW**
  ----------------------------------- ------------------------- ----------------------- -------------------------

Note: All Commercial Packages include success-based fees per Cooperation Agreement §8, in addition to any flat or subscription fees specified in Annex 4 Order Form.

**C. Stage Qualification Criteria (Development vs CapEx)**

Transaction stages are qualified based on project maturity indicators. Correct stage classification is essential for fee calculation (Development = 5%; CapEx = 2.7%).

  --------------------------------------------------------------------- ---------------------------------------------------------------------
  **Development Stage**                                                 **CapEx / Investment Stage**
  No Ready-to-Build (RTB) status yet                                    RTB status achieved (all permits, grid connection, land rights)
  Permits in progress or not yet applied                                FID (Final Investment Decision) taken or imminent
  Grid connection agreement not yet signed                              Grid connection agreement signed
  Pre-FID phase                                                         EPC contract ready or in tender stage
  Land rights not yet formalized                                        Land rights formally secured / long-term lease executed
  Main subject = development rights, permit package, early-stage work   Main subject = full capital investment for construction/acquisition
  Estimated timeline to RTB: 12+ months                                 Estimated timeline to operation: \< 12 months
  **AITA Fee: 5%**                                                      **AITA Fee: 2.7%**
  --------------------------------------------------------------------- ---------------------------------------------------------------------

Developers must declare the stage of each Project upon listing. AITA reserves the right to challenge the stage classification if material indicators are inconsistent with the declared stage. Any dispute shall be resolved per Cooperation Agreement §8.5.

**D. Project Access Levels**

All Projects have one of five access levels, controlling visibility, editing rights, and investor exposure:

  ------------ ---------------------------------------------------------------------------------------------------------------------------------------------------
  **Level**    **Description**
  Draft        Developer is editing; not yet submitted for verification. Visible only to Project owner.
  Verified     Developer submitted for review; AITA has verified core data (legal, financial, technical). Not yet public; AITA may request clarifications.
  Published    Full public listing; visible to all investors on the Platform. Actively marketed via AITA campaigns (if Commercial Package includes advertising).
  Restricted   Visible only to invited/qualified investors (e.g., due to sensitive location or off-market phase). Developer controls access list.
  Archived     Project closed, sold, or withdrawn. Not searchable; visible only to original stakeholders for historical reference.
  ------------ ---------------------------------------------------------------------------------------------------------------------------------------------------

**E. Summary and Next Steps**

Upon signing the Cooperation Agreement:

-   Developer selects Free Listing (max 2 Projects) or a Commercial Package (from 3rd Project).

-   For each Project, Developer declares the Transaction Stage (Development vs CapEx) and selects an initial Access Level (Draft, Verified, etc.).

-   AITA verifies Project data and approves advancement to Published or Restricted status.

-   Upon execution of an LOI for any Project, Exclusivity (§7 of Cooperation Agreement) and fee obligations (§8) commence.

-   Success fees are invoiced within 10 business days of Successful Closing.


---

# ═══ PROFILE 1 — Додаток 1: Пакети та Критерії (UA) ═══

**ДОДАТОК 1**

**Пакети та критерії відбору за стадіями**

Цей Додаток 1 визначає тариф «Безкоштовне розміщення», три Комерційних пакети, критерії відбору за стадіями та рівні доступу до проектів, доступні в рамках Договору про співпрацю.

**A. Безкоштовне розміщення (до 2 проектів)**

Розробники можуть безкоштовно розмістити до двох (2) Проектів у рамках тарифу «Безкоштовне розміщення». У таблиці нижче наведено включені функції:

  ---------------------------------------------------------------------------- -----------------
  **Функція**                                                                  **Включено**
  Базова картка проекту (назва, місце розташування, тип, потужність, стадія)   ✓
  Завантаження документів (до 10 документів)                                   ✓
  Автоматизована перевірка повноти                                             ✓
  Публікація за базовими налаштуваннями доступу                                ✓
  Обмежена видимість для пулу інвесторів                                       ✓
  Рекламні кампанії для інвесторів                                             ✗
  Розширена аналітика та звітність                                             ✗
  Модулі стратегії та відстеження                                              ✗
  Тільки базовий робочий процес Платформи                                      ✓
  **Вартість**                                                                 **БЕЗКОШТОВНО**
  ---------------------------------------------------------------------------- -----------------

**B. Комерційні пакети (починаючи з 3-го проекту)**

Починаючи з третього (3-го) Проекту, Розробники повинні обрати Комерційний пакет. Доступні три рівні:

  --------------------------------------- --------------------------- -------------------------- ---------------------------
  **Функція**                             **Рівень 1 Listing Plus**   **Рівень 2 Active**        **Рівень 3 Full Service**
  Повна картка проекту                    ✓                           ✓                          ✓
  Розширене завантаження документів       ✓                           ✓                          ✓
  Оцінка повноти документів               ✓                           ✓                          ✓
  Стандартний доступ до пулу інвесторів   ✓                           ✓                          ✓
  Базова аналітика                        ✓                           ✓                          ✓
  Рекламні кампанії для інвесторів        ✗                           ✓                          ✓
  Цільові знайомства з інвесторами        ✗                           ✓                          ✓
  Участь у роадшоу                        ✗                           ✓                          ✓
  Модуль відстеження лідів                ✗                           ✓                          ✓
  Розширена звітність та аналітика        ✗                           ✓                          ✓
  Модуль відстеження угод                 ✗                           ✓                          ✓
  Огляд стратегії та фінансової моделі    ✗                           ✗                          ✓
  Допомога у структуруванні SPV           ✗                           ✗                          ✓
  Пріоритетний підбір партнерів           ✗                           ✗                          ✓
  Виділений акаунт-менеджер               ✗                           ✗                          ✓
  **Вартість**                            **За Дод. 4 Замовлення**    **За Дод. 4 Замовлення**   **За ТЗ Проекту**
  --------------------------------------- --------------------------- -------------------------- ---------------------------

Примітка: Усі Комерційні пакети включають комісії за успішне закриття відповідно до Договору про співпрацю §8, на додаток до будь-яких фіксованих або підписних комісій, зазначених у Формі замовлення (Додаток 4).

**C. Критерії відбору за стадіями (Розробка vs CapEx)**

Стадії угоди класифікуються на основі показників зрілості проекту. Правильна класифікація стадії є суттєвою для розрахунку комісії (Розробка = 5%; CapEx = 2,7%).

  ------------------------------------------------------------------------------- ---------------------------------------------------------------------------
  **Стадія розробки**                                                             **Стадія CapEx / Інвестування**
  Статус «Готовий до будівництва» (RTB) ще не отримано                            Статус RTB досягнуто (усі дозволи, підключення до мережі, права на землю)
  Дозволи в процесі оформлення або ще не подано                                   Прийнято Остаточне інвестиційне рішення (FID) або воно невідкладне
  Угода про підключення до мережі ще не підписана                                 Угода про підключення до мережі підписана
  Фаза до FID                                                                     Контракт EPC готовий або на стадії тендеру
  Права на землю ще не оформлено                                                  Права на землю офіційно закріплені / довгострокова оренда укладена
  Основний предмет = права на розробку, пакет дозволів, роботи на ранній стадії   Основний предмет = повні капітальні інвестиції для будівництва/придбання
  Орієнтовний строк до RTB: більше 12 місяців                                     Орієнтовний строк до введення в експлуатацію: менше 12 місяців
  **Комісія AITA: 5%**                                                            **Комісія AITA: 2,7%**
  ------------------------------------------------------------------------------- ---------------------------------------------------------------------------

Розробники повинні оголосити стадію кожного Проекту при розміщенні. AITA залишає за собою право оскаржити класифікацію стадії, якщо суттєві показники не відповідають оголошеній стадії. Будь-який спір вирішується відповідно до §8.5 Договору про співпрацю.

**D. Рівні доступу до проектів**

Кожен Проект має один з п\'яти рівнів доступу, що контролює видимість, права на редагування та доступ інвесторів:

  -------------- -------------------------------------------------------------------------------------------------------------------------------------------------------
  **Рівень**     **Опис**
  Чернетка       Розробник вносить правки; ще не подано на верифікацію. Видно тільки власнику Проекту.
  Верифіковано   Розробник подав на розгляд; AITA верифікувала основні дані (юридичні, фінансові, технічні). Ще не публічно; AITA може запросити уточнення.
  Опубліковано   Повне публічне розміщення; видно всім інвесторам на Платформі. Активно просувається через кампанії AITA (якщо Комерційний пакет включає рекламу).
  Обмежено       Видно лише запрошеним/кваліфікованим інвесторам (наприклад, через чутливе місцезнаходження або позаринкову фазу). Розробник контролює список доступу.
  Архівовано     Проект закрито, продано або відкликано. Не доступний для пошуку; видно лише початковим стейкхолдерам для ознайомлення з історією.
  -------------- -------------------------------------------------------------------------------------------------------------------------------------------------------

**E. Підсумок та наступні кроки**

Після підписання Договору про співпрацю:

-   Розробник обирає «Безкоштовне розміщення» (макс. 2 Проекти) або Комерційний пакет (починаючи з 3-го Проекту).

-   Для кожного Проекту Розробник оголошує Стадію угоди (Розробка vs CapEx) та обирає початковий рівень доступу (Чернетка, Верифіковано тощо).

-   AITA верифікує дані Проекту та схвалює перехід до статусу «Опубліковано» або «Обмежено».

-   Після підписання ЛНН для будь-якого Проекту починається Ексклюзивність (§7 Договору про співпрацю) та зобов\'язання зі сплати комісії (§8).

-   Комісії за успішне закриття виставляються протягом 10 робочих днів після Успішного закриття.


---

# ═══ PROFILE 1 — Annex 2: Onboarding Checklist (EN) ═══

**ANNEX 2**

**Developer Onboarding Checklist**

*(Annex 2 to the Cooperation Agreement)*

This checklist defines the minimum information and document set required for Developer to complete onboarding on the AITA Platform. Completion of all \"Mandatory\" items is required to advance a Project from \"Draft\" to \"Verified\" status. \"Optional\" items are encouraged to maximise investor appeal and speed of deal execution.

**A. Corporate & Legal Identity**

  -------------------------------------------------- ------------ -----------------------------------------------------------
  **Item**                                           **Status**   **Notes**
  Certificate of Incorporation / Registration        Mandatory    Scanned copy, not older than 12 months
  Articles of Association / Bylaws                   Mandatory    Current version, with all amendments
  Excerpt from Commercial Register (or equivalent)   Mandatory    Issued within 6 months
  Tax Identification Number (TIN / VAT)              Mandatory    Applicable in jurisdiction of incorporation
  Proof of Registered Address                        Mandatory    Utility bill, bank letter, or official municipal document
  List of Beneficial Owners (UBOs ≥ 25%)             Mandatory    Required for AML/KYC compliance
  Organisational Chart / Group Structure             Optional     If part of a corporate group
  Powers of Attorney (if signatory ≠ director)       Mandatory    Notarised and apostilled where required
  -------------------------------------------------- ------------ -----------------------------------------------------------

**B. Authorised Representative / Contact**

  ----------------------------------- ------------ -----------------------------------------------
  **Item**                            **Status**   **Notes**
  Full Legal Name of Representative   Mandatory    As on passport or national ID
  Passport or Government-Issued ID    Mandatory    For KYC purposes; not stored on Platform
  Business Email Address              Mandatory    Used for all Platform communications
  Phone Number (mobile preferred)     Mandatory    For 2FA and deal notifications
  LinkedIn Profile                    Optional     Increases investor trust; recommended
  Secondary Contact Person            Optional     Finance director, legal counsel, or deal lead
  ----------------------------------- ------------ -----------------------------------------------

**C. Project Card Data (per Project)**

Each Project listed on the Platform must include the following data fields to generate a Project Card visible to investors:

  -------------------------------------------- ------------ --------------------------------------------------------
  **Field**                                    **Status**   **Description / Accepted Format**
  Project Name                                 Mandatory    Commercial or working title
  Project Type                                 Mandatory    Solar / Wind / Hydro / Storage / Transmission / Other
  Installed Capacity (MW / MWh)                Mandatory    Gross and net; separate AC/DC if applicable
  Location (Country / Region / Municipality)   Mandatory    GPS coordinates optional but recommended
  Current Development Stage                    Mandatory    Development / RTB / Construction / Operating
  Estimated Total CapEx (EUR / USD)            Mandatory    Total project cost including soft costs
  Transaction Type Sought                      Mandatory    Equity / Debt / M&A / PPP / JV
  AITA Fee Stage (Development / CapEx)         Mandatory    Per Annex 1, Part C criteria
  Target Close Date                            Optional     Month/Year; approximate acceptable
  Short Project Description (max 300 words)    Mandatory    Plain language; no confidential data in public card
  Project Logo / Rendering / Site Photo        Optional     PNG/JPG, min 1200×800 px; greatly increases engagement
  -------------------------------------------- ------------ --------------------------------------------------------

**D. Technical Documentation (per Project)**

  --------------------------------------------------------------- ------------------------------------ --------------------------------------------------------
  **Document**                                                    **Status**                           **Notes**
  Technical Feasibility Study or Pre-Feasibility Report           Mandatory                            Including energy resource assessment (wind/solar data)
  Grid Connection Application / Agreement                         Mandatory (CapEx) / Optional (Dev)   At minimum: confirmation of application submission
  Environmental Impact Assessment (EIA) or Screening              Mandatory (if available)             Issued or pending; draft acceptable
  Construction / Development Permit Status                        Mandatory                            Issued, applied for, or roadmap to permit
  Land Rights Documentation (ownership/lease/right of way)        Mandatory                            Title deed, long-term lease, or LOI with landowner
  EPC Scope of Work / Term Sheet (if available)                   Optional                             Strengthens investor confidence in execution readiness
  Energy Production Simulation (P50/P90)                          Optional                             Annual yield report from resource assessment
  Technical Advisors / Engineering Consultants (CVs/experience)   Optional                             Lends credibility; supports due diligence
  --------------------------------------------------------------- ------------------------------------ --------------------------------------------------------

**E. Financial Documentation (per Project)**

  --------------------------------------------------- ------------------------------------------- -------------------------------------------------------
  **Document**                                        **Status**                                  **Notes**
  Project Financial Model (Excel / PDF)               Mandatory                                   30-year DCF with NPV, IRR, DSCR assumptions
  CapEx / Budget Breakdown                            Mandatory                                   By phase and cost category
  Revenue Assumptions (PPA / merchant / tariff)       Mandatory                                   Signed PPA or comparable market reference rates
  Corporate Audited Accounts (last 2 years)           Optional (Mandatory if revenue \> EUR 1M)   Or management accounts if newly incorporated
  Debt Term Sheet or Letter of Interest from Lender   Optional                                    Indicates financing readiness
  Equity Structure / Cap Table                        Optional                                    Required if equity investment is the transaction type
  Insurance Summary / Coverage Plan                   Optional                                    Construction all-risk, O&M, liability
  --------------------------------------------------- ------------------------------------------- -------------------------------------------------------

**F. Platform Acceptance Declaration**

Upon uploading all Mandatory documents and completing the Platform Registration Form, the Developer electronically confirms:

-   All submitted data is accurate, complete, and current as of the date of submission.

-   Developer holds all rights and permissions necessary to share the uploaded documents with AITA.

-   Developer agrees to notify AITA within five (5) business days of any material change to Project data already submitted.

-   Developer has reviewed and agreed to the Cooperation Agreement, Annexes 1--5, and AITA\'s Privacy Policy.

AITA reserves the right to request additional documents or clarifications at any time during the verification process. AITA\'s failure to request documents does not relieve Developer of the obligation to maintain accuracy of submitted information.

**G. Acknowledgement**

**Developer confirms receipt and understanding of this Onboarding Checklist and commits to submit all Mandatory items prior to Project publication.**

+--------------------------------------------------------------------------+--------------------------------------------------------------------------+
| **AITA WORLD, S.L.**                                                     | **DEVELOPER**                                                            |
|                                                                          |                                                                          |
| By: _________________________________   | By: _________________________________   |
|                                                                          |                                                                          |
| Name: Dmytro Mekhed                                                      | Name:                                                                    |
|                                                                          |                                                                          |
| Title: Director                                                          | Title:                                                                   |
|                                                                          |                                                                          |
| Date: _________________________________ | Date: _________________________________ |
+--------------------------------------------------------------------------+--------------------------------------------------------------------------+


---

# ═══ PROFILE 1 — Додаток 2: Контрольний список онбордингу (UA) ═══

**ДОДАТОК 2**

**Контрольний список для онбордингу Розробника**

*(Додаток 2 до Договору про співпрацю)*

Цей контрольний список визначає мінімальний набір інформації та документів, необхідних Розробнику для завершення онбордингу на Платформі AITA. Завершення всіх «Обов\'язкових» пунктів потрібне для переведення Проекту зі статусу «Чернетка» до статусу «Верифіковано». «Опціональні» пункти рекомендуються для максимальної привабливості для інвесторів та прискорення закриття угоди.

**A. Корпоративна та правова ідентичність**

  ------------------------------------------------------ -------------- --------------------------------------------------------------------------------------
  **Документ**                                           **Статус**     **Примітки**
  Свідоцтво про реєстрацію / Установчий документ         Обов\'язково   Сканована копія, не старше 12 місяців
  Статут / Установчий договір                            Обов\'язково   Актуальна версія з усіма змінами
  Витяг з торгового реєстру (або аналог)                 Обов\'язково   Виданий не більше 6 місяців тому
  Ідентифікаційний номер платника податків (ІПН / ПДВ)   Обов\'язково   Застосовується у юрисдикції реєстрації
  Підтвердження юридичної адреси                         Обов\'язково   Рахунок за комунальні послуги, банківський лист або офіційний муніципальний документ
  Список кінцевих бенефіціарних власників (КБВ ≥ 25%)    Обов\'язково   Потрібно для відповідності вимогам ПВК/ПФТ
  Організаційна структура / Структура групи              Опціонально    Якщо є частиною корпоративної групи
  Довіреності (якщо підписант ≠ директор)                Обов\'язково   Нотаріально посвідчені та апостильовані за необхідності
  ------------------------------------------------------ -------------- --------------------------------------------------------------------------------------

**B. Уповноважений представник / Контактна особа**

  ------------------------------------------- -------------- --------------------------------------------------------------
  **Документ**                                **Статус**     **Примітки**
  Повне юридичне ім\'я представника           Обов\'язково   Як у паспорті або національному посвідченні
  Паспорт або національне посвідчення особи   Обов\'язково   Для цілей KYC; не зберігається на Платформі
  Корпоративна електронна адреса              Обов\'язково   Використовується для всіх комунікацій на Платформі
  Номер телефону (мобільний --- бажано)       Обов\'язково   Для двофакторної аутентифікації та сповіщень
  Профіль LinkedIn                            Опціонально    Підвищує довіру інвесторів; рекомендується
  Другий контактний представник               Опціонально    Фінансовий директор, юридичний радник або провідний по угоді
  ------------------------------------------- -------------- --------------------------------------------------------------

**C. Дані картки проекту (по кожному проекту)**

Кожен Проект, розміщений на Платформі, повинен містити наступні поля даних для формування Картки проекту, видимої інвесторам:

  ---------------------------------------------------- -------------- ------------------------------------------------------------------------
  **Поле**                                             **Статус**     **Опис / Прийнятий формат**
  Назва проекту                                        Обов\'язково   Комерційна або робоча назва
  Тип проекту                                          Обов\'язково   Сонячна / Вітрова / Гідро / Зберігання / Передача / Інше
  Встановлена потужність (МВт / МВт·год)               Обов\'язково   Брутто та нетто; AC/DC окремо, якщо застосовно
  Місцезнаходження (країна / регіон / муніципалітет)   Обов\'язково   GPS-координати опціонально, але рекомендується
  Поточна стадія розробки                              Обов\'язково   Розробка / RTB / Будівництво / Введено в експлуатацію
  Орієнтовний загальний CapEx (EUR / USD)              Обов\'язково   Загальна вартість проекту включно з непрямими витратами
  Тип шуканої угоди                                    Обов\'язково   Акціонерне / Боргове / M&A / ДПП / СП
  Стадія для комісії AITA (Розробка / CapEx)           Обов\'язково   Відповідно до критеріїв Додатку 1, Частина C
  Цільова дата закриття                                Опціонально    Місяць/Рік; орієнтовна дата прийнятна
  Короткий опис проекту (макс. 300 слів)               Обов\'язково   Доступна мова; у публічній картці не повинно бути конфіденційних даних
  Логотип / Рендеринг / Фото майданчика                Опціонально    PNG/JPG, мін. 1200×800 пкс; значно підвищує залученість
  ---------------------------------------------------- -------------- ------------------------------------------------------------------------

**D. Технічна документація (по кожному проекту)**

  ------------------------------------------------------------------ ----------------------------------------------- -----------------------------------------------------------------------------
  **Документ**                                                       **Статус**                                      **Примітки**
  Техніко-економічне обґрунтування або попереднє ТЕО                 Обов\'язково                                    Включаючи оцінку енергетичного ресурсу (дані вітру/сонця)
  Заявка на підключення / Угода про підключення до мережі            Обов\'язково (CapEx) / Опціонально (Розробка)   Мінімум: підтвердження подачі заяви
  Оцінка впливу на навколишнє середовище (ОВНС) або Скринінг         Обов\'язково (якщо є)                           Видана або на стадії розгляду; чернетка прийнятна
  Статус будівельного / дозвільного дозволу                          Обов\'язково                                    Видано, подано або дорожна карта до дозволу
  Документи на право землекористування (власність/оренда/сервітут)   Обов\'язково                                    Правовстановлюючий документ, довгострокова оренда або ЛНН з власником землі
  Технічне завдання EPC / Протокол намірів (якщо є)                  Опціонально                                     Підвищує довіру інвесторів щодо готовності до реалізації
  Симуляція виробництва електроенергії (P50/P90)                     Опціонально                                     Звіт про річний вихід з оцінки ресурсів
  Технічні консультанти / Інженерні компанії (CV/досвід)             Опціонально                                     Підвищує довіру; підтримує due diligence
  ------------------------------------------------------------------ ----------------------------------------------- -----------------------------------------------------------------------------

**E. Фінансова документація (по кожному проекту)**

  --------------------------------------------------------------- ----------------------------------------------------- ------------------------------------------------------------------
  **Документ**                                                    **Статус**                                            **Примітки**
  Фінансова модель проекту (Excel / PDF)                          Обов\'язково                                          30-річний DCF з припущеннями NPV, IRR, DSCR
  Розбивка CapEx / Бюджет                                         Обов\'язково                                          За фазами та категоріями витрат
  Припущення щодо доходів (PPA / ринок / тариф)                   Обов\'язково                                          Підписана угода PPA або порівнянні ринкові ставки
  Аудована корпоративна звітність (за 2 роки)                     Опціонально (Обов\'язково при виручці \> 1 млн EUR)   Або управлінська звітність для нещодавно зареєстрованих компаній
  Умовний аркуш боргу або Лист про зацікавленість від кредитора   Опціонально                                           Вказує на готовність до фінансування
  Акціонерна структура / Кептейбл                                 Опціонально                                           Обов\'язково, якщо тип угоди --- акціонерне інвестування
  Зведення страхового покриття / Plan страхування                 Опціонально                                           All-risk при будівництві, O&M, відповідальність
  --------------------------------------------------------------- ----------------------------------------------------- ------------------------------------------------------------------

**F. Декларація прийняття умов Платформи**

Після завантаження всіх Обов\'язкових документів та заповнення Форми реєстрації на Платформі, Розробник електронно підтверджує:

-   Усі подані дані є точними, повними та актуальними на дату подачі.

-   Розробник має всі права та дозволи, необхідні для надання завантажених документів AITA.

-   Розробник погоджується повідомити AITA протягом п\'яти (5) робочих днів про будь-які суттєві зміни в раніше поданих даних Проекту.

-   Розробник ознайомився та погодився з Договором про співпрацю, Додатками 1--5 та Політикою конфіденційності AITA.

AITA залишає за собою право в будь-який час у процесі верифікації запросити додаткові документи або роз\'яснення. Відсутність такого запиту з боку AITA не звільняє Розробника від обов\'язку підтримувати точність поданої інформації.

**G. Підтвердження**

**Розробник підтверджує отримання та розуміння цього Контрольного списку для онбордингу та зобов\'язується подати всі Обов\'язкові документи до публікації Проекту.**

+------------------------------------------------------------------------------+------------------------------------------------------------------------------+
| **AITA WORLD, S.L.**                                                         | **РОЗРОБНИК**                                                                |
|                                                                              |                                                                              |
| Підпис: _________________________________   | Підпис: _________________________________   |
|                                                                              |                                                                              |
| Ім\'я: Dmytro Mekhed                                                         | Ім\'я:                                                                       |
|                                                                              |                                                                              |
| Посада: Директор                                                             | Посада:                                                                      |
|                                                                              |                                                                              |
| Дата: ___________________________________ | Дата: ___________________________________ |
+------------------------------------------------------------------------------+------------------------------------------------------------------------------+


---

# ═══ PROFILE 1 — Annex 3: Invoice & Payment Terms (EN) ═══

**ANNEX 3**

**Invoice and Payment Terms Template**

*(Annex 3 to the Cooperation Agreement)*

This Annex 3 sets out the standard invoice format and payment terms that apply to all Success Fee invoices issued by AITA WORLD, S.L. to Developer under the Cooperation Agreement. Each invoice will be generated and delivered following a Successful Closing, as defined in Cooperation Agreement §2.5.

**A. Standard Invoice Template**

+-------------------------------------------------------+------------------------------------------------------------------+
| **INVOICE**                                           |                                                                  |
+-------------------------------------------------------+------------------------------------------------------------------+
| **ISSUED BY:**                                        | **INVOICED TO:**                                                 |
|                                                       |                                                                  |
| **AITA WORLD, S.L.**                                  | Company Name:                                                    |
|                                                       |                                                                  |
| CIF: B75859744                                        | Tax ID:                                                          |
|                                                       |                                                                  |
| Sabino Arana, 8-2, 48013 Bilbao, Bizkaia, España      | Address:                                                         |
|                                                       |                                                                  |
| Email: d.mekhed\@aita.world                           | Email:                                                           |
+-------------------------------------------------------+------------------------------------------------------------------+
| **Invoice No.:** AITA-                                | **Payment Due:** 10 business days from invoice date              |
|                                                       |                                                                  |
| **Invoice Date:**                                     | **Currency:** EUR (or as agreed in writing)                      |
+-------------------------------------------------------+------------------------------------------------------------------+

  ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- ----------------------------- ------------------ ----------------------
  **Description of Services**                                                                                                                                                                     **Transaction Value (EUR)**   **Fee Rate (%)**   **Fee Amount (EUR)**
  AITA Success Fee --- Project Sourcing, Listing, Verification, Investor Matching and Transaction Facilitation for: \[Project Name\] --- \[Location\] --- \[Capacity\] --- \[Transaction Type\]                                                                   
  Subtotal                                                                                                                                                                                                                                                        
  VAT (21% --- Spanish VAT, if applicable)                                                                                                                                                                                      21%                               
  **TOTAL DUE**                                                                                                                                                                                                                                    **               **
  ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- ----------------------------- ------------------ ----------------------

  -------------------------------------------------------------------------------------
  **PAYMENT DETAILS**
  Bank: BBVA (Bilbao, Spain) \| Account Holder: AITA WORLD, S.L.
  IBAN: ES__ ____ ____ ____ ____ ____ \| SWIFT/BIC: BBVAESMMXXX
  Payment Reference: \[Invoice No.\] --- \[Project Name\] --- \[Developer Name\]
  Wire transfer in EUR only. All bank charges payable by the payer.
  -------------------------------------------------------------------------------------

**B. Payment Terms and Conditions**

**B.1 **Due Date: All invoices are due within ten (10) business days from the invoice date, unless a different term has been agreed in writing between the Parties.

**B.2 **Late Payment: Overdue amounts shall accrue interest at the rate of three percent (3%) per annum above the European Central Bank base rate, from the due date until the date of actual payment.

**B.3 **Disputes: If Developer disputes any invoice amount, written notice must be provided to AITA within five (5) business days of invoice receipt, specifying the disputed amount and grounds. Undisputed portions are payable on the original due date.

**B.4 **Currency and Taxes: All fees are quoted and payable in EUR. Developer is responsible for all applicable taxes, withholdings, and levies outside Spain. AITA will apply Spanish VAT (21%) where required by law.

**B.5 **Escrow: For transactions exceeding EUR 5,000,000, AITA may request that success fees be deposited into a jointly-agreed escrow account at closing, to be released to AITA upon confirmation of the Successful Closing by both Parties.

**C. Transaction Confirmation Requirement**

Prior to issuing an invoice, AITA shall request written confirmation from Developer (and, where practicable, from the Investor or financing party) of the following:

-   Final transaction amount (equity raised, debt drawn, or purchase price paid).

-   Date of Successful Closing (execution of binding transaction documents).

-   Names of all parties involved in the transaction.

-   Confirmation that AITA\'s introduction or sourcing directly contributed to the transaction.

If Developer or Investor fails to provide confirmation within ten (10) business days of AITA\'s written request, AITA may issue an invoice based on available deal information and publicly accessible transaction data, which shall be binding unless challenged within five (5) business days of receipt.

**D. Illustrative Fee Examples**

  ------------------------------------------ ----------------------- ------------- -------------- ---------------
  **Scenario**                               **Transaction Value**   **Stage**     **Fee Rate**   **AITA Fee**
  Solar park rights sale (Development)       EUR 3,000,000           Development   5.0%           EUR 150,000
  Wind farm equity raise (RTB / CapEx)       EUR 20,000,000          CapEx         2.7%           EUR 540,000
  Hybrid solar+storage M&A deal (CapEx)      EUR 50,000,000          CapEx         2.7%           EUR 1,350,000
  Transmission corridor development rights   EUR 1,500,000           Development   5.0%           EUR 75,000
  ------------------------------------------ ----------------------- ------------- -------------- ---------------

Note: The above examples are illustrative only. Actual fees are calculated per the transaction value confirmed at Successful Closing, applying the applicable rate from Annex 1, Part C.

**E. Acknowledgement**

**Developer confirms it has reviewed and understood the payment terms set out in this Annex 3.**

+--------------------------------------------------------------------------+--------------------------------------------------------------------------+
| **AITA WORLD, S.L.**                                                     | **DEVELOPER**                                                            |
|                                                                          |                                                                          |
| By: _________________________________   | By: _________________________________   |
|                                                                          |                                                                          |
| Name: Dmytro Mekhed                                                      | Name:                                                                    |
|                                                                          |                                                                          |
| Title: Director                                                          | Title:                                                                   |
|                                                                          |                                                                          |
| Date: _________________________________ | Date: _________________________________ |
+--------------------------------------------------------------------------+--------------------------------------------------------------------------+


---

# ═══ PROFILE 1 — Додаток 3: Рахунок та умови оплати (UA) ═══

**ДОДАТОК 3**

**Шаблон рахунку-фактури та умови оплати**

*(Додаток 3 до Договору про співпрацю)*

Цей Додаток 3 встановлює стандартний формат рахунку-фактури та умови оплати, що застосовуються до всіх рахунків-фактур за комісію за успішне закриття, виставлених AITA WORLD, S.L. Розробнику відповідно до Договору про співпрацю. Кожен рахунок-фактура формується та надсилається після Успішного закриття, як визначено у §2.5 Договору про співпрацю.

**A. Стандартний шаблон рахунку-фактури**

+-------------------------------------------------------+-----------------------------------------------------------------+
| **РАХУНОК-ФАКТУРА**                                   |                                                                 |
+-------------------------------------------------------+-----------------------------------------------------------------+
| **ВИСТАВЛЕНО:**                                       | **ВИСТАВЛЕНО НА АДРЕСУ:**                                       |
|                                                       |                                                                 |
| **AITA WORLD, S.L.**                                  | Назва компанії:                                                 |
|                                                       |                                                                 |
| КІФ: B75859744                                        | ІПН:                                                            |
|                                                       |                                                                 |
| Sabino Arana, 8-2, 48013 Bilbao, Bizkaia, Іспанія     | Адреса:                                                         |
|                                                       |                                                                 |
| Email: d.mekhed\@aita.world                           | Email:                                                          |
+-------------------------------------------------------+-----------------------------------------------------------------+
| **№ рахунку:** AITA-                                  | **Строк оплати:** 10 робочих днів з дати рахунку                |
|                                                       |                                                                 |
| **Дата рахунку:**                                     | **Валюта:** EUR (або за письмовою домовленістю)                 |
+-------------------------------------------------------+-----------------------------------------------------------------+

  ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- --------------------------- ----------------- ------------------------
  **Опис послуг**                                                                                                                                                                                         **Вартість угоди (EUR)**    **Ставка (%)**    **Сума комісії (EUR)**
  Комісія AITA за успішне закриття --- Пошук, розміщення, верифікація проекту, підбір інвесторів та супровід угоди для: \[Назва проекту\] --- \[Місцезнаходження\] --- \[Потужність\] --- \[Тип угоди\]                                                                
  Проміжний підсумок                                                                                                                                                                                                                                                   
  ПДВ (21% --- іспанський ПДВ, якщо застосовно)                                                                                                                                                                                       21%                              
  **РАЗОМ ДО СПЛАТИ**                                                                                                                                                                                                                                   **               **
  ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- --------------------------- ----------------- ------------------------

  -------------------------------------------------------------------------------------
  **РЕКВІЗИТИ ДЛЯ ОПЛАТИ**
  Банк: BBVA (Більбао, Іспанія) \| Власник рахунку: AITA WORLD, S.L.
  IBAN: ES__ ____ ____ ____ ____ ____ \| SWIFT/BIC: BBVAESMMXXX
  Призначення платежу: \[№ рахунку\] --- \[Назва проекту\] --- \[Назва Розробника\]
  Переказ лише в EUR. Усі банківські комісії сплачує платник.
  -------------------------------------------------------------------------------------

**B. Умови оплати**

**B.1 **Строк оплати: Усі рахунки-фактури підлягають оплаті протягом десяти (10) робочих днів з дати виставлення рахунку, якщо інший строк не погоджено Сторонами в письмовій формі.

**B.2 **Прострочення платежу: На прострочені суми нараховуються відсотки у розмірі трьох відсотків (3%) річних понад базову ставку Європейського центрального банку, з дня настання строку оплати до дня фактичного платежу.

**B.3 **Спори: Якщо Розробник оскаржує будь-яку суму рахунку, письмове повідомлення повинно бути надано AITA протягом п\'яти (5) робочих днів після отримання рахунку, із зазначенням оспорюваної суми та підстав. Неоспорювані суми підлягають оплаті у первісний строк.

**B.4 **Валюта та податки: Усі комісії виставляються та сплачуються в EUR. Розробник несе відповідальність за всі застосовні податки, утримання та збори поза Іспанією. AITA застосовує іспанський ПДВ (21%), де це вимагається законом.

**B.5 **Ескроу: Для угод, що перевищують 5 000 000 EUR, AITA може вимагати, щоб комісії за успішне закриття були розміщені на спільно погодженому рахунку ескроу при закритті, з вивільненням коштів на користь AITA після підтвердження Успішного закриття обома Сторонами.

**C. Вимога щодо підтвердження угоди**

До виставлення рахунку-фактури AITA запитує у Розробника письмове підтвердження (а за можливістю --- від Інвестора або фінансуючої сторони) наступного:

-   Остаточна сума угоди (залучений акціонерний капітал, отримане боргове фінансування або сплачена ціна придбання).

-   Дата Успішного закриття (підписання обов\'язкових документів по угоді).

-   Назви всіх сторін, залучених до угоди.

-   Підтвердження того, що залучення або пошук з боку AITA безпосередньо сприяли угоді.

Якщо Розробник або Інвестор не надає підтвердження протягом десяти (10) робочих днів після письмового запиту AITA, AITA може виставити рахунок на підставі наявної інформації та публічно доступних даних по угоді, який вважається обов\'язковим, якщо не оскаржено протягом п\'яти (5) робочих днів після отримання.

**D. Ілюстративні приклади розрахунку комісії**

  ------------------------------------------------------------------ -------------------- ------------ ------------ ------------------
  **Сценарій**                                                       **Вартість угоди**   **Стадія**   **Ставка**   **Комісія AITA**
  Продаж прав на сонячний парк (Розробка)                            3 000 000 EUR        Розробка     5,0%         150 000 EUR
  Залучення акціонерного капіталу для вітрової ферми (RTB / CapEx)   20 000 000 EUR       CapEx        2,7%         540 000 EUR
  Угода M&A гібридний сонце+зберігання (CapEx)                       50 000 000 EUR       CapEx        2,7%         1 350 000 EUR
  Права на розробку коридору електропередач                          1 500 000 EUR        Розробка     5,0%         75 000 EUR
  ------------------------------------------------------------------ -------------------- ------------ ------------ ------------------

Примітка: Наведені вище приклади мають ілюстративний характер. Фактичні комісії розраховуються відповідно до суми угоди, підтвердженої при Успішному закритті, за застосовною ставкою з Додатку 1, Частина C.

**E. Підтвердження**

**Розробник підтверджує, що ознайомився та зрозумів умови оплати, встановлені у цьому Додатку 3.**

+------------------------------------------------------------------------------+------------------------------------------------------------------------------+
| **AITA WORLD, S.L.**                                                         | **РОЗРОБНИК**                                                                |
|                                                                              |                                                                              |
| Підпис: _________________________________   | Підпис: _________________________________   |
|                                                                              |                                                                              |
| Ім\'я: Dmytro Mekhed                                                         | Ім\'я:                                                                       |
|                                                                              |                                                                              |
| Посада: Директор                                                             | Посада:                                                                      |
|                                                                              |                                                                              |
| Дата: ___________________________________ | Дата: ___________________________________ |
+------------------------------------------------------------------------------+------------------------------------------------------------------------------+


---

# ═══ PROFILE 1 — Annex 4: Commercial Package Order (EN) ═══

**ANNEX 4**

**Commercial Package Order Form**

*(Annex 4 to the Cooperation Agreement)*

This Order Form is used by Developer to activate a Commercial Package for one or more Projects on the AITA Platform, in accordance with Cooperation Agreement §5.2 and Annex 1, Part B. A completed and countersigned Order Form constitutes a binding commitment by Developer to the selected Package and its fee schedule.

**A. Developer Details**

  ---------------------------- ----------------------------------------------------------------------------------
  **Field**                    **Value**
  Developer Legal Name                                                                                         
  Country of Incorporation                                                                                     
  Authorised Representative                                                                                    
  Contact Email                                                                                                
  Cooperation Agreement Date                                                                                   
  Order Form Reference No.     AITA-OF-                                                            
  Order Form Date                                                                                              
  ---------------------------- ----------------------------------------------------------------------------------

**B. Project Details**

Complete one (1) row per Project covered by this Order Form. Additional rows may be added for multi-project orders. Each Project must correspond to an existing listing on the AITA Platform.

  ---------------------- -------------- ------------------- -------------- -------------- ----------------------
  **Project Name**       **Type**       **Capacity (MW)**   **Stage**      **Country**    **Platform Status**
                                                                                                              
                                                                                                              
                                                                                                              
  ---------------------- -------------- ------------------- -------------- -------------- ----------------------

**C. Package Selection**

Select the Commercial Package(s) applicable to this Order. One Package applies per Project, unless otherwise agreed. For Tier 3 (Full Service), a separate Scope of Work may be attached.

+-------------------------+-----------------------------------------------------------+--------------------+----------------+---------------------------+
| **Package**             | **Key Features**                                          | **Fee Type**       | **Select (✓)** | **Applies to Project(s)** |
+-------------------------+-----------------------------------------------------------+--------------------+----------------+---------------------------+
| **Tier 1 Listing Plus** | Full Project Card + extended document upload              | Flat fee per Order |                |                           |
|                         |                                                           |                    |                |                           |
|                         | Completeness scoring + Standard investor pool access      |                    |                |                           |
|                         |                                                           |                    |                |                           |
|                         | Basic analytics dashboard                                 |                    |                |                           |
+-------------------------+-----------------------------------------------------------+--------------------+----------------+---------------------------+
| **Tier 2 Active**       | **All Tier 1 features, plus:**                            | Flat fee per Order |                |                           |
|                         |                                                           |                    |                |                           |
|                         | Investor advertising campaigns (AITA network + digital)   |                    |                |                           |
|                         |                                                           |                    |                |                           |
|                         | Targeted investor introductions + roadshow inclusion      |                    |                |                           |
|                         |                                                           |                    |                |                           |
|                         | Lead tracking + deal tracking module + advanced analytics |                    |                |                           |
+-------------------------+-----------------------------------------------------------+--------------------+----------------+---------------------------+
| **Tier 3 Full Service** | **All Tier 2 features, plus:**                            | Project SOW        |                |                           |
|                         |                                                           |                    |                |                           |
|                         | Strategy & financial model review by AITA analysts        |                    |                |                           |
|                         |                                                           |                    |                |                           |
|                         | SPV structuring assistance                                |                    |                |                           |
|                         |                                                           |                    |                |                           |
|                         | Priority matchmaking + dedicated account manager          |                    |                |                           |
|                         |                                                           |                    |                |                           |
|                         | *Separate Scope of Work (SOW) applies*                    |                    |                |                           |
+-------------------------+-----------------------------------------------------------+--------------------+----------------+---------------------------+

All Commercial Packages are in addition to (not a substitute for) the Success Fee applicable upon Successful Closing per Cooperation Agreement §8 and Annex 1, Part C.

**D. Investor Advertising Scope (Tiers 2 & 3 only)**

Where Developer selects Tier 2 or Tier 3, the following advertising scope applies by default. Developer may customise within the scope below by written instruction to AITA:

  ---------------------------------------------- ------------------------ ------------------------ ---------------------------
  **Advertising Channel**                        **Included in Tier 2**   **Included in Tier 3**   **Developer Can Opt Out**
  AITA Investor Newsletter (monthly)             ✓                        ✓                        Yes
  AITA LinkedIn & Social Media Posts             ✓                        ✓                        Yes
  AITA Investor Database --- Targeted Outreach   ✓                        ✓                        No
  AITA Investor Roadshow Inclusion               ✓                        ✓                        Yes
  1-on-1 Investor Introduction Meetings          ✗                        ✓                        No
  Financial Model / Teaser Preparation by AITA   ✗                        ✓                        N/A
  Press Release / Case Study Publication         ✗                        ✓                        Yes
  ---------------------------------------------- ------------------------ ------------------------ ---------------------------

AITA shall provide monthly reports on advertising reach, investor inquiries received, and response rates for all Tier 2 and Tier 3 Projects.

**E. Package Fee Summary**

Package fees are assessed per the fee schedule agreed at the time of Order Form execution and set out below. Where blank, fees are to be quoted by AITA based on project specifics:

  ----------------------------- ------------------------------- ---------------------- ---------------------------------------------------
  **Package**                   **Fee Type**                    **Amount (EUR)**       **When Payable**
  Tier 1 --- Listing Plus       Flat Fee (one-time)                                    Upon countersignature of Order Form
  Tier 2 --- Active             Flat Fee (one-time or annual)                          50% upon Order Form; 50% after 6 months
  Tier 3 --- Full Service       SOW-based (milestone)           Per SOW                Per SOW milestones
  **Success Fee (all tiers)**   \% of Transaction Value         Per Annex 1, Part C    Due within 10 business days of Successful Closing
  ----------------------------- ------------------------------- ---------------------- ---------------------------------------------------

All fees are subject to Spanish VAT (21%) as applicable. Payment instructions per Annex 3. Late payment interest: 3% p.a. above ECB base rate.

**F. Additional Terms & Developer Instructions**

Please specify any special instructions, campaign preferences, target geographies, or investor profile preferences for advertising:

  ------------------------------------------------------------------------------------------------------
  **Instructions / Preferences**
                                                                                                      
  ------------------------------------------------------------------------------------------------------

**G. Execution**

**By countersigning below, Developer activates the selected Commercial Package(s), acknowledges the applicable fee schedule, and confirms agreement to the terms of the Cooperation Agreement and its Annexes.**

+--------------------------------------------------------------------------+--------------------------------------------------------------------------+
| **AITA WORLD, S.L.**                                                     | **DEVELOPER**                                                            |
|                                                                          |                                                                          |
| By: _________________________________   | By: _________________________________   |
|                                                                          |                                                                          |
| Name: Dmytro Mekhed                                                      | Name:                                                                    |
|                                                                          |                                                                          |
| Title: Director                                                          | Title:                                                                   |
|                                                                          |                                                                          |
| Date: _________________________________ | Date: _________________________________ |
+--------------------------------------------------------------------------+--------------------------------------------------------------------------+


---

# ═══ PROFILE 1 — Додаток 4: Замовлення комерційного пакету (UA) ═══

**ДОДАТОК 4**

**Форма замовлення комерційного пакету**

*(Додаток 4 до Договору про співпрацю)*

Ця Форма замовлення використовується Розробником для активації Комерційного пакету для одного або кількох Проектів на Платформі AITA відповідно до §5.2 Договору про співпрацю та Додатку 1, Частина B. Заповнена та скріплена підписами обох сторін Форма замовлення є обов\'язковим зобов\'язанням Розробника щодо обраного Пакету та його шкали комісій.

**A. Реквізити Розробника**

  -------------------------------------- ----------------------------------------------------------------------------------
  **Поле**                               **Значення**
  Юридична назва Розробника                                                                                              
  Країна реєстрації                                                                                                      
  Уповноважений представник                                                                                              
  Контактна електронна адреса                                                                                            
  Дата Договору про співпрацю                                                                                            
  Реєстраційний номер Форми замовлення   AITA-OF-                                                            
  Дата Форми замовлення                                                                                                  
  -------------------------------------- ----------------------------------------------------------------------------------

**B. Дані проекту**

Заповніть один (1) рядок на кожен Проект, що охоплюється цією Формою замовлення. Для замовлень на кілька проектів можна додавати рядки. Кожен Проект повинен відповідати наявному розміщенню на Платформі AITA.

  ---------------------- -------------- ---------------------- -------------- -------------- -------------------------
  **Назва проекту**      **Тип**        **Потужність (МВт)**   **Стадія**     **Країна**     **Статус на Платформі**
                                                                                                                 
                                                                                                                 
                                                                                                                 
  ---------------------- -------------- ---------------------- -------------- -------------- -------------------------

**C. Вибір пакету**

Оберіть Комерційний пакет(и), застосовний до цього Замовлення. Один Пакет застосовується до одного Проекту, якщо не погоджено інше. Для Рівня 3 (Full Service) може додаватися окреме Технічне завдання.

+---------------------------+----------------------------------------------------------+-------------------------+---------------+---------------+
| **Пакет**                 | **Ключові функції**                                      | **Тип комісії**         | **Вибір (✓)** | **Проект(и)** |
+---------------------------+----------------------------------------------------------+-------------------------+---------------+---------------+
| **Рівень 1 Listing Plus** | Повна картка проекту + розширене завантаження документів | Фіксована по Замовленню |               |               |
|                           |                                                          |                         |               |               |
|                           | Оцінка повноти + Стандартний доступ до пулу інвесторів   |                         |               |               |
|                           |                                                          |                         |               |               |
|                           | Базова аналітична панель                                 |                         |               |               |
+---------------------------+----------------------------------------------------------+-------------------------+---------------+---------------+
| **Рівень 2 Active**       | **Усі функції Рівня 1, плюс:**                           | Фіксована по Замовленню |               |               |
|                           |                                                          |                         |               |               |
|                           | Рекламні кампанії для інвесторів (мережа AITA + цифрові) |                         |               |               |
|                           |                                                          |                         |               |               |
|                           | Цільові знайомства + участь у роадшоу                    |                         |               |               |
|                           |                                                          |                         |               |               |
|                           | Відстеження лідів + угод + розширена аналітика           |                         |               |               |
+---------------------------+----------------------------------------------------------+-------------------------+---------------+---------------+
| **Рівень 3 Full Service** | **Усі функції Рівня 2, плюс:**                           | За Техн. завд.          |               |               |
|                           |                                                          |                         |               |               |
|                           | Огляд стратегії та фінансової моделі аналітиками AITA    |                         |               |               |
|                           |                                                          |                         |               |               |
|                           | Допомога у структуруванні SPV                            |                         |               |               |
|                           |                                                          |                         |               |               |
|                           | Пріоритетний підбір + виділений акаунт-менеджер          |                         |               |               |
|                           |                                                          |                         |               |               |
|                           | *Застосовується окреме Технічне завдання*                |                         |               |               |
+---------------------------+----------------------------------------------------------+-------------------------+---------------+---------------+

Усі Комерційні пакети доповнюють (а не замінюють) Комісію за успішне закриття, застосовну при Успішному закритті відповідно до §8 Договору про співпрацю та Додатку 1, Частина C.

**D. Обсяг реклами для інвесторів (лише Рівні 2 та 3)**

Якщо Розробник обирає Рівень 2 або Рівень 3, за замовчуванням застосовується наступний обсяг реклами. Розробник може налаштувати обсяг письмовою інструкцією до AITA:

  -------------------------------------------- ------------------------- ------------------------- --------------------------------
  **Канал реклами**                            **Включено в Рівень 2**   **Включено в Рівень 3**   **Розробник може відмовитись**
  Інвесторський newsletter AITA (щомісяця)     ✓                         ✓                         Так
  Дописи AITA у LinkedIn та соцмережах         ✓                         ✓                         Так
  База інвесторів AITA --- Цільова розсилка    ✓                         ✓                         Ні
  Участь в інвесторських роадшоу AITA          ✓                         ✓                         Так
  Особисті зустрічі з інвесторами (1-на-1)     ✗                         ✓                         Ні
  Підготовка фінансової моделі / тізера AITA   ✗                         ✓                         Н/З
  Публікація прес-релізу / кейс-стаді          ✗                         ✓                         Так
  -------------------------------------------- ------------------------- ------------------------- --------------------------------

AITA надаватиме щомісячні звіти про охоплення реклами, отримані запити інвесторів та частоту відповідей для всіх Проектів Рівнів 2 та 3.

**E. Зведення комісій за пакетами**

Комісії за пакетами встановлюються відповідно до погодженої на момент виконання Форми замовлення шкали і наведені нижче. Де залишено пустим --- комісії буде визначено AITA на основі специфіки проекту:

  --------------------------------------------- ------------------------------------ -------------------------- ---------------------------------------------------
  **Пакет**                                     **Тип комісії**                      **Сума (EUR)**             **Строк оплати**
  Рівень 1 --- Listing Plus                     Фіксована (одноразово)                                          Після підписання Форми замовлення обома сторонами
  Рівень 2 --- Active                           Фіксована (одноразово або щорічно)                              50% при підписанні Форми; 50% через 6 місяців
  Рівень 3 --- Full Service                     За ТЗ (по віхах)                     За ТЗ                      За віхами ТЗ
  **Комісія за успішне закриття (всі рівні)**   \% від вартості угоди                За Додатком 1, Частина C   Протягом 10 робочих днів після Успішного закриття
  --------------------------------------------- ------------------------------------ -------------------------- ---------------------------------------------------

На всі комісії нараховується іспанський ПДВ (21%), де застосовно. Реквізити для оплати --- відповідно до Додатку 3. Штраф за прострочення: 3% річних понад базову ставку ЄЦБ.

**F. Додаткові умови та інструкції Розробника**

Вкажіть будь-які спеціальні інструкції, рекламні переваги, цільові географії або профілі інвесторів для реклами:

  ------------------------------------------------------------------------------------------------------
  **Інструкції / Переваги**
                                                                                                      
  ------------------------------------------------------------------------------------------------------

**G. Підписи**

**Підписуючи нижче, Розробник активує обраний(і) Комерційний(і) пакет(и), підтверджує застосовну шкалу комісій та погоджується з умовами Договору про співпрацю та його Додатків.**

+------------------------------------------------------------------------------+------------------------------------------------------------------------------+
| **AITA WORLD, S.L.**                                                         | **РОЗРОБНИК**                                                                |
|                                                                              |                                                                              |
| Підпис: _________________________________   | Підпис: _________________________________   |
|                                                                              |                                                                              |
| Ім\'я: Dmytro Mekhed                                                         | Ім\'я:                                                                       |
|                                                                              |                                                                              |
| Посада: Директор                                                             | Посада:                                                                      |
|                                                                              |                                                                              |
| Дата: ___________________________________ | Дата: ___________________________________ |
+------------------------------------------------------------------------------+------------------------------------------------------------------------------+


---

# ═══ PROFILE 1 — Annex 5: LOI Template (EN) ═══

**LETTER OF INTENT AND EXCLUSIVITY AGREEMENT**

***(Annex 5 to the Cooperation Agreement)***

[Date:                                                   ]

[Place:                                                 ]

**PARTIES:**

+-------------------------------+-------------------------------------------------------------------------------------+
| **AITA WORLD, S.L.**          | **DEVELOPER / INVESTOR**                                                            |
|                               |                                                                                     |
| CIF: B75859744                | [Legal Name:                                                   ]        |
|                               |                                                                                     |
| Address: Sabino Arana, 8-2    | [Country:                                                             ] |
|                               |                                                                                     |
| 48013 Bilbao, Bizkaia, España | [Contact Email:                                                 ]       |
|                               |                                                                                     |
| Email: d.mekhed\@aita.world   | [Contact Phone:                                                 ]       |
+-------------------------------+-------------------------------------------------------------------------------------+

**1. Project Description**

**1.1 **Project Name:                                                             

**1.2 **Location (Country / Region):                                         

**1.3 **Capacity / Scale:                                                   

**1.4 **Project Description / Business Model:

[                                                                      ]

[                                                                      ]

**2. Expression of Intent**

The Parties express their mutual interest in negotiating and potentially closing a transaction for the Project described in Section 1, on the following basis:

**2.1 **Transaction Stage (select one):

-   \[ \] Development Stage (permits, pre-FID, rights packages) → AITA fee: 5%

-   \[ \] CapEx / Investment Stage (RTB, FID-ready, construction financing) → AITA fee: 2.7%

**2.2 **Transaction Type (select one):

-   \[ \] Equity Investment

-   \[ \] Debt Financing

-   \[ \] M&A / Asset Sale

-   \[ \] PPP / Concession

-   \[ \] Strategic Partnership / Joint Venture

-   \[ \] Other:                                                   

**3. Exclusivity Period**

**3.1 **Term: One hundred twenty (120) calendar days from the Effective Date of this LOI (\"Exclusivity Period\").

**3.2 **During the Exclusivity Period, Developer agrees not to:

-   \(a\) Negotiate, finalize, or accept any competing offer for the same Project with other investors or financing parties;

-   \(b\) Propose materially better economic terms off-Platform to other potential investors;

-   \(c\) Use AITA\'s proprietary materials, data, investor introductions, or methodologies to complete an off-Platform transaction with any Investor;

-   \(d\) Engage third-party intermediaries or advisors to circumvent this LOI or AITA\'s involvement.

**3.3 **Permitted Exceptions: Developer may pursue parallel conversations with lenders or technical advisors (EPC, environmental) for due diligence purposes, provided such discussions do not constitute negotiation of commercial terms outside AITA\'s framework.

**4. AITA Success Fee Acknowledgment**

**4.1 **Developer acknowledges and accepts AITA\'s success-based fee as specified in the Cooperation Agreement §8 and Annex 1, Part C:

**• Development Stage:** 5% of total transaction value

**• CapEx / Investment Stage:** 2.7% of total transaction value

**4.2 **Transaction value is calculated per Cooperation Agreement §8.3 (total capital raised, debt principal, purchase price, or NPV equivalent).

**4.3 **Developer further acknowledges that AITA\'s introduction, sourcing, and negotiation support directly contributed to Investor\'s interest and that fees are due upon Successful Closing.

**5. Non-Circumvention**

**5.1 **Developer confirms that Section 9 of the Cooperation Agreement (Non-Circumvention, Confidentiality, Platform Non-Competition) applies in full to this LOI and any resulting transaction.

**5.2 **For twelve (12) months after termination of this LOI or after Successful Closing, Developer shall not circumvent AITA or solicit the identified Investor for the same or substantially similar Project without AITA\'s written consent.

**6. Governing Law and Dispute Resolution**

**6.1 **This LOI shall be governed by the laws of the Kingdom of Spain.

**6.2 **Any dispute arising from or relating to this LOI shall be resolved by binding arbitration under the Rules of the Corte de Arbitraje de Madrid (CAM), with seat in Madrid, Spain, conducted in English.

**7. Extension**

The Exclusivity Period may be extended by written agreement of the Parties. If the Parties wish to extend, both must execute a written extension letter at least thirty (30) days before the Exclusivity Period expires.

**8. Effect of This LOI**

**8.1 **Binding Provisions: The Exclusivity Period (§3), AITA Fee Acknowledgment (§4), and Non-Circumvention (§5) provisions are binding and enforceable upon execution.

**8.2 **Non-Binding Expression of Intent: All other provisions of this LOI (transaction structure, pricing, timeline, financing terms) express the Parties\' current intent but are not binding. Substantive transaction terms remain subject to negotiation and execution of definitive documentation (share purchase agreement, loan agreement, equity investment agreement, or other transaction documents as applicable).

**8.3 **No Obligation to Transact: Execution of this LOI does not obligate either Party to execute a definitive transaction agreement. However, all Parties commit to negotiate in good faith and in a timely manner.

**9. Execution**

**IN WITNESS WHEREOF, the Parties have executed this LOI as of the date first written above.**

+--------------------------------------------------------------------------+--------------------------------------------------------------------------+
| **AITA WORLD, S.L.**                                                     | **DEVELOPER / INVESTOR**                                                 |
|                                                                          |                                                                          |
| By: _________________________________   | By: _________________________________   |
|                                                                          |                                                                          |
| Name: Dmytro Mekhed                                                      | Name:                                                                    |
|                                                                          |                                                                          |
| Title: Director                                                          | Title:                                                                   |
|                                                                          |                                                                          |
| Date: _________________________________ | Date: _________________________________ |
+--------------------------------------------------------------------------+--------------------------------------------------------------------------+


---

# ═══ PROFILE 1 — Додаток 5: Лист про наміри (UA) ═══

**ЛИСТ ПРО НАМІРИ ТА УГОДА ПРО ЕКСКЛЮЗИВНІСТЬ**

***(Додаток 5 до Договору про співпрацю)***

[Дата:                                                   ]

[Місце:                                                 ]

**СТОРОНИ:**

+--------------------------------+--------------------------------------------------------------------------------------+
| **AITA WORLD, S.L.**           | **РОЗРОБНИК / ІНВЕСТОР**                                                             |
|                                |                                                                                      |
| КІФ: B75859744                 | [Юридична назва:                                           ]             |
|                                |                                                                                      |
| Адреса: Sabino Arana, 8-2      | [Країна:                                                               ] |
|                                |                                                                                      |
| 48013 Bilbao, Bizkaia, Іспанія | [Контактний Email:                                             ]         |
|                                |                                                                                      |
| Email: d.mekhed\@aita.world    | [Контактний телефон:                                           ]         |
+--------------------------------+--------------------------------------------------------------------------------------+

**1. Опис проекту**

**1.1 **Назва проекту:                                                             

**1.2 **Місцезнаходження (Країна / Регіон):                                 

**1.3 **Потужність / Масштаб:                                                   

**1.4 **Опис проекту / Бізнес-модель:

[                                                                      ]

[                                                                      ]

**2. Вираження намірів**

Сторони виражають взаємний інтерес до проведення переговорів та потенційного закриття угоди щодо Проекту, описаного у Розділі 1, на наступних засадах:

**2.1 **Стадія угоди (оберіть одну):

-   \[ \] Стадія розробки (дозволи, до FID, пакети прав) → Комісія AITA: 5%

-   \[ \] Стадія CapEx / Інвестування (RTB, готовий до FID, будівельне фінансування) → Комісія AITA: 2,7%

**2.2 **Тип угоди (оберіть один):

-   \[ \] Акціонерне інвестування

-   \[ \] Боргове фінансування

-   \[ \] M&A / Продаж активів

-   \[ \] ДПП / Концесія

-   \[ \] Стратегічне партнерство / Спільне підприємство

-   \[ \] Інше:                                                   

**3. Ексклюзивний період**

**3.1 **Строк: Сто двадцять (120) календарних днів з Дати набрання чинності цього ЛНН («Ексклюзивний період»).

**3.2 **Протягом Ексклюзивного періоду Розробник погоджується не:

-   (а) вести переговори, завершувати або приймати конкуруючі пропозиції щодо того ж Проекту від інших інвесторів або фінансуючих сторін;

-   (б) пропонувати суттєво кращі економічні умови поза Платформою іншим потенційним інвесторам;

-   (в) використовувати пропрієтарні матеріали, дані, представлення інвесторів або методологію AITA для завершення позаплатформних угод з будь-яким Інвестором;

-   (г) залучати сторонніх посередників або консультантів для обходу цього ЛНН або участі AITA.

**3.3 **Дозволені винятки: Розробник може вести паралельні розмови з кредиторами або технічними консультантами (EPC, екологічними) для цілей due diligence, за умови, що такі розмови не є переговорами щодо комерційних умов поза межами структури AITA.

**4. Визнання комісії AITA**

**4.1 **Розробник визнає та приймає комісію AITA, що залежить від успішного закриття, відповідно до §8 Договору про співпрацю та Додатку 1, Частина C:

**• Стадія розробки:** 5% від загальної вартості угоди

**• Стадія CapEx / Інвестування:** 2,7% від загальної вартості угоди

**4.2 **Вартість угоди розраховується відповідно до §8.3 Договору про співпрацю (загальний залучений капітал, сума основного боргу, ціна придбання або NPV-еквівалент).

**4.3 **Розробник також визнає, що пошук, підбір та підтримка переговорів з боку AITA безпосередньо сприяли зацікавленості Інвестора, і що комісії підлягають сплаті при Успішному закритті.

**5. Незалучення третіх сторін**

**5.1 **Розробник підтверджує, що Розділ 9 Договору про співпрацю (Незалучення третіх сторін, Конфіденційність, Некомпетиція на Платформі) застосовується у повному обсязі до цього ЛНН та будь-якої угоди, що з нього виникає.

**5.2 **Протягом дванадцяти (12) місяців після припинення цього ЛНН або після Успішного закриття Розробник не має права обходити AITA або залучати ідентифікованого Інвестора для того ж або аналогічного Проекту без письмової згоди AITA.

**6. Застосовне право та вирішення спорів**

**6.1 **Цей ЛНН регулюється законодавством Королівства Іспанія.

**6.2 **Будь-який спір, що виникає з цього ЛНН або пов\'язаний з ним, вирішується шляхом обов\'язкового арбітражу відповідно до Регламенту Мадридського арбітражного суду (CAM), місцем проведення є Мадрид, Іспанія, мовою провадження --- іспанська або англійська.

**7. Продовження**

Ексклюзивний період може бути продовжено за письмовою домовленістю Сторін. Якщо Сторони бажають продовжити, обидві повинні підписати письмовий лист про продовження не менше ніж за тридцять (30) днів до закінчення Ексклюзивного періоду.

**8. Правові наслідки цього ЛНН**

**8.1 **Обов\'язкові положення: Ексклюзивний період (§3), Визнання комісії AITA (§4) та Незалучення третіх сторін (§5) є обов\'язковими та виконуваними з моменту підписання.

**8.2 **Необов\'язкове вираження намірів: Усі інші положення цього ЛНН (структура угоди, ціноутворення, строки, умови фінансування) виражають поточні наміри Сторін, але не є обов\'язковими. Суттєві умови угоди залишаються предметом переговорів та підписання остаточної документації (договір купівлі-продажу акцій, кредитний договір, договір акціонерного інвестування або інші документи по угоді).

**8.3 **Відсутність зобов\'язання укладати угоду: Підписання цього ЛНН не зобов\'язує жодну зі Сторін підписувати остаточний договір по угоді. Однак усі Сторони зобов\'язуються вести переговори добросовісно та своєчасно.

**9. Підписи**

**НА ПІДТВЕРДЖЕННЯ ЧОГО Сторони підписали цей ЛНН на дату, зазначену в преамбулі.**

+------------------------------------------------------------------------------+------------------------------------------------------------------------------+
| **AITA WORLD, S.L.**                                                         | **РОЗРОБНИК / ІНВЕСТОР**                                                     |
|                                                                              |                                                                              |
| Підпис: _________________________________   | Підпис: _________________________________   |
|                                                                              |                                                                              |
| Ім\'я: Dmytro Mekhed                                                         | Ім\'я:                                                                       |
|                                                                              |                                                                              |
| Посада: Директор                                                             | Посада:                                                                      |
|                                                                              |                                                                              |
| Дата: ___________________________________ | Дата: ___________________________________ |
+------------------------------------------------------------------------------+------------------------------------------------------------------------------+


---

# ═══ PROFILE 2 — INVESTOR: ISA Agreement (EN) ═══

**INVESTOR SERVICES AGREEMENT**
===============================

**Matching, Transaction Support, Platform Execution, Co-Investment & Compliance Screening**

This Investor Services Agreement (the "**Agreement**") is entered into on **\[Date\]** (the "**Effective Date**") by and between:

1.  **AITA WORLD, S.L.**, a company incorporated under the laws of Spain, with registered office at **Sabino Arana, 8-2, 48013 Bilbao, Bizkaia, España**, registration no. **B75859744** ("**AITA**" or "**Provider**"), and

2.  **\[Investor Legal Name\]**, a **\[company / fund / individual\]** organized under the laws of **\[●\]**, with address at **\[●\]** ("**Investor**").

AITA and Investor are collectively the "**Parties**" and individually a "**Party**".

**1. Purpose and Scope**
------------------------

1.1. AITA provides Investor with services for sourcing and executing renewable/energy-related opportunities, including project matching, baseline audit support, deal tracking, legal coordination, platform-enabled procurement, advisory support, and (where applicable) co-investment into AITA-originated projects.\
1.2. Investor may purchase one or more service packages described in **Annex 1 (Commercial Terms & Fees)**.

**2. Definitions**
------------------

2.1. **Project** means an investment opportunity evaluated or executed under this Agreement.\
2.2. **Matching** means identifying, introducing, and coordinating relevant Project participants (developers, EPCs, suppliers, lenders, off-takers, etc.) and assembling a transaction workflow.\
2.3. **Baseline Audit** means the initial screening and validation package as defined in Annex 2.\
2.4. **Platform Transaction** means procurement or payment flows executed through AITA's platform where AITA purchases or arranges purchase for Investor.\
2.5. **AITA-Originated Projects** means projects sourced/owned/controlled by AITA and/or its affiliated ecosystem companies (or SPVs) and offered to Investor under co-investment terms.

**3. Service Packages**
-----------------------

3.1. **Package A --- Matching + Baseline Audit + Tracking + Legal Coordination.\
** AITA provides Matching bundled with Baseline Audit, transaction tracking, and coordination with legal service providers. Commercial terms: **Annex 1, Section A**.

3.2. **Package B --- Advisory Retainer + Deal Execution Support.\
** AITA provides consulting/advisory services up to the monthly hours cap plus Matching and deal execution support, and Platform Transactions where applicable. Commercial terms: **Annex 1, Section B**.

3.3. **Package C --- Co-Investment in AITA-Originated Projects.\
** AITA offers Investor participation in AITA-Originated Projects under special co-investment terms, including management services at a commercial rate. Commercial terms: **Annex 1, Section C**.

3.4. **Package D --- Investor/Deal Compliance Screening.\
** AITA provides screening of a prospective investor (or Investor's SPV / investment structure) against bank and institutional lender requirements per Project. Commercial terms: **Annex 1, Section D**.

**4. Baseline Audit, Due Diligence, and Legal Support**
-------------------------------------------------------

4.1. Baseline Audit is included only where expressly stated (Package A) and is limited to the scope in **Annex 2**.\
4.2. Any expanded technical, legal, tax, or financial due diligence beyond Baseline Audit is considered **Additional Work** and is chargeable if:\
(a) agreed in writing in advance (email or in-platform approval), and\
(b) budgeted or capped per **Annex 3 (Pre-Approved Costs & Budgeting)**.\
4.3. Legal services may be performed by AITA's in-house legal function and/or external counsel. External counsel fees are paid by Investor unless otherwise agreed.

**5. Deal Process, Tracking, and Investor Cooperation**
-------------------------------------------------------

5.1. Investor shall timely provide information required for onboarding, KYC/AML (if applicable), investment criteria, and decision-making.\
5.2. AITA will maintain deal status tracking and key documentation within the platform (or equivalent reporting channel if needed).\
5.3. Investor acknowledges that timelines and outcomes depend on third parties (developers, authorities, lenders, EPCs, sellers).

**6. Platform Transactions (Procurement for Investor)**
-------------------------------------------------------

6.1. Where Investor requests AITA to purchase equipment/services for Investor through the platform ("Platform Transactions"), Investor shall:\
(a) pre-approve scope and budget; and\
(b) fund the transaction or provide agreed payment security as required.\
6.2. Platform Transaction fees apply as per **Annex 1, Section B**.

**7. Fees, Invoicing, and Payment**
-----------------------------------

7.1. Fees are set out in **Annex 1**.\
7.2. Invoices are payable within **10 (ten) business days** unless stated otherwise.\
7.3. Unless explicitly stated, fees are exclusive of VAT and applicable taxes.

**8. Non-Circumvention**
------------------------

8.1. Investor shall not knowingly circumvent AITA by closing a transaction directly with a party introduced by AITA (or through AITA's platform process) for the same or substantially similar Project to avoid fees under this Agreement.\
8.2. This obligation applies during the term and for **12 months** after termination with respect to introductions made during the term.

**9. Confidentiality**
----------------------

9.1. "Confidential Information" includes any non-public information relating to Projects, counterparties, pricing, structures, documents, and platform outputs shared under this Agreement.\
9.2. Each Party shall use Confidential Information solely for performing this Agreement and shall protect it with commercially reasonable measures.\
9.3. Confidentiality survives for **3 years** after termination. Trade secrets remain protected as long as they remain trade secrets.

**10. Compliance; KYC/AML; Sanctions (where applicable)**
---------------------------------------------------------

10.1. Investor shall provide information reasonably required for KYC/AML, sanctions screening, and bank/institutional compliance checks, if requested by AITA or relevant financial counterparties.\
10.2. AITA may pause services if required compliance information is not provided.

**11. No Investment Advice; No Guarantee**
------------------------------------------

11.1. Unless explicitly agreed otherwise in writing, AITA provides operational, sourcing, and transaction support and does not provide regulated investment advice. Investor remains responsible for final investment decisions.\
11.2. AITA does not guarantee funding, returns, approvals, or closing of any transaction.

**12. Liability**
-----------------

12.1. Each Party is liable for its own willful misconduct and gross negligence.\
12.2. Except for fraud, willful misconduct, or breach of confidentiality, neither Party shall be liable for indirect or consequential damages.

**13. Term and Termination**
----------------------------

13.1. This Agreement begins on the Effective Date and continues for **12 months**, renewing automatically unless either Party gives **30 days' notice**.\
13.2. Either Party may terminate for material breach if not cured within **15 days** after written notice.\
13.3. Fees accrued prior to termination remain payable. Non-circumvention and confidentiality survive termination.

**14. Governing Law and Dispute Resolution**
--------------------------------------------

14.1. Governing law: **Spain**.\
14.2. Disputes: negotiation first, then **Corte de Arbitraje de Madrid (CAM), seat in Madrid, under CAM Arbitration Rules**.

**15. Force Majeure**

15.1. Neither Party shall be liable for delay or failure to perform obligations under this Agreement to the extent caused by events beyond its reasonable control, including but not limited to: acts of God, war, terrorism, pandemic, government restrictions, fire, flood, or power outages ("Force Majeure Event").

15.2. The affected Party shall promptly notify the other Party of the Force Majeure Event and use reasonable efforts to mitigate its effects. Obligations are suspended for the duration of the Force Majeure Event.

15.3. If a Force Majeure Event continues for more than sixty (60) days, either Party may terminate this Agreement by written notice without liability.

**16. Language and Controlling Version**

16.1. This Agreement is executed in English. The English version shall be the controlling version. Any translation of this Agreement into any other language is for informational purposes only and shall not affect the interpretation or enforcement of the English version.

**17. Personal Data Protection**

17.1. To the extent any Party processes personal data of individuals (including employees, representatives, and contacts) in connection with this Agreement, each Party shall act as an independent controller and shall comply with all applicable data protection laws, including Regulation (EU) 2016/679 (GDPR) and Ley Orgánica 3/2018 (LOPDGDD) where applicable.

17.2. Each Party warrants that it has an adequate legal basis for any processing of personal data undertaken in connection with this Agreement. The Parties shall cooperate to respond to data subject requests and regulatory inquiries.

**18. Notices**

18.1. Notices shall be sent to:\
**AITA email:** \[●\]\
**Investor email:** \[●\]\
**AITA address:** \[●\]\
**Investor address:** \[●\]

**19. Signatures**
------------------

**AITA WORLD, S.L.\
** Name/Title: _______________________\
Signature: ________________________ Date: ___________

**\[Investor Legal Name\]\
** Name/Title: _______________________\
Signature: ________________________ Date: ___________

**ANNEX 1 --- COMMERCIAL TERMS & FEES (MONETIZATION)**
======================================================

**A. Package A --- Matching + Baseline Audit + Tracking + Legal Coordination**
------------------------------------------------------------------------------

A.1. Scope: Matching bundled with Baseline Audit (Annex 2), deal tracking, and coordination with legal service providers.\
A.2. Fee: **1.5%** payable by Investor, calculated on the **Investment Amount** (defined below) for each closed Project.\
A.3. **Investment Amount** means the total equity and/or debt capital committed by Investor (or Investor's controlled entities/SPVs) into the Project at closing (or in tranches, pro rata upon each tranche).\
A.4. Trigger: payable upon the earliest of (i) signing of binding investment documentation that creates a funding obligation, or (ii) first capital transfer for the Project.

**B. Package B --- Advisory Retainer + Deal Execution + Platform Transactions**
-------------------------------------------------------------------------------

B.1. Retainer: **EUR 4,000 per month** covering up to **20 hours/month** of advisory time. Unused hours do not roll over unless agreed.\
B.2. Matching & Deal Execution Fee: **1.0%** of Investment Amount for each closed Project supported under this package.\
B.3. Platform Transaction Fee: **0.4%** of the gross transaction value executed through the platform where AITA purchases (or arranges purchase) for Investor.\
B.4. Pre-Approved Costs: Investor shall reimburse pre-approved third-party costs for selection and audit (technical/legal/tax/insurance/engineering), only if agreed in advance per Annex 3.

**C. Package C --- Co-Investment in AITA-Originated Projects (Special Terms)**
------------------------------------------------------------------------------

C.1. Eligibility: applies only to AITA-Originated Projects offered by AITA under a separate Project Term Sheet / SPV documentation.\
C.2. Minimum Ticket: the minimum check by Investor (or Investor group) depends on **country** and **availability of required licenses/permits** in the relevant jurisdiction; the specific minimum ticket is defined in the Project Term Sheet.\
C.3. Management Fee: AITA charges a commercial management fee of **10%**, based on a **mutually agreed market analysis** for the relevant country/project type and defined precisely in the Project Term Sheet (e.g., as a percentage of distributable cash flow, gross margin, or other agreed base).\
C.4. Other Terms: co-investment economics (equity split, preferred return, waterfall, governance, exit) are defined in the Project Term Sheet and SPV documents.

**D. Package D --- Bank/Institutional Compliance Screening (Per Project)**
--------------------------------------------------------------------------

D.1. Scope: screening of a prospective investor structure and/or counterparties for alignment with bank and institutional lender requirements (KYC/AML readiness, document checklist, structure fit, red-flag screening) per Project.\
D.2. Fee: **USD 15 per Project** screened, payable upon delivery of the screening output (report/checklist result) via platform or email.\
D.3. Limitations: this is a readiness/screening service and does not guarantee bank approval.

**ANNEX 2 --- BASELINE AUDIT (PACKAGE A INCLUDED SCOPE)**
=========================================================

Baseline Audit is an initial screening package intended to reduce obvious risks and prepare for deeper due diligence, including (as applicable to the Project stage):

1.  **Document intake & completeness check** (title, corporate documents/SPV, key permits status, grid connection status, land rights).

2.  **Counterparty sanity check** (basic background signals, reputational red flags using open sources where lawful).

3.  **Project parameters validation** (capacity, configuration assumptions, high-level CAPEX/OPEX reasonableness check).

4.  **Stage-gate readiness** (what is missing to move from pre-feasibility to feasibility / investment decision).

5.  **Risk register v1** (top risks + recommended mitigation actions).

Anything beyond the above is "Additional Work" under Annex 3.

**ANNEX 3 --- PRE-APPROVED COSTS & BUDGETING (SELECTION / AUDIT)**
==================================================================

3.1. Any third-party costs (technical, legal, tax, insurance, site visits, engineering, specialized audits) must be **pre-approved in writing** by Investor with either: (a) a fixed budget cap, or (b) a rate card and maximum hours.\
3.2. AITA may propose vendors and coordinate procurement; Investor pays third-party invoices directly where possible, or reimburses AITA if AITA pays on Investor's behalf (with evidence).\
3.3. If costs are not pre-approved, Investor has no obligation to reimburse them.

**ANNEX 4 --- OPTIONAL: SERVICE SELECTION (CHECKBOX PAGE)**
===========================================================

Investor selects (tick):\
☐ Package A (1.5%)\
☐ Package B (EUR 4,000/month + 1% + 0.4%)\
☐ Package C (Co-Investment; Project Term Sheet required)\
☐ Package D (\$15 per Project compliance screening)


---

# ═══ PROFILE 2 — INVESTOR: Угода ISA (UA) ═══

**УГОДА ПРО ІНВЕСТОРСЬКІ ПОСЛУГИ**

*Підбір, підтримка угод, виконання через Платформу, спільне інвестування та комплаєнс-скринінг*

Цю Угоду про інвесторські послуги («Угода») укладено \[Дата\] («Дата набрання чинності») між:

**AITA WORLD, S.L.**, компанія, зареєстрована відповідно до законодавства Іспанії, із зареєстрованим офісом за адресою: Sabino Arana, 8-2, 48013 Bilbao, Bizkaia, Іспанія, реєстраційний номер B75859744 («AITA» або «Провайдер»),

та

**\[Юридична назва Інвестора\]**, \[компанія / фонд / фізична особа\], зареєстрована(-ий) відповідно до законодавства \[●\], за адресою: \[●\] («Інвестор»).

AITA та Інвестор разом --- «Сторони», кожна окремо --- «Сторона».

**1. Предмет та сфера застосування**

**1.1 **AITA надає Інвестору послуги з пошуку та виконання можливостей у сфері відновлюваної енергетики / енергетичних проектів, включаючи підбір проектів, підтримку базового аудиту, відстеження угод, юридичну координацію, прокьюремент через Платформу, консультаційну підтримку та (за необхідності) спільне інвестування в проекти, що ініційовані AITA.

**1.2 **Інвестор може придбати один або декілька сервісних пакетів, описаних у Додатку 1 (Комерційні умови та тарифи).

**2. Визначення**

**2.1 **Проект --- інвестиційна можливість, що оцінюється або виконується за цією Угодою.

**2.2 **Підбір --- ідентифікація, представлення та координація відповідних учасників Проекту (розробників, EPC-підрядників, постачальників, кредиторів, offtake-партнерів тощо) та збирання workflow угоди.

**2.3 **Базовий аудит --- початковий пакет скринінгу та валідації, визначений у Додатку 2.

**2.4 **Платформна угода --- прокьюремент або платіжні потоки, що виконуються через Платформу AITA, де AITA купує або організовує купівлю для Інвестора.

**2.5 **Проекти, ініційовані AITA --- проекти, залучені/власні/контрольовані AITA та/або її афілійованими екосистемними компаніями (або SPV) та запропоновані Інвестору на умовах спільного інвестування.

**3. Сервісні пакети**

**3.1 **Пакет A --- Підбір + Базовий аудит + Відстеження + Юридична координація. AITA надає Підбір разом з Базовим аудитом, відстеженням угод та координацією з постачальниками юридичних послуг. Комерційні умови: Додаток 1, Розділ A.

**3.2 **Пакет B --- Консультаційний ретейнер + Підтримка виконання угоди. AITA надає консультаційні послуги до місячного ліміту годин плюс Підбір та підтримку виконання угоди, а також Платформні угоди, де застосовно. Комерційні умови: Додаток 1, Розділ B.

**3.3 **Пакет C --- Спільне інвестування в Проекти, ініційовані AITA. AITA пропонує Інвестору участь у Проектах, ініційованих AITA, на спеціальних умовах спільного інвестування, включаючи управлінські послуги за комерційною ставкою. Комерційні умови: Додаток 1, Розділ C.

**3.4 **Пакет D --- Комплаєнс-скринінг Інвестора/угоди. AITA проводить скринінг структури потенційного інвестора (або SPV Інвестора / інвестиційної структури) на відповідність вимогам банків та інституційних кредиторів за Проектом. Комерційні умови: Додаток 1, Розділ D.

**4. Базовий аудит, due diligence та юридична підтримка**

**4.1 **Базовий аудит включено лише там, де це прямо зазначено (Пакет A), і обмежується сферою, визначеною у Додатку 2.

**4.2 **Будь-яке розширене технічне, юридичне, податкове або фінансове due diligence понад Базовий аудит вважається Додатковою роботою та підлягає оплаті, якщо: (а) погоджено в письмовій формі заздалегідь (електронний лист або схвалення на Платформі), та (б) передбачено бюджетом або обмежено відповідно до Додатку 3 (Попередньо затверджені витрати та бюджетування).

**4.3 **Юридичні послуги можуть надаватися власною юридичною функцією AITA та/або зовнішніми юрадвокатами. Витрати на зовнішніх юрадвокатів сплачуються Інвестором, якщо не погоджено інше.

**5. Процес угоди, відстеження та співпраця Інвестора**

**5.1 **Інвестор своєчасно надає інформацію, необхідну для онбордингу, KYC/ПВК (за необхідності), інвестиційних критеріїв та прийняття рішень.

**5.2 **AITA підтримуватиме відстеження статусу угоди та ключову документацію на Платформі (або еквівалентному каналі звітності, якщо необхідно).

**5.3 **Інвестор визнає, що строки та результати залежать від третіх сторін (розробників, органів влади, кредиторів, EPC-підрядників, продавців).

**6. Платформні угоди (Прокьюремент для Інвестора)**

**6.1 **Якщо Інвестор запитує AITA придбати обладнання/послуги для Інвестора через Платформу («Платформні угоди»), Інвестор зобов\'язаний: (а) попередньо схвалити сферу та бюджет; та (б) профінансувати угоду або надати погоджене платіжне забезпечення.

**6.2 **Тарифи за Платформні угоди --- відповідно до Додатку 1, Розділ B.

**7. Тарифи, виставлення рахунків та оплата**

**7.1 **Тарифи визначені у Додатку 1.

**7.2 **Рахунки підлягають оплаті протягом 10 (десяти) робочих днів, якщо не зазначено інше.

**7.3 **Якщо прямо не зазначено, тарифи не включають ПДВ та застосовні податки.

**8. Незалучення третіх сторін**

**8.1 **Інвестор не має права свідомо обходити AITA, укладаючи угоду безпосередньо зі стороною, представленою AITA (або через процес Платформи AITA), щодо того ж або аналогічного Проекту з метою уникнення тарифів за цією Угодою.

**8.2 **Це зобов\'язання діє протягом строку дії та 12 місяців після припинення стосовно представлень, зроблених протягом строку дії.

**9. Конфіденційність**

**9.1 **«Конфіденційна інформація» включає будь-яку непублічну інформацію, що стосується Проектів, контрагентів, ціноутворення, структур, документів та виходів Платформи, наданих за цією Угодою.

**9.2 **Кожна Сторона використовуватиме Конфіденційну інформацію виключно для виконання цієї Угоди та захищатиме її з комерційно обґрунтованими заходами.

**9.3 **Конфіденційність зберігається протягом 3 років після припинення. Комерційна таємниця залишається захищеною, доки вона залишається комерційною таємницею.

**10. Комплаєнс; KYC/ПВК; Санкції (де застосовно)**

**10.1 **Інвестор надає інформацію, обґрунтовано необхідну для KYC/ПВК, скринінгу санкцій та перевірок відповідності вимогам банків/інституційних кредиторів, якщо цього вимагає AITA або відповідні фінансові контрагенти.

**10.2 **AITA може призупинити надання послуг, якщо необхідна комплаєнс-інформація не надана.

**11. Відсутність інвестиційних рекомендацій; Відсутність гарантій**

**11.1 **Якщо прямо не погоджено інше в письмовій формі, AITA надає операційну, пошукову та транзакційну підтримку і не надає регульованих інвестиційних рекомендацій. Інвестор залишається відповідальним за остаточні інвестиційні рішення.

**11.2 **AITA не гарантує фінансування, доходи, схвалення або закриття будь-якої угоди.

**12. Відповідальність**

**12.1 **Кожна Сторона несе відповідальність за власні умисні порушення та грубу необережність.

**12.2 **За винятком шахрайства, умисних порушень або порушення конфіденційності, жодна Сторона не несе відповідальності за непрямі або наслідкові збитки.

**13. Строк та припинення**

**13.1 **Ця Угода починається з Дати набрання чинності та діє 12 місяців, автоматично поновлюючись, якщо жодна зі Сторін не надасть 30-денного повідомлення.

**13.2 **Будь-яка Сторона може розірвати Угоду через суттєве порушення, якщо воно не усунуте протягом 15 днів після письмового повідомлення.

**13.3 **Тарифи, нараховані до припинення, залишаються до сплати. Незалучення третіх сторін та конфіденційність зберігаються після припинення.

**14. Застосовне право та вирішення спорів**

**14.1 **Застосовне право: Іспанія.

**14.2 **Спори: спочатку переговори, потім Мадридський арбітражний суд (CAM), місце проведення --- Мадрид, відповідно до Арбітражного регламенту CAM.

**18. Повідомлення**

**18.1 **Повідомлення надсилаються на:

Email AITA: \[●\]

Email Інвестора: \[●\]

Адреса AITA: Sabino Arana, 8-2, 48013 Bilbao, Bizkaia, Іспанія

Адреса Інвестора: \[●\]

**19. Підписи**

+---------------------------------------------------------------------------------------+---------------------------------------------------------------------------------------+
| **AITA WORLD, S.L.**                                                                  | **\[Юридична назва Інвестора\]**                                                      |
|                                                                                       |                                                                                       |
| Ім\'я/Посада: _______________________                          | Ім\'я/Посада: _______________________                          |
|                                                                                       |                                                                                       |
| Підпис: ________________________ Дата: ___________ | Підпис: ________________________ Дата: ___________ |
+---------------------------------------------------------------------------------------+---------------------------------------------------------------------------------------+

**ДОДАТОК 1 --- КОМЕРЦІЙНІ УМОВИ ТА ТАРИФИ**

**A. Пакет A --- Підбір + Базовий аудит + Відстеження + Юридична координація**

**A.1 **Сфера: Підбір разом з Базовим аудитом (Додаток 2), відстеженням угод та координацією з постачальниками юридичних послуг.

**A.2 **Тариф: 1,5%, що сплачуються Інвестором, розраховані від Суми інвестиції (визначено нижче) для кожного закритого Проекту.

**A.3 **Сума інвестиції означає загальний акціонерний та/або борговий капітал, виділений Інвестором (або контрольованими Інвестором структурами/SPV) у Проект при закритті (або траншами, пропорційно при кожному транші).

**A.4 **Тригер: підлягає сплаті при настанні першої з подій --- (i) підписання обов\'язкової інвестиційної документації, що створює зобов\'язання з фінансування, або (ii) перший капітальний переказ для Проекту.

**B. Пакет B --- Консультаційний ретейнер + Виконання угоди + Платформні угоди**

**B.1 **Ретейнер: 4 000 EUR/місяць, що покриває до 20 годин/місяць консультаційного часу. Невикористані години не переносяться, якщо не погоджено.

**B.2 **Тариф за підбір та виконання угоди: 1,0% від Суми інвестиції для кожного закритого Проекту, підтриманого в рамках цього пакету.

**B.3 **Тариф за Платформну угоду: 0,4% від валової вартості угоди, виконаної через Платформу, де AITA купує (або організовує купівлю) для Інвестора.

**B.4 **Попередньо затверджені витрати: Інвестор відшкодовує попередньо затверджені витрати на сторонні послуги з відбору та аудиту (технічного/юридичного/податкового/страхового/інженерного) лише за попередньою письмовою домовленістю згідно з Додатком 3.

**C. Пакет C --- Спільне інвестування в Проекти, ініційовані AITA (Спеціальні умови)**

**C.1 **Право на участь: застосовується лише до Проектів, ініційованих AITA, запропонованих AITA за окремим Терм-шитом Проекту / документацією SPV.

**C.2 **Мінімальний чек: мінімальний чек Інвестора (або групи Інвесторів) залежить від країни та наявності необхідних ліцензій/дозволів у відповідній юрисдикції; конкретний мінімальний чек визначається в Терм-шиті Проекту.

**C.3 **Управлінський тариф: AITA стягує комерційний управлінський тариф у розмірі 10%, на основі взаємно погодженого ринкового аналізу для відповідної країни/типу проекту, точно визначений у Терм-шиті Проекту.

**C.4 **Інші умови: економіка спільного інвестування (розподіл акцій, привілейований дохід, воотерфол, корпоративне управління, вихід) визначається в Терм-шиті Проекту та документах SPV.

**D. Пакет D --- Банківський/інституційний комплаєнс-скринінг (на Проект)**

**D.1 **Сфера: скринінг структури потенційного інвестора та/або контрагентів на відповідність вимогам банків та інституційних кредиторів (готовність KYC/ПВК, контрольний список документів, відповідність структури, скринінг червоних прапорців) для кожного Проекту.

**D.2 **Тариф: 15 USD за Проект, що пройшов скринінг, підлягає сплаті при доставці результату скринінгу (звіту/результату контрольного списку) через Платформу або електронну пошту.

**D.3 **Обмеження: це послуга з готовності/скринінгу і не гарантує банківського схвалення.

**ДОДАТОК 2 --- БАЗОВИЙ АУДИТ (ВКЛЮЧЕНА СФЕРА ПАКЕТУ A)**

Базовий аудит --- це початковий пакет скринінгу, призначений для зменшення очевидних ризиків та підготовки до більш глибокого due diligence, включаючи (де застосовно до стадії Проекту):

-   Прийом документів та перевірка повноти (правовстановлюючі документи, корпоративні документи/SPV, статус ключових дозволів, статус підключення до мережі, права на землю).

-   Перевірка контрагента (базові сигнали щодо репутації, репутаційні червоні прапорці з відкритих джерел, де законно).

-   Валідація параметрів Проекту (потужність, конфігураційні припущення, перевірка обґрунтованості CAPEX/OPEX на високому рівні).

-   Готовність до стадії (що відсутнє для переходу від попередньої техніко-економічної оцінки до техніко-економічної оцінки / інвестиційного рішення).

-   Реєстр ризиків v1 (основні ризики + рекомендовані дії з пом\'якшення).

Все, що виходить за межи вищезазначеного, є «Додатковою роботою» відповідно до Додатку 3.

**ДОДАТОК 3 --- ПОПЕРЕДНЬО ЗАТВЕРДЖЕНІ ВИТРАТИ ТА БЮДЖЕТУВАННЯ**

**3.1 **Будь-які витрати на сторонні послуги (технічні, юридичні, податкові, страхові, відвідування майданчика, інженерні, спеціалізовані аудити) мають бути попередньо затверджені Інвестором у письмовій формі з: (а) фіксованим граничним бюджетом, або (б) тарифною карткою та максимальною кількістю годин.

**3.2 **AITA може пропонувати постачальників та координувати прокьюремент; Інвестор сплачує рахунки сторонніх постачальників безпосередньо, де можливо, або відшкодовує AITA, якщо AITA сплачує від імені Інвестора (з підтвердженням).

**3.3 **Якщо витрати не затверджено попередньо, Інвестор не зобов\'язаний їх відшкодовувати.

**ДОДАТОК 4 --- ВИБІР ПОСЛУГ (ЧЕКБОКС)**

Інвестор обирає (відзначте):

-   [ ] Пакет A (1,5%)

-   [ ] Пакет B (4 000 EUR/місяць + 1% + 0,4%)

-   [ ] Пакет C (Спільне інвестування; потрібен Терм-шит Проекту)

-   [ ] Пакет D (15 USD за Проект для комплаєнс-скринінгу)


---

# ═══ PROFILE 3 — EPC PARTNER: Partnership Agreement (EN) ═══

**PARTNERSHIP AGREEMENT**
=========================

Platform Use, Lead Distribution, Marketplace, EPC Sales & Open-Book Procurement

This Partnership Agreement (the "Agreement") is entered into on \[Date\] (the "Effective Date") by and between:

1.  AITA WORLD, S.L., a company incorporated under the laws of Spain, with registered office at Sabino Arana, 8-2, 48013 Bilbao, Bizkaia, España, registration no. B75859744 ("Platform"), and

2.  \[Partner Legal Name\], a company incorporated under the laws of \[●\], with registered office at \[●\], registration no. \[●\] ("Partner").

Platform and Partner are collectively the "Parties" and individually a "Party".

**1. Purpose and Scope**
------------------------

1.1. Platform provides Partner access to the Platform and a dedicated Partner Dashboard enabling matching, deal workflow, documentation, tracking, reporting, and monetization calculations.\
1.2. Partner develops and executes the following vertical ("Partner Vertical"): gas turbine and gas engine (reciprocating) power solutions combined with BESS, including related integration, engineering, delivery, commissioning, and service.\
1.3. The Parties cooperate on: (i) lead distribution and execution, (ii) Partner-originated project onboarding and investor recommendation, (iii) distribution of Partner equipment to ecosystem participants, (iv) sale of Partner works/EPC by Platform, and (v) Platform procurement from Partner on an Open-Book basis.

**2. Definitions**
------------------

2.1. Lead means an opportunity/contact (client, investor, EPC, developer, asset owner, offtaker, etc.) recorded in Platform that may result in a transaction.\
2.2. Project means a structured initiative registered in Platform with relevant parameters (site, capacity, CAPEX/OPEX, stage, participants, schedule, etc.).\
2.3. Matching means connecting and coordinating participants through Platform processes, including introductions, workflow, documentation, verification steps, and tracking.\
2.4. Partner Vertical has the meaning set out in Section 1.2.\
2.5. Partner Equipment means equipment offered by Partner within the Partner Vertical (including gas turbine/gas engine units, BESS and components, EMS/SCADA where applicable, and related balance-of-plant items).\
2.6. Partner Works / EPC Services means design, engineering, supply integration, installation, commissioning, O&M/service, and EPC/BoP works performed by Partner (directly or via subcontractors).\
2.7. Profit / Margin means the financial result attributable to a specific transaction, calculated in accordance with Annex A (Margin Rules).\
2.8. Open-Book means a procurement model where Partner discloses cost structure and supporting evidence; Platform applies agreed norm margins to verified cost bases as set out in Annex B (Open-Book Procurement).\
2.9. Fee Base means the base used to calculate the 1.5% / 3% fees for Partner-originated Projects, as set out in Annex C (Fee Base).

**3. Platform Access and Partner Dashboard**
--------------------------------------------

3.1. Partner receives access to:\
(a) functions available to commercial users of Platform (subject to Platform's general terms/policies and selected plan), and\
(b) additional partner features via the Partner Dashboard (lead assignment, status tracking, monetization reporting, commission calculations, and functional requirements board).\
3.2. Partner shall manage Leads/Projects governed by this Agreement through Platform (status updates, key documents, milestones), except where legally impossible---then Partner shall upload a summary and supporting documents to Platform.

**4. Lead Distribution by Platform (Revenue Share)**
----------------------------------------------------

4.1. Leads within Partner Vertical. If Platform assigns a Lead to Partner within the Partner Vertical, Platform is entitled to 50% of Profit/Margin generated by Partner from that Lead.\
4.2. Leads outside Partner Vertical. If Platform assigns to Partner a Lead outside the Partner Vertical and Partner elects to execute it, Platform is entitled to 30% of Profit/Margin from that Lead.\
4.3. Commission Trigger. Platform's share becomes due upon the earliest of:\
(a) Partner receiving any payment related to the transaction; or\
(b) signing of any binding agreement (contract/PO/LOI/framework) that creates a right to revenue for Partner.

**5. Partner-Originated Projects on Platform (Fees)**
-----------------------------------------------------

5.1. Project Matching Fee (1.5%). If Partner registers its own Project on Platform for Matching, Partner shall pay Platform 1.5% of the Fee Base.\
5.2. Direct Investor Recommendation Fee (3%). If Platform makes a direct recommendation of Partner's Project to an investor (intro, submission to investor shortlist, organized investment discussions) and that results in funding/transaction, Partner shall pay Platform 3% of the Fee Base.\
5.3. No stacking by default. Fees under Sections 5.1 and 5.2 shall not be cumulatively applied to the same funding/transaction unless explicitly agreed in writing; by default, the higher applicable fee applies.

**6. Target Leads via Advertising (10% Profit Share)**
------------------------------------------------------

6.1. Partner may request targeted Leads with reduced Platform share of 10% of Profit/Margin, provided Partner funds advertising and pays Platform's partner-rate commercial fee for campaign management/media buying as per an Advertising Order (IO) under Annex D (Advertising Order & Partner Rates).\
6.2. Platform does not guarantee Lead volume unless specific KPIs are set in the IO. Target profile, geography, KPIs, budget, and timeline must be defined in the IO.

**7. Marketplace Distribution of Partner Equipment (30% of Equipment Margin)**
------------------------------------------------------------------------------

7.1. Partner may distribute Partner Equipment through Platform to ecosystem participants (investors, EPCs, developers, asset owners, end customers).\
7.2. Where a sale/supply of Partner Equipment is concluded due to Platform enablement (listing, matching, facilitated communications, negotiations, workflow, documents, verified order), Platform is entitled to 30% of the Equipment Profit/Margin (Annex A).\
7.3. Platform may set listing/data requirements (technical datasheets, certifications, lead times, warranties, Incoterms, payment terms). Partner shall maintain accuracy and updates.

**8. Platform Sale of Partner Works / EPC Services (50/50)**
------------------------------------------------------------

8.1. If Platform sells Partner Works/EPC Services to an end customer (or ecosystem participant) as part of Platform's offering, the Parties shall share the Profit/Margin attributable to Works/EPC 50/50 (Platform 50%, Partner 50%), unless a specific order/SOW specifies otherwise.\
8.2. Platform leads commercial packaging and coordination; Partner is responsible for technical deliverability, timelines, quality, compliance, and subcontractor management (if any).

**9. Platform Procurement from Partner (Open-Book, Norm Margins)**
------------------------------------------------------------------

9.1. If Platform procures from Partner any combination of Partner Equipment and/or Partner Works/EPC Services for onward sale or inclusion in a bundled solution, the Parties apply Open-Book.\
9.2. Partner shall disclose verified costs with supporting documents via Platform and allow reasonable verification.\
9.3. Norm margins payable to Partner on verified cost base (baseline portfolio-average) are:\
(a) Works/EPC: +9% average norm margin on verified works cost base;\
(b) Equipment: +4% average norm margin on verified equipment cost base.\
9.4. Specific orders may adjust norm margins for complexity, guarantees, FX/logistics risks, volume, and schedule, but only if agreed in writing in the relevant order/specification.

**10. Functional Requirements Participation**
---------------------------------------------

10.1. Partner may propose functionality necessary for the Partner Vertical (stage gates, templates, parameter sets, qualification rules, investor package structure).\
10.2. Functional delivery is tracked through Platform tasks and/or a roadmap annex. Material development costs (if any) require a separate written approval.

**11. Reporting, Invoicing, Payment**
-------------------------------------

11.1. Platform provides transaction reporting and fee/commission calculations in Partner Dashboard.\
11.2. Partner shall provide data and documentation reasonably required for Profit/Fee Base calculations and verification.\
11.3. Invoices are payable within 10 (ten) business days unless otherwise stated in the invoice/order.

**12. Confidentiality**
-----------------------

12.1. "Confidential Information" means any non-public information disclosed by a Party (the "Disclosing Party") to the other Party (the "Receiving Party"), whether in written, oral, visual, electronic or any other form, including without limitation: business and technical information, pricing, commercial terms, contacts, deal structures, project parameters, investor materials, product roadmaps, documentation, templates, workflows, source data, analytics, know-how, and Platform operational data. For the avoidance of doubt, all data and outputs contained in the Platform and Partner Dashboard relating to Leads, Projects, participants, performance, conversion, and monetization calculations constitute Platform Confidential Information (except Partner's pre-existing materials uploaded by Partner, which remain Partner Confidential Information).\
12.2. The Receiving Party shall use Confidential Information solely to perform this Agreement and shall not disclose it to any third party except as permitted herein.\
12.3. The Receiving Party may disclose Confidential Information only to its employees, directors, officers, professional advisers, and subcontractors who have a need to know for the purposes of this Agreement and are bound by confidentiality obligations no less protective than those herein.\
12.4. If disclosure is required by law/regulation/court order, the Receiving Party shall (to the extent permitted) provide prompt notice and cooperate to seek protective treatment.\
12.5. Confidential Information excludes information that the Receiving Party can demonstrate: (a) is or becomes public through no breach; (b) was lawfully known before disclosure; (c) is lawfully received from a third party without confidentiality obligations; or (d) is independently developed without use of Confidential Information.\
12.6. Each Party shall maintain commercially reasonable administrative, technical, and organizational measures to protect Confidential Information from unauthorized access or disclosure.\
12.7. Confidentiality obligations apply during the term of this Agreement and survive for three (3) years after termination. Trade secrets remain protected for as long as they remain trade secrets under applicable law.

**13. Intellectual Property and Data**
--------------------------------------

13.1. Platform retains all rights to Platform software, architecture, databases, and interfaces.\
13.2. Partner retains rights to its content/materials and grants Platform a non-exclusive license to use them strictly for executing this Agreement (matching, investor presentation, workflow, documentation).\
13.3. Jointly produced deal data may be used by each Party within the scope of this Agreement; transfer to third parties requires consent except as necessary to close a transaction.

**14. Deal Protection and Non-Circumvention**
---------------------------------------------

14.1. Any Lead assigned by Platform is protected for \[90\] days from assignment, provided Partner actively updates statuses and progresses the Lead in Platform.\
14.2. Partner shall not circumvent Platform regarding Leads/Projects introduced or enabled by Platform. If circumvention is proven, Platform is entitled to the applicable Platform share as if executed via Platform, plus \[●\]% penalty or actual damages to the extent permitted by law.

**15. Non-Compete / Non-Solicitation with Platform (Limited)**
--------------------------------------------------------------

15.1. During the term of this Agreement, Partner shall not build, launch, or operate a product or service that is substantially similar to and directly competitive with Platform, where such product/service is intended to replicate Platform's core function of: (i) multi-party energy project matching, (ii) lead routing and monetization tracking, and (iii) a digital deal workflow system, and is marketed to Platform users/participants as a replacement to Platform.\
15.2. This Section does not restrict Partner from: (a) conducting its ordinary business in the Partner Vertical; (b) using other tools for internal project management; (c) selling equipment and services independently, provided Partner does not misuse Platform Confidential Information or circumvent Platform-introduced Leads.\
15.3. During the term of this Agreement and for twelve (12) months thereafter, Partner shall not knowingly solicit Platform's active ecosystem participants introduced to Partner via Platform to transact outside Platform for substantially similar opportunities where such transactions would avoid fees/shares set out herein.\
15.4. If any part of this Section is unenforceable under applicable law, it shall be reformed to the minimum extent necessary to be enforceable.

**16. Add-On Functionality / Paid Modules**
-------------------------------------------

16.1. Partner's access includes Platform's standard commercial functionality and Partner Dashboard features made available under the selected plan. Any functionality not included in the standard package may be offered as an Add-On Module.\
16.2. Partner may purchase Add-On Modules under a written order/SOW or in-Platform purchase flow. Each Add-On shall define scope, delivery timeline (if applicable), price, payment terms, acceptance criteria, and support/SLA (if applicable).\
16.3. If Partner requests bespoke functionality beyond standard functionality, Platform may provide such development under an SOW with separate pricing. Unless otherwise agreed, Platform retains IP rights in Platform and generic modules, while Partner retains rights to its pre-existing materials.\
16.4. Platform may develop and release additional functionality at its discretion. Add-On purchases do not obligate Platform to provide future features unless expressly included in the relevant SOW/order.

**17. Platform Updates to Terms; Notice (50 Days)**
---------------------------------------------------

17.1. Platform may amend the commercial terms of this Agreement (including monetization percentages, fee bases, and operational policies) to reflect changes in Platform products, market conditions, compliance requirements, or ecosystem rules, provided that Platform gives Partner at least fifty (50) calendar days' prior written notice.\
17.2. Notice may be delivered by: (a) email to Partner's notice address, and/or (b) an in-Platform notification visible in Partner Dashboard. The notice shall specify the effective date and a summary of changes.\
17.3. If Partner materially disagrees with the amended terms, Partner may terminate this Agreement by written notice before the effective date. In such case:\
(a) transactions registered/assigned in Platform before the notice date remain governed by the previous terms until closed or until the end of the protection window (whichever comes first); and\
(b) no new Leads/Projects will be assigned after termination becomes effective.\
17.4. Amendments shall not apply retroactively to amounts already accrued or to deals assigned/registered before the notice date, unless required by law or expressly agreed by the Parties.

**18. Compliance and Responsibility**
-------------------------------------

18.1. Partner is responsible for performance, quality, compliance, certifications, permits, and lawful execution of its deliveries.\
18.2. Platform is not responsible for Partner's commercial outcome except for willful misconduct or gross negligence.

**19. Term and Termination**
----------------------------

19.1. This Agreement starts on the Effective Date and lasts twelve (12) months, auto-renewing for successive 12-month periods unless terminated with thirty (30) days' notice.\
19.2. Termination does not affect accrued payment obligations. Monetization provisions apply to deals initiated before termination and closed within the protection window.

**20. Governing Law and Dispute Resolution**
--------------------------------------------

20.1. Governing law: Spain.\
20.2. Disputes: negotiation first, then Corte de Arbitraje de Madrid (CAM), seat in Madrid, under CAM Arbitration Rules.

**24. Notices**
---------------

24.1. Notices shall be sent to the addresses below (and may also be delivered via in-Platform notification where allowed):\
Platform notice email: \[●\]\
Partner notice email: \[●\]\
Platform address: Sabino Arana, 8-2, 48013 Bilbao, Bizkaia, España\
Partner address: \[●\]

**25. Signatures**
------------------

PLATFORM: AITA WORLD, S.L.\
Name/Title: _______________________\
Signature: ________________________ Date: ___________

PARTNER: \[Partner Legal Name\]\
Name/Title: _______________________\
Signature: ________________________ Date: ___________

**21. Force Majeure**

21.1. Neither Party shall be liable for delay or failure to perform obligations under this Agreement to the extent caused by events beyond its reasonable control, including but not limited to: acts of God, war, terrorism, pandemic, government restrictions, fire, flood, or power outages ("Force Majeure Event").

21.2. The affected Party shall promptly notify the other Party of the Force Majeure Event and use reasonable efforts to mitigate its effects. Obligations are suspended for the duration of the Force Majeure Event.

21.3. If a Force Majeure Event continues for more than sixty (60) days, either Party may terminate this Agreement by written notice without liability.

**22. Language and Controlling Version**

22.1. This Agreement is executed in English. The English version shall be the controlling version. Any translation of this Agreement into any other language is for informational purposes only and shall not affect the interpretation or enforcement of the English version.

**23. Personal Data Protection**

23.1. To the extent any Party processes personal data of individuals (including employees, representatives, and contacts) in connection with this Agreement, each Party shall act as an independent controller and shall comply with all applicable data protection laws, including Regulation (EU) 2016/679 (GDPR) and Ley Orgánica 3/2018 (LOPDGDD) where applicable.

23.2. Each Party warrants that it has an adequate legal basis for any processing of personal data undertaken in connection with this Agreement. The Parties shall cooperate to respond to data subject requests and regulatory inquiries.

**ANNEX A --- Margin / Profit Rules (Default)**

A1. Default (Commission / Revenue Share model).\
Profit/Margin per transaction = Revenue received by Partner (for that transaction) minus Direct Verified Costs.

A2. Direct Verified Costs include (where directly attributable and evidenced): supplier invoices for equipment/materials, logistics & shipping, customs duties, insurance, subcontractors and site labor directly tied to the transaction, bank guarantees / LC / bonding costs directly tied to the deal, third-party referral fees directly tied to that deal.

A3. Exclusions (unless agreed): general overhead, corporate payroll, office costs, unrelated marketing.

A4. Split by component. Where a deal includes both equipment and works, margin shall be split into Equipment Margin and Works/EPC Margin, unless the Parties agree a single blended margin.

**ANNEX B --- Open-Book Procurement Model**
===========================================

B1. Verified Cost Base. Partner provides cost evidence for equipment and works separately.\
B2. Norm Margins (baseline portfolio average).

-   Works/EPC: +9% on verified works cost base;

-   Equipment: +4% on verified equipment cost base.\
    > B3. Verification Right. Platform may request reasonable supporting documents for verification with confidentiality safeguards.\
    > B4. Order-Level Adjustments. Any deviation must be agreed in writing in the relevant order/specification.

**ANNEX C --- Fee Base for 1.5% / 3% Fees (Partner Project Onboarding)**
========================================================================

Select one Fee Base per Project (in the Project Card / order):

Option 1 (Investment / Funding Base): total committed funding amount raised for the Project.\
Option 2 (CAPEX Base): total EPC/CAPEX contract value.\
Option 3 (Contract Value Base): total value of contracts signed with investors/offtakers/customers attributable to the Project.

Default (if not selected): Option 2 (CAPEX Base).

**ANNEX D --- Advertising Order (IO) & Partner Rates (Template)**
=================================================================

D1. Parties: Platform / Partner\
D2. Campaign objective: targeted Leads for Partner Vertical\
D3. Geography / ICP: \[●\]\
D4. Qualification rules: \[●\]\
D5. KPI: \[\# Leads, CPL, conversion targets\]\
D6. Budget:

-   Media spend (paid by Partner): \[●\]

-   Platform partner-rate service fee: \[●\]\
    > D7. Term: \[start/end\]\
    > D8. Monetization: Platform share reduced to 10% of Profit/Margin for Leads generated under this IO (as tracked in Platform).\
    > D9. Acceptance: IO is effective when signed by both Parties or confirmed in Platform.

**ANNEX E --- Monetization Matrix (Summary)**
=============================================

1.  Platform assigns Lead within Partner Vertical → Platform 50% of Profit/Margin

2.  Platform assigns Lead outside Partner Vertical (Partner executes) → Platform 30% of Profit/Margin

3.  Partner registers own Project for Matching → Platform 1.5% of Fee Base

4.  Platform direct investor recommendation for Partner Project → Platform 3% of Fee Base

5.  Advertising-funded targeted Leads (IO signed, budget paid) → Platform 10% of Profit/Margin

6.  Partner Equipment sold via Platform marketplace → Platform 30% of Equipment Margin

7.  Platform sells Partner Works/EPC to customers → 50/50 on Works/EPC Margin

8.  Platform procures from Partner (Open-Book) → Partner norm margins: 9% Works / 4% Equipment (baseline)


---

# ═══ PROFILE 3 — EPC PARTNER: Партнерська угода (UA) ═══

**ПАРТНЕРСЬКА УГОДА**

*Використання Платформи, розподіл лідів, маркетплейс, EPC-продажі та прокьюремент з відкритою книгою*

Цю Партнерську угоду («Угода») укладено \[Дата\] («Дата набрання чинності») між:

**AITA WORLD, S.L.**, компанія, зареєстрована відповідно до законодавства Іспанії, із зареєстрованим офісом за адресою: Sabino Arana, 8-2, 48013 Bilbao, Bizkaia, Іспанія, реєстраційний номер B75859744 («Платформа»),

**\[Юридична назва Партнера\]**, компанія, зареєстрована відповідно до законодавства \[●\], із зареєстрованим офісом за адресою: \[●\], реєстраційний номер \[●\] («Партнер»).

Платформа та Партнер разом --- «Сторони», кожна окремо --- «Сторона».

**1. Предмет та сфера застосування**

**1.1 **Платформа надає Партнеру доступ до Платформи та виділеного Партнерського дашборду, що забезпечують підбір, workflow угоди, документообіг, відстеження, звітність та розрахунки монетизації.

**1.2 **Партнер розробляє та реалізує наступну вертикаль («Вертикаль Партнера»): рішення на базі газових турбін та газових двигунів (поршневих) у поєднанні з BESS, включаючи відповідну інтеграцію, інжиніринг, постачання, введення в експлуатацію та сервіс.

**1.3 **Сторони співпрацюють у: (i) розподілі та виконанні лідів, (ii) онбордингу Проектів, ініційованих Партнером, та рекомендації інвесторів, (iii) дистрибуції обладнання Партнера учасникам екосистеми, (iv) продажі Платформою робіт/EPC Партнера, та (v) прокьюременті Платформи від Партнера на умовах відкритої книги.

**2. Визначення**

**2.1 **Лід --- можливість/контакт (клієнт, інвестор, EPC, розробник, власник активу, offtake-партнер тощо), зафіксований на Платформі, що може призвести до угоди.

**2.2 **Проект --- структурована ініціатива, зареєстрована на Платформі з відповідними параметрами (майданчик, потужність, CAPEX/OPEX, стадія, учасники, графік тощо).

**2.3 **Підбір --- з\'єднання та координація учасників через процеси Платформи, включаючи представлення, workflow, документообіг, кроки верифікації та відстеження.

**2.4 **Вертикаль Партнера --- значення відповідно до Розділу 1.2.

**2.5 **Обладнання Партнера --- обладнання, запропоноване Партнером у межах Вертикалі Партнера (включаючи агрегати газових турбін/газових двигунів, BESS та компоненти, EMS/SCADA за необхідності та пов\'язані BoP-елементи).

**2.6 **Роботи/EPC-послуги Партнера --- проектування, інжиніринг, постачання інтеграції, монтаж, введення в експлуатацію, ТО/сервіс та EPC/BoP-роботи, що виконуються Партнером (безпосередньо або через субпідрядників).

**2.7 **Прибуток/Маржа --- фінансовий результат, що відноситься до конкретної угоди, розрахований відповідно до Додатку A (Правила маржі).

**2.8 **Відкрита книга --- модель прокьюременту, де Партнер розкриває структуру витрат та підтверджуючі документи; Платформа застосовує погоджені нормативні маржі до верифікованої бази витрат відповідно до Додатку B.

**2.9 **База тарифу --- база, що використовується для розрахунку тарифів 1,5% / 3% для Проектів, ініційованих Партнером, відповідно до Додатку C.

**3. Доступ до Платформи та Партнерський дашборд**

**3.1 **Партнер отримує доступ до: (а) функцій, доступних комерційним користувачам Платформи (відповідно до загальних умов/політик Платформи та обраного тарифного плану), та (б) додаткових партнерських функцій через Партнерський дашборд (призначення лідів, відстеження статусу, звіти монетизації, розрахунки комісій та дошка функціональних вимог).

**3.2 **Партнер управляє Лідами/Проектами, що регулюються цією Угодою, через Платформу (оновлення статусу, ключові документи, віхи), крім випадків, коли це юридично неможливо --- тоді Партнер завантажує зведення та підтверджуючі документи на Платформу.

**4. Розподіл лідів Платформою (Розподіл доходу)**

**4.1 **Ліди у межах Вертикалі Партнера. Якщо Платформа призначає Лід Партнеру в межах Вертикалі Партнера, Платформа має право на 50% Прибутку/Маржі, отриманої Партнером від цього Ліду.

**4.2 **Ліди поза межами Вертикалі Партнера. Якщо Платформа призначає Партнеру Лід поза межами Вертикалі Партнера і Партнер обирає його виконання, Платформа має право на 30% Прибутку/Маржі від цього Ліду.

**4.3 **Тригер комісії. Частка Платформи підлягає сплаті при настанні першої з подій: (а) отримання Партнером будь-якого платежу, пов\'язаного з угодою; або (б) підписання будь-якого обов\'язкового договору (контракт/ЗН/ЛНН/рамкова угода), що створює право на дохід Партнера.

**5. Проекти, ініційовані Партнером, на Платформі (Тарифи)**

**5.1 **Тариф за підбір Проекту (1,5%). Якщо Партнер реєструє власний Проект на Платформі для Підбору, Партнер сплачує Платформі 1,5% від Бази тарифу.

**5.2 **Тариф за пряму рекомендацію Інвестору (3%). Якщо Платформа робить пряму рекомендацію Проекту Партнера інвестору (представлення, подача до шорт-листа інвестора, організовані інвестиційні переговори) і це призводить до фінансування/угоди, Партнер сплачує Платформі 3% від Бази тарифу.

**5.3 **Відсутність подвійного нарахування за замовчуванням. Тарифи за Розділами 5.1 та 5.2 не застосовуються кумулятивно до одного фінансування/угоди, якщо прямо не погоджено в письмовій формі; за замовчуванням застосовується вищий тариф.

**6. Цільові ліди через рекламу (10% частка прибутку)**

**6.1 **Партнер може запросити цільові Ліди зі зниженою часткою Платформи 10% від Прибутку/Маржі, за умови, що Партнер фінансує рекламу та сплачує комерційний тариф Платформи за управління кампанією/медіабаінг відповідно до Замовлення на розміщення (IO) за Додатком D.

**6.2 **Платформа не гарантує обсяг лідів, якщо в IO не встановлено конкретних KPI. Цільовий профіль, географія, KPI, бюджет та строки повинні бути визначені в IO.

**7. Маркетплейс-дистрибуція Обладнання Партнера (30% від маржі обладнання)**

**7.1 **Партнер може дистрибутувати Обладнання Партнера через Платформу учасникам екосистеми (інвесторам, EPC-підрядникам, розробникам, власникам активів, кінцевим клієнтам).

**7.2 **Якщо продаж/постачання Обладнання Партнера відбулася завдяки сприянню Платформи (розміщення, підбір, полегшена комунікація, переговори, workflow, документи, верифіковане замовлення), Платформа має право на 30% від Прибутку/Маржі обладнання (Додаток A).

**7.3 **Платформа може встановлювати вимоги до розміщення/даних (технічні специфікації, сертифікації, терміни постачання, гарантії, Інкотермс, умови оплати). Партнер підтримує точність та оновлення.

**8. Продаж Платформою Робіт/EPC-послуг Партнера (50/50)**

**8.1 **Якщо Платформа продає Роботи/EPC-послуги Партнера кінцевому клієнту (або учаснику екосистеми) як частину пропозиції Платформи, Сторони розподіляють Прибуток/Маржу, що відноситься до Робіт/EPC, 50/50 (Платформа 50%, Партнер 50%), якщо в конкретному замовленні/ТЗ не вказано інше.

**8.2 **Платформа керує комерційним пакетуванням та координацією; Партнер відповідає за технічну виконуваність, строки, якість, відповідність нормативним вимогам та управління субпідрядниками (за необхідності).

**9. Прокьюремент Платформи від Партнера (Відкрита книга, нормативні маржі)**

**9.1 **Якщо Платформа закуповує у Партнера будь-яку комбінацію Обладнання Партнера та/або Робіт/EPC-послуг Партнера для перепродажу або включення у бандловане рішення, Сторони застосовують Відкриту книгу.

**9.2 **Партнер розкриває верифіковані витрати з підтверджуючими документами через Платформу та дозволяє обґрунтовану верифікацію.

**9.3 **Нормативні маржі, що виплачуються Партнеру на верифіковану базу витрат (базовий середньопортфельний показник): (а) Роботи/EPC: +9% середня нормативна маржа на верифіковану базу витрат на роботи; (б) Обладнання: +4% середня нормативна маржа на верифіковану базу витрат на обладнання.

**9.4 **Конкретні замовлення можуть коригувати нормативні маржи з урахуванням складності, гарантій, ризиків FX/логістики, обсягу та графіку, але лише за письмовою домовленістю у відповідному замовленні/специфікації.

**10. Участь у функціональних вимогах**

**10.1 **Партнер може пропонувати функціональність, необхідну для Вертикалі Партнера (стадійні ворота, шаблони, набори параметрів, правила кваліфікації, структура інвестиційного пакету).

**10.2 **Функціональна реалізація відстежується через задачи Платформи та/або дорожньо-картний додаток. Суттєві витрати на розробку (за наявності) потребують окремого письмового схвалення.

**11. Звітність, виставлення рахунків, оплата**

**11.1 **Платформа надає звіти по угодах та розрахунки тарифів/комісій у Партнерському дашборді.

**11.2 **Партнер надає дані та документацію, обґрунтовано необхідні для розрахунків Прибутку/Бази тарифу та верифікації.

**11.3 **Рахунки підлягають оплаті протягом 10 (десяти) робочих днів, якщо в рахунку/замовленні не зазначено інше.

**12. Конфіденційність**

**12.1 **«Конфіденційна інформація» означає будь-яку непублічну інформацію, розкриту Стороною («Сторона, що розкриває») іншій Стороні («Сторона, що отримує»), у будь-якій формі, включаючи: бізнес та технічну інформацію, ціноутворення, комерційні умови, контакти, структури угод, параметри проектів, матеріали для інвесторів, дорожні карти продуктів, документацію, шаблони, workflow, вихідні дані, аналітику, ноу-хау та операційні дані Платформи.

**12.2 **Сторона, що отримує, використовуватиме Конфіденційну інформацію виключно для виконання цієї Угоди та не розкриватиме її третім особам, крім випадків, передбачених цією Угодою.

**12.3 **Зобов\'язання щодо конфіденційності діють протягом строку дії цієї Угоди та зберігаються протягом трьох (3) років після припинення. Комерційна таємниця залишається захищеною, доки вона залишається комерційною таємницею відповідно до застосовного законодавства.

**13. Інтелектуальна власність та дані**

**13.1 **Платформа зберігає всі права на програмне забезпечення Платформи, архітектуру, бази даних та інтерфейси.

**13.2 **Партнер зберігає права на власний контент/матеріали та надає Платформі невиключну ліцензію на їх використання виключно для виконання цієї Угоди.

**13.3 **Дані угод, спільно отримані, можуть використовуватися кожною Стороною в межах цієї Угоди; передача третім особам потребує згоди, крім випадків, необхідних для закриття угоди.

**14. Захист угод та незалучення третіх сторін**

**14.1 **Будь-який Лід, призначений Платформою, захищається протягом \[90\] днів з дати призначення, за умови, що Партнер активно оновлює статуси та просуває Лід на Платформі.

**14.2 **Партнер не має права обходити Платформу щодо Лідів/Проектів, представлених або забезпечених Платформою. У разі доведення факту обходу Платформа має право на відповідну частку, як якби угода була виконана через Платформу, плюс штраф або фактичні збитки в межах, дозволених законом.

**15. Обмежена некомпетиція / Незалучення щодо Платформи**

**15.1 **Протягом строю дії цієї Угоди Партнер не має права будувати, запускати або управляти продуктом або послугою, що суттєво аналогічна та прямо конкурує з Платформою, де такий продукт/послуга призначений(а) для відтворення основних функцій Платформи: (i) багатосторонній підбір енергетичних проектів, (ii) маршрутизація лідів та відстеження монетизації, (iii) цифрова система workflow угоди.

**15.2 **Цей Розділ не обмежує Партнера у: (а) здійсненні звичайної діяльності у Вертикалі Партнера; (б) використанні інших інструментів для внутрішнього управління проектами; (в) продажу обладнання та послуг самостійно, за умови, що Партнер не зловживає Конфіденційною інформацією Платформи або не обходить Ліди, представлені Платформою.

**15.3 **Протягом строю дії цієї Угоди та дванадцяти (12) місяців після неї Партнер не має права свідомо залучати активних учасників екосистеми Платформи, представлених Партнеру через Платформу, для здійснення угод поза Платформою щодо аналогічних можливостей.

**17. Оновлення умов Платформою; Повідомлення (50 днів)**

**17.1 **Платформа може вносити зміни до комерційних умов цієї Угоди за умови надання Партнеру попереднього письмового повідомлення не менше ніж за п\'ятдесят (50) календарних днів.

**17.2 **Якщо Партнер суттєво не погоджується зі зміненими умовами, Партнер може розірвати цю Угоду письмовим повідомленням до дати набрання чинності.

**17.3 **Зміни не застосовуються ретроспективно до вже нарахованих сум або угод, призначених/зареєстрованих до дати повідомлення, якщо це не вимагається законом або прямо не погоджено Сторонами.

**18. Відповідальність та виконання**

**18.1 **Партнер відповідає за виконання, якість, відповідність нормативним вимогам, сертифікації, дозволи та правомірне виконання своїх поставок.

**18.2 **Платформа не несе відповідальності за комерційний результат Партнера, крім випадків умисного порушення або грубої необережності.

**19. Строк та припинення**

**19.1 **Ця Угода починається з Дати набрання чинності та діє дванадцять (12) місяців, автоматично поновлюючись на наступні 12-місячні періоди, якщо вона не припинена з повідомленням за тридцять (30) днів.

**19.2 **Припинення не впливає на нараховані зобов\'язання з оплати. Положення про монетизацію застосовуються до угод, ініційованих до припинення та закритих протягом захисного вікна.

**20. Застосовне право та вирішення спорів**

**20.1 **Застосовне право: Іспанія.

**20.2 **Спори: спочатку переговори, потім Мадридський арбітражний суд (CAM), місце проведення --- Мадрид, відповідно до Арбітражного регламенту CAM.

**24. Повідомлення**

**24.1 **Повідомлення надсилаються на адреси нижче (і можуть також доставлятися через сповіщення на Платформі, де дозволено):

Email Платформи: \[●\]

Email Партнера: \[●\]

Адреса Платформи: Sabino Arana, 8-2, 48013 Bilbao, Bizkaia, Іспанія

Адреса Партнера: \[●\]

**25. Підписи**

+---------------------------------------------------------------------------------------+---------------------------------------------------------------------------------------+
| **ПЛАТФОРМА: AITA WORLD, S.L.**                                                       | **ПАРТНЕР: \[Юридична назва Партнера\]**                                              |
|                                                                                       |                                                                                       |
| Ім\'я/Посада: _______________________                          | Ім\'я/Посада: _______________________                          |
|                                                                                       |                                                                                       |
| Підпис: ________________________ Дата: ___________ | Підпис: ________________________ Дата: ___________ |
+---------------------------------------------------------------------------------------+---------------------------------------------------------------------------------------+

**ДОДАТОК A --- ПРАВИЛА МАРЖІ/ПРИБУТКУ (ЗА ЗАМОВЧУВАННЯМ)**

**A1 **За замовчуванням (модель комісії / розподілу доходу). Прибуток/Маржа за угодою = Дохід, отриманий Партнером (за цією угодою) мінус Прямі верифіковані витрати.

**A2 **Прямі верифіковані витрати включають (де прямо відносяться та підтверджені): рахунки постачальників за обладнання/матеріали, логістику та доставку, мита, страхування, субпідрядників та майданчиковий персонал, безпосередньо пов\'язаних з угодою, витрати на банківські гарантії/акредитиви/бондінг, безпосередньо пов\'язані з угодою, комісії сторонніх посередників, безпосередньо пов\'язані з цією угодою.

**A3 **Виключення (якщо не погоджено): загальні накладні витрати, корпоративний фонд оплати праці, офісні витрати, невідповідний маркетинг.

**A4 **Розподіл за компонентами. Якщо угода включає і обладнання, і роботи, маржа розподіляється на Маржу обладнання та Маржу Робіт/EPC, якщо Сторони не погоджуються на єдину змішану маржу.

**ДОДАТОК B --- МОДЕЛЬ ПРОКЬЮРЕМЕНТУ З ВІДКРИТОЮ КНИГОЮ**

**B1 **Верифікована база витрат. Партнер надає підтвердження витрат на обладнання та роботи окремо.

**B2 **Нормативні маржі (базовий середньопортфельний показник). Роботи/EPC: +9% на верифіковану базу витрат на роботи; Обладнання: +4% на верифіковану базу витрат на обладнання.

**B3 **Право верифікації. Платформа може запитувати обґрунтовані підтверджуючі документи для верифікації із заходами конфіденційності.

**B4 **Коригування на рівні замовлення. Будь-яке відхилення має бути погоджено в письмовій формі у відповідному замовленні/специфікації.

**ДОДАТОК C --- БАЗА ТАРИФУ ДЛЯ 1,5% / 3% (ОНБОРДИНГ ПРОЕКТУ ПАРТНЕРА)**

Оберіть одну Базу тарифу для кожного Проекту (у Картці Проекту / замовленні):

-   Варіант 1 (База інвестування/фінансування): загальна сума committed фінансування, залученого для Проекту.

-   Варіант 2 (База CAPEX): загальна вартість EPC/CAPEX-контракту.

-   Варіант 3 (База вартості контракту): загальна вартість контрактів, підписаних з інвесторами/offtake-партнерами/клієнтами, що відносяться до Проекту.

-   За замовчуванням (якщо не обрано): Варіант 2 (База CAPEX).

**ДОДАТОК D --- ЗАМОВЛЕННЯ НА РОЗМІЩЕННЯ (IO) ТА ТАРИФИ ПАРТНЕРА (ШАБЛОН)**

**D1 **Сторони: Платформа / Партнер

**D2 **Мета кампанії: цільові ліди для Вертикалі Партнера

**D3 **Географія / ICP: \[●\]

**D4 **Правила кваліфікації: \[●\]

**D5 **KPI: \[кількість лідів, вартість за лід, цілі конверсії\]

**D6 **Бюджет: Медійні витрати (сплачує Партнер): \[●\]; Тариф Платформи (партнерська ставка): \[●\]

**D7 **Строк: \[початок/кінець\]

**D8 **Монетизація: частка Платформи знижується до 10% Прибутку/Маржі для Лідів, згенерованих у рамках цього IO (відстежується на Платформі).

**D9 **Прийняття: IO набирає чинності після підписання обома Сторонами або підтвердження на Платформі.

**ДОДАТОК E --- МАТРИЦЯ МОНЕТИЗАЦІЇ (ЗВЕДЕННЯ)**

  ----------------------------------------------------------------- ------------------------------------------------------
  **Сценарій**                                                      **Частка Платформи**
  Платформа призначає Лід у межах Вертикалі Партнера                50% Прибутку/Маржі
  Платформа призначає Лід поза межами Вертикалі (Партнер виконує)   30% Прибутку/Маржі
  Партнер реєструє власний Проект для Підбору                       1,5% від Бази тарифу
  Пряма рекомендація Платформи інвестору для Проекту Партнера       3% від Бази тарифу
  Ліди з рекламним фінансуванням (IO підписано, бюджет сплачено)    10% Прибутку/Маржі
  Обладнання Партнера продано через маркетплейс Платформи           30% Маржі обладнання
  Платформа продає Роботи/EPC Партнера клієнтам                     50/50 від Маржі Робіт/EPC
  Платформа закуповує від Партнера (Відкрита книга)                 Нормативні маржі Партнера: 9% Роботи / 4% Обладнання
  ----------------------------------------------------------------- ------------------------------------------------------


---

# ═══ PROFILE 4 — DEAL DELIVERY TEAM: Agreement (EN) ═══

**AITA DEAL DELIVERY TEAM AGREEMENT**
-------------------------------------

**(Digital-Only / Full Support / Team Pool 30% / Self-Governed Roles & KPIs / NDA & Restrictions)**

**Date:** \[●\] 2026\
**Place:** Spain, Bilbao

### **1. Parties**

1.  **Ivan Shumlianskyi** --- Founder of the Group, Co-Founder of AITA (the **"Founder"**).

2.  **Dmytro Mekhed** --- CEO of AITA, Co-Founder of AITA (the **"CEO"**).

3.  **Delivery Team Members** (each individually and jointly the **"Team"**), listed in **Appendix T1 (Team Roster)**:

-   \[Name, ID/Passport, email\]

-   \[Name, ID/Passport, email\]

-   ...

Collectively, the **"Parties"**.

### **2. Purpose**

2.1. This Agreement defines the engagement rules for the **Delivery Team** to execute the **Deal** described in **Appendix A (Deal Passport)**, including: full support scope, mandatory execution through the AITA Platform, governance rules, KPI obligations, and allocation of a **Team Profit Pool** equal to **30% of the Profit of the Deal**.\
2.2. The Team operates as a self-governed delivery unit: internal roles, workload split, and internal distribution of the Team Profit Pool are decided by the Team and recorded in AITA.

### **3. Definitions**

3.1. **Deal** --- the commercial transaction(s) defined in **Appendix A (Deal Passport)**, including all related contracts, orders, milestones, deliverables and payments.\
3.2. **AITA Platform** --- the mandatory digital workspace for execution and evidence: tasks, documents, approvals, versioning, KPI dashboards, logs and analytics.\
3.3. **Profit of the Deal** --- calculated under **Appendix B (Profit Formula)**, including agreed adjustments for returns, penalties, third-party commissions and reserves.\
3.4. **Team Profit Pool** --- **30% of the Profit of the Deal** allocated to the Team under this Agreement.\
3.5. **Team Distribution Rules** --- internal allocation rules decided by the Team and recorded in AITA (Appendix T2).\
3.6. **Approval Gates** --- decisions requiring Founder/CEO approval recorded in AITA (Section 7).

### **4. Mandatory Digital-Only execution**

4.1. The Parties agree that **all activities and results** under this Deal must be performed and recorded in the **AITA Platform** and be visible in the unified Deal context, including:

-   stakeholder mapping, introductions, meeting scheduling, negotiation logs;

-   offers, drafts, versions, approvals;

-   task tracking, deadlines, owners;

-   product requirements, specs, tickets, releases;

-   KPI dashboards, pilot evidence, final analytics pack.\
    > 4.2. Deliverables or actions not recorded in AITA may be treated as **non-verifiable** for compensation purposes unless explicitly validated by Founder/CEO in AITA.

### **5. Team Scope of Work --- Full Support**

The Team commits to provide **full support** for the Deal, including, without limitation:

5.1. **Commercial & Negotiation Support**

-   preparation of negotiation materials; agendas, minutes, follow-ups;

-   maintaining deal momentum and decision gates;

-   coordination with counterparties and internal stakeholders.

5.2. **Contracts & Legal Pack**

-   drafting and negotiating contract terms (within Approval Gates);

-   maintaining a versioned contract repository;

-   signature workflow coordination and consistency checks.

5.3. **Product & Functional Delivery**

-   defining and building required AITA platform functionality for this Deal;

-   integrations, dashboards, analytics, reporting deliverables;

-   internal QA and release management.

5.4. **Delivery Operations**

-   supplier/EPC/O&M coordination (if applicable);

-   SLA/support processes; incident handling (if applicable);

-   post-go-live support where required by the Deal.

**5A. Definition of Full Support (Mandatory Artifacts, SLA, DoD)**
------------------------------------------------------------------

### **5A.1 Mandatory artifacts (all inside AITA Platform)**

The Team must create and keep updated the following artifacts for the Deal:

a\) **Deal Workspace** (structure, access, versioning).\
b) **Stakeholder Map** (decision makers, influencers, intro chain).\
c) **Deal Timeline & Decision Gates** (phases, proof required per gate).\
d) **Negotiation Log** (meetings, minutes, commitments, next steps).\
e) **Offer & Commercial Pack** (value proposition, scope, assumptions, pricing corridors via Approval Gates).\
f) **Contract Pack Repository** (all versions/redlines/approvals history).\
g) **Product/Functional Backlog** (requirements → tickets → releases).\
h) **KPI Dashboard** (joint KPIs + pilot evidence; see Section 5B).\
i) **Risk Register** (risks, mitigations, owner, escalation).\
j) **Board-grade Outcome Pack** (scale/no-scale or closure decision pack).

### **5A.2 Minimum SLA (response & discipline)**

-   **Response SLA:** for critical Deal items --- Team response in AITA within **4 hours** on business days.

-   **Meeting Minutes SLA:** minutes + decisions + next steps within **12 hours** after a meeting/call.

-   **Follow-up SLA:** external follow-up within **24 hours** after a meeting (unless otherwise agreed).

-   **Escalation SLA:** if a risk threatens a decision gate --- escalate in AITA to Founder/CEO within **24 hours**.

-   **Versioning rule:** any offer/contract changes must be versioned in AITA; "latest version" must be clearly marked.

### **5A.3 Definition of Done (DoD) for key deliverables**

-   **Commercial Pack DoD:** value proposition + scope + assumptions + pricing corridor + approval log.

-   **Contract Pack DoD:** agreed text + redlines history + approvals + signature workflow + final signed copies.

-   **Functional Delivery DoD:** requirements → tickets → release → verification → KPI dashboard updated.

-   **Pilot DoD (if applicable):** baseline data → pilot passport/pre-FEED → launch → KPI evidence → final report.

**5B. Joint Deal KPIs (Mandatory)**
-----------------------------------

### **5B.1 KPI Matrix is mandatory**

Within **5 business days** of signing (or Deal start --- whichever comes first), the Team must create a **joint KPI matrix** and publish it as **KPI Dashboard** in AITA.

### **5B.2 Minimum KPI structure (4 blocks)**

The KPI matrix must include at minimum:

1.  **Deal Progress KPIs\
    > **

-   confirmed decision-makers coverage;

-   decision gate completion (%);

-   average time-to-next-step.

2.  **Negotiation & Contract KPIs\
    > **

-   key meetings count + outcomes;

-   offer/contract version status and cycle time;

-   signature readiness score.

3.  **Product/Delivery KPIs\
    > **

-   backlog planned vs done;

-   release cycle time;

-   data/monitoring coverage.

4.  **Outcome/Pilot KPIs (if applicable)\
    > **

-   operational KPI (uptime/availability/session success etc. per Deal Passport);

-   economic effect proxy (savings/€ per site, profit proxy);

-   readiness-to-scale score.

### **5B.3 Targets and thresholds**

For key KPIs the Team must define **minimum acceptable / target / stretch** values where feasible, to make "scale/no-scale" decisions objective.

### **5B.4 KPI cadence**

-   **Weekly KPI review** inside AITA (status update, blockers, corrective actions).

-   **One owner per KPI** assigned by the Team and recorded in AITA.

### **5B.5 KPI changes**

Any KPI change must be versioned in AITA with a stated reason.

**6. Team Self-Governance (roles, decisions, internal distribution)**
---------------------------------------------------------------------

6.1. **Roles:** the Team independently assigns internal roles (e.g., Negotiation Lead, Legal Coordinator, Product Owner, Delivery Ops, Data/KPI Lead, etc.) and records them in AITA.\
6.2. **Decision-making:** unless the Team records another rule in AITA, Team operational decisions are taken by **simple majority** of active Team members.\
6.3. **Internal distribution:** the Team distributes the Team Profit Pool among members at its discretion and records the rules in **Appendix T2** in AITA (including changes, effective dates).\
6.4. **Internal disputes:** Founder/CEO are not responsible for internal distribution disputes if Team Distribution Rules exist in AITA and were followed.

**7. Governance and Approval Gates (Founder/CEO)**
--------------------------------------------------

7.1. The Team cannot bind the Group/AITA legally or financially without approvals recorded in AITA, including:

-   signing contracts or committing final commercial terms/pricing corridors;

-   issuing warranties/guarantees;

-   bank/financial commitments;

-   public statements on behalf of AITA/Group.\
    > 7.2. Signing authority is granted only via separate mandates/powers of attorney and within defined limits.

**8. Compensation: Team Profit Pool (30%)**
-------------------------------------------

8.1. The Team is entitled to **Team Profit Pool = 30% of the Profit of the Deal**, calculated under Appendix B.\
8.2. The Team Profit Pool accrues as profit is realized and may be paid pro-rata, subject to reserves defined in Appendix B.\
8.3. Allocation among Team members is governed by Team Distribution Rules (Appendix T2) recorded in AITA.

**9. Roster management**
------------------------

9.1. Team roster is defined in Appendix T1 and may be updated only via AITA with version control and Founder/CEO acknowledgment.\
9.2. A leaving member retains rights only as defined by Team Distribution Rules recorded in AITA and only for realized profit, unless the Team rules state otherwise.

**10. Confidentiality (Strict NDA)**
------------------------------------

10.1. Each Team member must keep confidential all non-public information about the Deal, counterparties, negotiations, pricing, profit, product logic, documents, and AITA internal materials/processes.\
10.2. No disclosure, forwarding, publishing, or use for personal benefit without Founder/CEO written approval in AITA.\
10.3. Material breach may result in immediate removal and forfeiture of unpaid compensation, plus liability for damages.

**11. Non-circumvention, non-solicitation, limited non-competition (5 years)**
------------------------------------------------------------------------------

11.1. During the term and for **5 years** after termination, each Team member agrees to:

-   **non-circumvent:** not bypass the Parties to capture the Deal, contacts, suppliers or execution chain;

-   **non-solicit:** not poach employees, agents, contractors or clients introduced via the Deal;

-   **limited non-competition:** not execute directly competing work with the same key counterparties/locations/portfolio defined in Appendix A/E, to the extent enforceable under applicable law.\
    > 11.2. Exact scope may be maintained as a versioned appendix in AITA.

**12. Term and termination**
----------------------------

12.1. Effective from signature until Deal completion and settlement, unless terminated earlier.\
12.2. Founder/CEO may remove a Team member immediately for material breach (NDA breach, circumvention, sabotage, systematic Digital-Only violations).\
12.3. Upon removal for breach, unpaid compensation for that member is forfeited; the Team may reallocate per Team Distribution Rules.

**13. Governing law and disputes**
----------------------------------

13.1. Governing law: Spain, unless otherwise agreed.\
13.2. Disputes: 10 days negotiation, then Corte de Arbitraje de Madrid (CAM), seat in Madrid, under CAM Arbitration Rules.

**14. Force Majeure**

14.1. Neither Party shall be liable for delay or failure to perform obligations under this Agreement to the extent caused by events beyond its reasonable control, including but not limited to: acts of God, war, terrorism, pandemic, government restrictions, fire, flood, or power outages ("Force Majeure Event").

14.2. The affected Party shall promptly notify the other Party of the Force Majeure Event and use reasonable efforts to mitigate its effects. Obligations are suspended for the duration of the Force Majeure Event.

14.3. If a Force Majeure Event continues for more than sixty (60) days, either Party may terminate this Agreement by written notice without liability.

**15. Language and Controlling Version**

15.1. This Agreement is executed in English. The English version shall be the controlling version. Any translation of this Agreement into any other language is for informational purposes only and shall not affect the interpretation or enforcement of the English version.

**16. Personal Data Protection**

16.1. To the extent any Party processes personal data of individuals (including employees, representatives, and contacts) in connection with this Agreement, each Party shall act as an independent controller and shall comply with all applicable data protection laws, including Regulation (EU) 2016/679 (GDPR) and Ley Orgánica 3/2018 (LOPDGDD) where applicable.

16.2. Each Party warrants that it has an adequate legal basis for any processing of personal data undertaken in connection with this Agreement. The Parties shall cooperate to respond to data subject requests and regulatory inquiries.

**17. Final provisions**

17.1. AITA-recorded approvals, versioned updates, KPI dashboards, and distribution rules are recognized as written evidence.\
14.2. Changes to this Agreement require a signed addendum or an AITA-recorded decision approved by Founder and CEO.

**Appendices (maintained in AITA)**
===================================

**Appendix A --- Deal Passport\
** **Appendix B --- Profit Formula & Reserves\
** **Appendix T1 --- Team Roster (Members List)\
** **Appendix T2 --- Team Distribution Rules (Self-Governed)\
** *(Optional)* **Appendix E --- Restriction Map (Counterparties / Locations / Scope)**

**Signatures**
--------------

**Ivan Shumlianskyi** __________________ Date: ***/***/2026\
**Dmytro Mekhed** ______________________ Date: ***/***/2026

**Team Member:** ________________________ Name: \[●\] Date: ***/***/2026\
**Team Member:** ________________________ Name: \[●\] Date: ***/***/2026\
**Team Member:** ________________________ Name: \[●\] Date: ***/***/2026


---

# ═══ PROFILE 4 — DEAL DELIVERY TEAM: Договір (UA) ═══

**УГОДА З КОМАНДОЮ ВИКОНАННЯ УГОДИ**

*(Лише цифровий формат / Повна підтримка / Командний пул 30% / Самокеровані ролі та KPI / NDA та обмеження)*

Дата: \[●\] 2026 р. \| Місце: Іспанія, Більбао

**1. Сторони**

Іван Шумлянський --- Засновник Групи, Співзасновник AITA (\"Засновник\").

Дмитро Мехед --- Генеральний директор AITA, Співзасновник AITA (\"Генеральний директор\").

Члени команди виконання (кожен окремо та спільно --- \"Команда\"), зазначені в Додатку T1 (Реєстр команди):

\[Ім\'я, ІД/Паспорт, електронна пошта\]

\[Ім\'я, ІД/Паспорт, електронна пошта\]

...

Спільно --- \"Сторони\".

**2. Мета**

**2.1 **Ця Угода визначає правила залучення Команди виконання для реалізації Угоди, описаної в Додатку А (Паспорт угоди), включаючи: повний обсяг підтримки, обов\'язкове виконання через Платформу AITA, правила управління, зобов\'язання щодо KPI та розподіл Командного пулу прибутку у розмірі 30% від Прибутку від угоди.

**2.2 **Команда функціонує як самокероване підрозділ виконання: внутрішні ролі, розподіл навантаження та внутрішній розподіл Командного пулу прибутку визначаються Командою та фіксуються в AITA.

**3. Визначення**

**3.1 **Угода --- комерційна(-і) транзакція(-ії), визначена(-і) в Додатку А (Паспорт угоди), включаючи всі пов\'язані договори, замовлення, етапи, результати та платежі.

**3.2 **Платформа AITA --- обов\'язковий цифровий робочий простір для виконання та фіксації: завдань, документів, затверджень, версіонування, панелей KPI, журналів і аналітики.

**3.3 **Прибуток від угоди --- розраховується згідно з Додатком Б (Формула прибутку), включаючи узгоджені коригування на повернення, штрафи, комісії третіх сторін і резерви.

**3.4 **Командний пул прибутку --- 30% Прибутку від угоди, виділених Команді за цією Угодою.

**3.5 **Правила внутрішнього розподілу Команди --- внутрішні правила розподілу, визначені Командою та зафіксовані в AITA (Додаток T2).

**3.6 **Ворота затвердження --- рішення, що вимагають затвердження Засновника/Генерального директора, зафіксовані в AITA (Розділ 7).

**4. Обов\'язкове виконання лише у цифровому форматі**

**4.1 **Сторони погоджуються, що всі дії та результати за цією Угодою повинні виконуватися та фіксуватися на Платформі AITA та бути видимими у єдиному контексті Угоди, включаючи:

-   картографування зацікавлених сторін, знайомства, планування зустрічей, журнали переговорів;

-   пропозиції, чернетки, версії, затвердження;

-   відстеження завдань, дедлайни, відповідальні;

-   вимоги до продукту, специфікації, тікети, релізи;

-   панелі KPI, докази пілотування, фінальний аналітичний пакет.

**4.2 **Результати або дії, не зафіксовані в AITA, можуть вважатися неперевіреними для цілей компенсації, якщо вони не були явно підтверджені Засновником/Генеральним директором в AITA.

**5. Обсяг роботи Команди --- Повна підтримка**

Команда зобов\'язується надати повну підтримку щодо Угоди, включаючи, без обмежень:

**5.1**

-   підготовка матеріалів для переговорів: порядків денних, протоколів, подальших кроків;

-   підтримка динаміки угоди та воріт прийняття рішень;

-   координація з контрагентами та внутрішніми зацікавленими сторонами.

**5.2**

-   підготовка та узгодження договірних умов (у межах Воріт затвердження);

-   ведення версіонованого репозиторію договорів;

-   координація робочого процесу підписання та перевірки узгодженості.

**5.3**

-   визначення та побудова необхідного функціоналу Платформи AITA для цієї Угоди;

-   інтеграції, панелі управління, аналітика, звітні результати;

-   внутрішнє QA та управління релізами.

**5.4**

-   координація з постачальниками/EPC/O&M (за потреби);

-   процеси SLA/підтримки; обробка інцидентів (за потреби);

-   підтримка після запуску там, де це передбачено Угодою.

**5А. Визначення повної підтримки (обов\'язкові артефакти, SLA, DoD)**

**5А.1**

Команда повинна створити та підтримувати в актуальному стані такі артефакти для Угоди:

-   а) Робочий простір Угоди (структура, доступ, версіонування).

-   б) Карта зацікавлених сторін (особи, що приймають рішення, впливові особи, ланцюжок знайомств).

-   в) Часова шкала Угоди та Ворота прийняття рішень (фази, необхідні докази на кожному воріті).

-   г) Журнал переговорів (зустрічі, протоколи, зобов\'язання, наступні кроки).

-   ґ) Пропозиція та комерційний пакет (ціннісна пропозиція, обсяг, припущення, цінові коридори через Ворота затвердження).

-   д) Репозиторій договірного пакету (всі версії/редлайни/історія затверджень).

-   е) Беклог продукту/функціоналу (вимоги → тікети → релізи).

-   є) Панель KPI (спільні KPI + докази пілотування; див. Розділ 5Б).

-   ж) Реєстр ризиків (ризики, пом\'якшення, відповідальний, ескалація).

-   з) Пакет результатів рівня Ради (пакет рішення щодо масштабування/відмови або закриття).

**5А.2**

-   SLA реакції: для критичних елементів Угоди --- відповідь Команди в AITA протягом 4 годин у робочі дні.

-   SLA протоколів зустрічей: протоколи + рішення + наступні кроки протягом 12 годин після зустрічі/дзвінка.

-   SLA подальших кроків: зовнішні подальші кроки протягом 24 годин після зустрічі (якщо інше не узгоджено).

-   SLA ескалації: якщо ризик загрожує воротам прийняття рішень --- ескалувати в AITA до Засновника/Генерального директора протягом 24 годин.

-   Правило версіонування: будь-які зміни пропозиції/договору повинні бути версіонованими в AITA; «остання версія» повинна бути чітко позначена.

**5А.3**

-   DoD комерційного пакету: ціннісна пропозиція + обсяг + припущення + ціновий коридор + журнал затверджень.

-   DoD договірного пакету: узгоджений текст + історія редлайнів + затвердження + процес підписання + підписані копії.

-   DoD функціонального виконання: вимоги → тікети → реліз → верифікація → оновлення панелі KPI.

-   DoD пілоту (за наявності): базові дані → паспорт пілоту/pre-FEED → запуск → докази KPI → фінальний звіт.

**5Б. Спільні KPI Угоди (обов\'язкові)**

**5Б.1**

Протягом 5 робочих днів після підписання (або початку Угоди --- залежно від того, що настане раніше) Команда повинна створити спільну матрицю KPI та опублікувати її як Панель KPI в AITA.

**5Б.2**

Матриця KPI повинна включати щонайменше:

KPI прогресу Угоди:

-   підтверджене охоплення осіб, що приймають рішення;

-   виконання воріт прийняття рішень (%);

-   середній час до наступного кроку.

KPI переговорів та договорів:

-   кількість ключових зустрічей + результати;

-   статус та час циклу версії пропозиції/договору;

-   оцінка готовності до підписання.

KPI продукту/виконання:

-   запланований vs виконаний беклог;

-   час циклу релізу;

-   охоплення даних/моніторингу.

KPI результату/пілоту (за наявності):

-   операційний KPI (доступність/uptime/успішність сесій тощо за Паспортом угоди);

-   проксі економічного ефекту (економія/€ на об\'єкт, проксі прибутку);

-   оцінка готовності до масштабування.

**5Б.3**

Для ключових KPI Команда повинна визначити мінімально прийнятне/цільове/амбіційне значення там, де це можливо, для об\'єктивного прийняття рішень «масштабувати/не масштабувати».

**5Б.4**

-   Щотижневий огляд KPI в AITA (оновлення статусу, блокери, коригувальні дії).

-   Один відповідальний за кожен KPI, призначений Командою та зафіксований в AITA.

**5Б.5**

Будь-яка зміна KPI повинна бути версіонованою в AITA із зазначенням причини.

**6. Самоврядування команди**

**6.1 **Ролі: Команда самостійно призначає внутрішні ролі (наприклад, Лідер переговорів, Юридичний координатор, Власник продукту, Операційний виконавець, Лідер з даних/KPI тощо) та фіксує їх в AITA.

**6.2 **Прийняття рішень: якщо Команда не зафіксувала інше правило в AITA, операційні рішення Команди приймаються простою більшістю активних членів Команди.

**6.3 **Внутрішній розподіл: Команда розподіляє Командний пул прибутку між членами на власний розсуд та фіксує правила в Додатку T2 в AITA (включаючи зміни, дати набрання чинності).

**6.4 **Внутрішні суперечки: Засновник/Генеральний директор не несуть відповідальності за внутрішні суперечки щодо розподілу, якщо Правила внутрішнього розподілу Команди існують в AITA та були дотримані.

**7. Управління та Ворота затвердження (Засновник/Генеральний директор)**

**7.1 **Команда не може юридично або фінансово зобов\'язувати Групу/AITA без затверджень, зафіксованих в AITA, включаючи:

-   підписання договорів або прийняття остаточних комерційних умов/цінових коридорів;

-   видача гарантій/поручительств;

-   банківські/фінансові зобов\'язання;

-   публічні заяви від імені AITA/Групи.

**7.2 **Право підпису надається лише через окремі мандати/довіреності та в межах визначених лімітів.

**8. Компенсація: Командний пул прибутку (30%)**

**8.1 **Команда має право на Командний пул прибутку = 30% Прибутку від угоди, розрахованого згідно з Додатком Б.

**8.2 **Командний пул прибутку нараховується в міру реалізації прибутку та може виплачуватися пропорційно, з урахуванням резервів, визначених у Додатку Б.

**8.3 **Розподіл між членами Команди регулюється Правилами внутрішнього розподілу Команди (Додаток T2), зафіксованими в AITA.

**9. Управління реєстром**

**9.1 **Реєстр Команди визначається в Додатку T1 та може бути оновлений лише через AITA з контролем версій та підтвердженням Засновника/Генерального директора.

**9.2 **Член, який вибуває, зберігає права лише відповідно до Правил внутрішнього розподілу Команди, зафіксованих в AITA, та лише щодо реалізованого прибутку, якщо правила Команди не передбачають інше.

**10. Конфіденційність (Суворий NDA)**

**10.1 **Кожен член Команди зобов\'язаний зберігати конфіденційність усієї непублічної інформації про Угоду, контрагентів, переговори, ціноутворення, прибуток, логіку продукту, документи та внутрішні матеріали/процеси AITA.

**10.2 **Заборона розголошення, пересилання, публікації або використання в особистих цілях без письмового дозволу Засновника/Генерального директора в AITA.

**10.3 **Суттєве порушення може призвести до негайного видалення та втрати невиплаченої компенсації, а також до відповідальності за збитки.

**11. Заборона обходу, переманювання, обмежена конкуренція (5 років)**

**11.1 **Протягом строку дії та протягом 5 років після припинення кожен член Команди погоджується на:

-   заборону обходу: не обходити Сторони для захоплення Угоди, контактів, постачальників або ланцюжка виконання;

-   заборону переманювання: не переманювати співробітників, агентів, підрядників або клієнтів, залучених через Угоду;

-   обмежену конкуренцію: не виконувати безпосередньо конкуруючі роботи з тими самими ключовими контрагентами/локаціями/портфелем, визначеними в Додатках А/Е, у тій мірі, в якій це є виконуваним за застосовним правом.

**11.2 **Точний обсяг може підтримуватися як версіонований додаток в AITA.

**12. Строк та розірвання**

**12.1 **Набирає чинності з моменту підписання до завершення Угоди та врегулювання всіх зобов\'язань, якщо не буде розірвана раніше.

**12.2 **Засновник/Генеральний директор може негайно видалити члена Команди за суттєве порушення (порушення NDA, обхід, саботаж, систематичні порушення режиму лише цифрового формату).

**12.3 **У разі видалення за порушення невиплачена компенсація такого члена втрачається; Команда може перерозподілити її відповідно до Правил внутрішнього розподілу.

**13. Застосовне право та вирішення спорів**

**13.1 **Застосовне право: Іспанія, якщо інше не погоджено.

**13.2 **Спори: 10 днів переговорів, після чого --- Corte de Arbitraje de Madrid (CAM), місце арбітражу --- Мадрид, відповідно до Арбітражного регламенту CAM.

**17. Заключні положення**

**17.1 **Затвердження, зафіксовані в AITA, версіоновані оновлення, панелі KPI та правила розподілу визнаються письмовими доказами.

**14.2 **Зміни до цієї Угоди вимагають підписаного додатку або рішення, зафіксованого в AITA та затвердженого Засновником і Генеральним директором.

**. Додатки (зберігаються в AITA)**

Додаток А --- Паспорт угоди

Додаток Б --- Формула прибутку та резерви

Додаток T1 --- Реєстр Команди (Список членів)

Додаток T2 --- Правила внутрішнього розподілу Команди (Самокеровані)

(Необов\'язково) Додаток Е --- Карта обмежень (Контрагенти / Локації / Обсяг)

**. Підписи**

+--------------------------------------------------------------------+--------------------------------------------------------------------+--------------------------------------------------------------------+
| **ЗАСНОВНИК**                                                      | **ГЕНЕРАЛЬНИЙ ДИРЕКТОР**                                           | **ЧЛЕН КОМАНДИ**                                                   |
|                                                                    |                                                                    |                                                                    |
| Іван Шумлянський                                                   | Дмитро Мехед                                                       | Ім\'я:                                                             |
|                                                                    |                                                                    |                                                                    |
| _________________________________ | _________________________________ | _________________________________ |
|                                                                    |                                                                    |                                                                    |
| Дата: _____________________________   | Дата: _____________________________   | Дата: _____________________________   |
+--------------------------------------------------------------------+--------------------------------------------------------------------+--------------------------------------------------------------------+

+--------------------------------------------------------------------+--------------------------------------------------------------------+
| **ЧЛЕН КОМАНДИ**                                                   | **ЧЛЕН КОМАНДИ**                                                   |
|                                                                    |                                                                    |
| Ім\'я:                                                             | Ім\'я:                                                             |
|                                                                    |                                                                    |
| _________________________________ | _________________________________ |
|                                                                    |                                                                    |
| Дата: _____________________________   | Дата: _____________________________   |
+--------------------------------------------------------------------+--------------------------------------------------------------------+


---

# ═══ PROFILE 5 — PROJECT LEAD: Deal Execution Agreement (EN) ═══

**AITA DEAL EXECUTION AGREEMENT**
---------------------------------

**(Digital-Only / Project Lead / Product-Only Exception / Profit Split)**

**Date:** \[●\] 2026\
**Place:** Spain, Bilbao

### **1. Parties**

1.  **Ivan Shumlianskyi** --- Founder of the Group, **Co-Founder of AITA** (the **"Founder"**).

2.  **Dmytro Mekhed** --- **CEO of AITA**, **Co-Founder of AITA** (the **"CEO"**).

3.  **Katerina Abramova** --- Project Lead (the **"Project Lead"**).

Collectively, the **"Parties"**.

### **2. Purpose and scope**

2.1. This Agreement sets the rules of engagement for the Parties to execute a specific commercial **Deal** (defined below), including roles, mandatory digital execution via AITA, governance, profit split, confidentiality and post-termination restrictions.\
2.2. This Agreement is a framework and will be **supplemented by the Deal Context** (Appendices and versioned Deal documents), which become binding once approved in the AITA digital workspace under this Deal.

### **3. Definitions**

3.1. **Deal** --- the commercial project/transaction(s) described in **Appendix A (Deal Passport)**, including all related contracts, orders, milestones, deliverables and payments.\
3.2. **AITA Platform** --- the digital platform/workspace used for deal execution, where actions, evidence, tasks, documents, approvals, KPI and analytics are recorded.\
3.3. **Profit of the Deal** --- calculated under **Appendix B (Profit Formula)**, including agreed adjustments for returns, penalties, third-party commissions and reserves.\
3.4. **Team Profit Share** --- 50% of the Profit of the Deal allocated to the delivery team as described in Section 8.\
3.5. **Product-Only Exception** --- a rule for this Deal: product decisions are handled by the **Project Lead** within the approved strategy and boundaries, without requiring separate approvals for each product detail, while contractual/legal/financial commitments remain subject to Founder/CEO approvals as per Section 6.

### **4. Deal context and version control**

4.1. The Deal Context is defined by and maintained in the following appendices (and their versioned updates):

-   **Appendix A --- Deal Passport** (participants, goals, definition of done, phases, KPI, stakeholder map).

-   **Appendix B --- Profit Formula** (what counts as profit, costs, exclusions, reserves).

-   **Appendix C --- Strategy & Boundaries** (messaging, decision gates, approval matrix).\
    > 4.2. Any updates to the Deal Context must be made **through the AITA Platform**, with versioning and timestamps.\
    > 4.3. If there is a conflict, priority order is: this Agreement → Appendix A → Appendix C → Appendix B.

### **5. Role of Katerina Abramova --- Project Lead**

5.1. Katerina is appointed as **Project Lead** for the entire Deal lifecycle.\
5.2. Project Lead responsibilities include:

-   stakeholder & relationship coordination, scheduling, follow-ups, meeting notes and next steps;

-   keeping the delivery plan, dependencies and risks under control;

-   preparing product packaging for the pilot/case, data requirements, dashboards and analytics deliverables;

-   ensuring the team operates inside the Strategy and records everything in AITA.\
    > 5.3. Under the **Product-Only Exception**, the Project Lead may independently run product execution decisions **within** the approved Strategy & Boundaries (Appendix C).

### **6. Governance and approvals**

6.1. The Project Lead **cannot** bind the Parties legally/financially without approvals recorded in AITA. This includes: pricing commitments at group level, signing contracts, bank/financial commitments, warranties, public statements on behalf of AITA/Group.\
6.2. **Founder and CEO approvals** are required for:

-   final commercial terms and pricing corridors;

-   any binding obligations to third parties;

-   changes to profit split rules;

-   escalation decisions and dispute resolutions.

### **7. Mandatory digital execution (Digital-Only)**

7.1. The Parties agree that **all Deal activity and results must be executed through the AITA Platform** and be visible in the unified Deal context, including:

-   contact introductions, meetings/calls, agendas, minutes, next steps;

-   documents, offers, versions, approvals;

-   task tracking, deadlines, owners;

-   KPI tracking, pilot metrics, evidence;

-   final "board-grade" analytics pack and outcome validation.\
    > 7.2. Work/results not recorded in AITA may be treated as **non-verifiable** for performance and compensation purposes unless explicitly validated by Founder/CEO in AITA.

### **8. Profit split and compensation**

8.1. For this Deal, the delivery team executes under **Team Profit Share = 50% of the Profit of the Deal**.\
8.2. From the **Profit of the Deal**:

-   **20% of the Profit of the Deal** is allocated to the **Project Lead** as **Lead Success Fee**;

-   **30% of the Profit of the Deal** is allocated to the team pool and distributed per AITA rules / Founder+CEO decision recorded in AITA;

-   the remaining **50% of the Profit of the Deal** is allocated outside the Team Profit Share per the Deal structure in Appendix A.\
    > 8.3. The Parties confirm that the "20% to Project Lead" is part of the overall profit split for the Deal and is calculated according to Appendix B.

### **9. Advisory support limit**

9.1. Founder/CEO provide advisory support to the Project Lead **as needed**, limited to **45 minutes per day**, with the ability to **accumulate unused time** across days.\
9.2. Advisory support does not imply transfer of legal authority unless separately granted.

### **10. Trigger and payment mechanics**

10.1. The Project Lead becomes entitled to the Lead Success Fee if:

-   the Deal reaches the "Definition of Done" (Appendix A) and/or generates realized Profit as defined in Appendix B;

-   Profit is realized/received according to Appendix B;

-   the Project Lead complied with Digital-Only (Section 7) and there is no material breach of NDA / restrictions.\
    > 10.2. Payments may be made pro-rata as profit is realized and may include a reasonable warranty reserve (e.g., up to 10% for 90--180 days) if stated in Appendix B.

### **11. Next analytical case on the same terms**

11.1. Subject to successful performance and compliance under this Deal, the Founder and CEO are prepared to provide the Project Lead with a **next analytical case** to validate and replicate the model **under the same key terms**:\
Digital-Only via AITA, Project Lead role, profit split in Section 8, and advisory limits in Section 9---unless the Parties agree otherwise in AITA.

### **12. Confidentiality (strict NDA)**

12.1. The Project Lead and all Parties must keep confidential all non-public information about the Deal, contacts, negotiations, pricing, profit, product logic, documents, processes and any AITA internal materials.\
12.2. Any breach may result in immediate termination, loss of unpaid compensation, and liability for damages.

### **13. Non-circumvention, non-solicitation, limited non-competition (5 years)**

13.1. During the term and for **5 years** after termination, the Project Lead agrees to:

-   **non-circumvent**: not bypass the Parties to capture the Deal, contacts, suppliers or execution chain for personal benefit;

-   **non-solicit**: not poach team members, agents, contractors, or clients introduced via the Deal;

-   **limited non-competition**: not engage in directly competing execution with the same key Deal counterparties/locations/portfolio as defined in Appendix A/E, to the extent enforceable under applicable law.\
    > 13.2. The exact scope (counterparties, geography, activities) may be specified and updated in AITA as a versioned appendix to keep it enforceable.

### **14. Term and termination**

14.1. This Agreement is effective from the signing date until the Deal is completed and all obligations are settled, unless terminated earlier.\
14.2. Founder and CEO may terminate immediately for material breach (NDA breach, circumvention, systematic Digital-Only violations, sabotage).\
14.3. Upon termination due to breach, unpaid Lead Success Fee is forfeited.

### **15. Governing law and disputes**

15.1. Governing law: Spain, unless otherwise agreed.\
15.2. Disputes: 10 days negotiation, then Corte de Arbitraje de Madrid (CAM), seat in Madrid, under CAM Arbitration Rules.

### 

**16. Force Majeure**

16.1. Neither Party shall be liable for delay or failure to perform obligations under this Agreement to the extent caused by events beyond its reasonable control, including but not limited to: acts of God, war, terrorism, pandemic, government restrictions, fire, flood, or power outages ("Force Majeure Event").

16.2. The affected Party shall promptly notify the other Party of the Force Majeure Event and use reasonable efforts to mitigate its effects. Obligations are suspended for the duration of the Force Majeure Event.

16.3. If a Force Majeure Event continues for more than sixty (60) days, either Party may terminate this Agreement by written notice without liability.

**17. Language and Controlling Version**

17.1. This Agreement is executed in English. The English version shall be the controlling version. Any translation of this Agreement into any other language is for informational purposes only and shall not affect the interpretation or enforcement of the English version.

**18. Personal Data Protection**

18.1. To the extent any Party processes personal data of individuals (including employees, representatives, and contacts) in connection with this Agreement, each Party shall act as an independent controller and shall comply with all applicable data protection laws, including Regulation (EU) 2016/679 (GDPR) and Ley Orgánica 3/2018 (LOPDGDD) where applicable.

18.2. Each Party warrants that it has an adequate legal basis for any processing of personal data undertaken in connection with this Agreement. The Parties shall cooperate to respond to data subject requests and regulatory inquiries.

**19. Final provisions**

19.1. Approvals and versioned updates recorded in AITA are recognized as written confirmations between the Parties for operational governance.\
16.2. Any change to this Agreement must be made in writing (signed addendum or AITA-recorded decision signed/approved by Founder and CEO).

**Appendices (to be maintained in AITA)**
-----------------------------------------

**Appendix A --- Deal Passport (BM×Zunder×AITA / One-Strike Pilot)\
** **Appendix B --- Profit Formula & Reserves\
** **Appendix C --- Strategy & Boundaries (Approval Matrix, Versioning)\
** *(Optional)* Appendix E --- Restriction Map (Counterparties / Locations / Scope)

**Signatures**
--------------

**Ivan Shumlianskyi** __________________ Date: ***/***/2026\
**Dmytro Mekhed** ______________________ Date: ***/***/2026\
**Katerina Abramova** __________________ Date: ***/***/2026


---

# ═══ PROFILE 5 — PROJECT LEAD: Договір виконання угод (UA) ═══

**УГОДА ПРО ВИКОНАННЯ УГОДИ**

*(Лише цифровий формат / Керівник проекту / Виняток «лише продукт» / Розподіл прибутку)*

Дата: \[●\] 2026 р. \| Місце: Іспанія, Більбао

**1. Сторони**

Іван Шумлянський --- Засновник Групи, Співзасновник AITA (\"Засновник\").

Дмитро Мехед --- Генеральний директор AITA, Співзасновник AITA (\"Генеральний директор\").

Катерина Абрамова --- Керівник проекту (\"Керівник проекту\").

Спільно --- \"Сторони\".

**2. Мета та обсяг**

**2.1 **Ця Угода встановлює правила взаємодії Сторін для виконання конкретної комерційної Угоди (визначеної нижче), включаючи ролі, обов\'язкове цифрове виконання через AITA, управління, розподіл прибутку, конфіденційність та обмеження після припинення.

**2.2 **Ця Угода є рамковою та доповнюватиметься Контекстом угоди (Додатками та версіонованими документами Угоди), які набувають обов\'язкової сили після затвердження в цифровому робочому просторі AITA за цією Угодою.

**3. Визначення**

**3.1 **Угода --- комерційний проект/транзакція(-ії), описані в Додатку А (Паспорт угоди), включаючи всі пов\'язані договори, замовлення, етапи, результати та платежі.

**3.2 **Платформа AITA --- цифрова платформа/робочий простір, що використовується для виконання угод, де фіксуються дії, докази, завдання, документи, затвердження, KPI та аналітика.

**3.3 **Прибуток від угоди --- розраховується згідно з Додатком Б (Формула прибутку), включаючи узгоджені коригування на повернення, штрафи, комісії третіх сторін і резерви.

**3.4 **Частка команди у прибутку --- 50% Прибутку від угоди, виділених команді виконання відповідно до Розділу 8.

**3.5 **Виняток «лише продукт» --- правило для цієї Угоди: продуктові рішення обробляються Керівником проекту в межах затвердженої стратегії та кордонів, без необхідності отримання окремих затверджень для кожної деталі продукту, тоді як договірні/правові/фінансові зобов\'язання залишаються предметом затверджень Засновника/Генерального директора відповідно до Розділу 6.

**4. Контекст угоди та контроль версій**

**4.1 **Контекст угоди визначається та підтримується в таких додатках (та їх версіонованих оновленнях):

-   Додаток А --- Паспорт угоди (учасники, цілі, визначення готовності, фази, KPI, карта зацікавлених сторін).

-   Додаток Б --- Формула прибутку (що вважається прибутком, витрати, виключення, резерви).

-   Додаток В --- Стратегія та кордони (меседжинг, ворота прийняття рішень, матриця затверджень).

**4.2 **Будь-які оновлення Контексту угоди повинні здійснюватися через Платформу AITA з версіонуванням та часовими мітками.

**4.3 **У разі конфлікту пріоритет визначається таким порядком: ця Угода → Додаток А → Додаток В → Додаток Б.

**5. Роль Катерини Абрамової --- Керівника проекту**

**5.1 **Катерина призначається Керівником проекту на весь життєвий цикл Угоди.

**5.2 **До обов\'язків Керівника проекту належать:

-   координація зацікавлених сторін і відносин, планування зустрічей, подальші кроки, нотатки та наступні дії;

-   контроль плану виконання, залежностей і ризиків;

-   підготовка упаковки продукту для пілоту/кейсу, вимог до даних, панелей і аналітичних результатів;

-   забезпечення роботи команди в межах Стратегії та фіксації всього в AITA.

**5.3 **Відповідно до Винятку «лише продукт» Керівник проекту може самостійно приймати рішення щодо виконання продукту в межах затвердженої Стратегії та кордонів (Додаток В).

**6. Управління та затвердження**

**6.1 **Керівник проекту не може юридично/фінансово зобов\'язувати Сторони без затверджень, зафіксованих в AITA. Це включає: цінові зобов\'язання на рівні групи, підписання договорів, банківські/фінансові зобов\'язання, гарантії, публічні заяви від імені AITA/Групи.

**6.2 **Затвердження Засновника та Генерального директора потрібні для:

-   остаточних комерційних умов та цінових коридорів;

-   будь-яких зобов\'язань перед третіми сторонами;

-   змін правил розподілу прибутку;

-   рішень щодо ескалації та вирішення спорів.

**7. Обов\'язкове виконання лише у цифровому форматі**

**7.1 **Сторони погоджуються, що вся діяльність та результати за Угодою повинні виконуватися через Платформу AITA та бути видимими у єдиному контексті Угоди, включаючи:

-   знайомства з контактами, зустрічі/дзвінки, порядки денних, протоколи, наступні кроки;

-   документи, пропозиції, версії, затвердження;

-   відстеження завдань, дедлайни, відповідальні;

-   відстеження KPI, метрики пілоту, докази;

-   фінальний аналітичний пакет рівня Ради та валідація результату.

**7.2 **Робота/результати, не зафіксовані в AITA, можуть вважатися неперевіреними для цілей виконання та компенсації, якщо вони не були явно підтверджені Засновником/Генеральним директором в AITA.

**8. Розподіл прибутку та компенсація**

**8.1 **За цією Угодою команда виконання діє в межах Частки команди у прибутку = 50% Прибутку від угоди.

**8.2 **З Прибутку від угоди:

-   20% Прибутку від угоди виділяється Керівнику проекту як Гонорар за успіх керівника;

-   30% Прибутку від угоди виділяється до командного пулу та розподіляється відповідно до правил AITA / рішення Засновника+Генерального директора, зафіксованого в AITA;

-   решта 50% Прибутку від угоди розподіляється поза Часткою команди у прибутку відповідно до структури Угоди в Додатку А.

**8.3 **Сторони підтверджують, що «20% Керівнику проекту» є частиною загального розподілу прибутку за Угодою та розраховується відповідно до Додатку Б.

**9. Ліміт консультаційної підтримки**

**9.1 **Засновник/Генеральний директор надають консультаційну підтримку Керівнику проекту за потреби, обмежену 45 хвилинами на день, з можливістю накопичення невикористаного часу протягом днів.

**9.2 **Консультаційна підтримка не передбачає передачі юридичних повноважень, якщо вони не надані окремо.

**10. Тригер та механіка оплати**

**10.1 **Керівник проекту набуває права на Гонорар за успіх керівника якщо:

-   Угода досягає «Визначення готовності» (Додаток А) та/або генерує реалізований Прибуток відповідно до Додатку Б;

-   Прибуток реалізований/отриманий відповідно до Додатку Б;

-   Керівник проекту дотримувався режиму лише цифрового формату (Розділ 7) та не допустив суттєвого порушення NDA/обмежень.

**10.2 **Виплати можуть здійснюватися пропорційно в міру реалізації прибутку та можуть включати розумний гарантійний резерв (наприклад, до 10% протягом 90--180 днів), якщо це зазначено в Додатку Б.

**11. Наступний аналітичний кейс на тих самих умовах**

**11.1 **За умови успішного виконання та дотримання умов за цією Угодою, Засновник та Генеральний директор готові надати Керівнику проекту наступний аналітичний кейс для валідації та тиражування моделі на тих самих ключових умовах: лише цифровий формат через AITA, роль Керівника проекту, розподіл прибутку відповідно до Розділу 8, та ліміти консультацій відповідно до Розділу 9, --- якщо Сторони не домовляться про інше в AITA.

**12. Конфіденційність (Суворий NDA)**

**12.1 **Керівник проекту та всі Сторони зобов\'язані зберігати конфіденційність усієї непублічної інформації про Угоду, контакти, переговори, ціноутворення, прибуток, логіку продукту, документи, процеси та будь-які внутрішні матеріали AITA.

**12.2 **Будь-яке порушення може призвести до негайного розірвання, втрати невиплаченої компенсації та відповідальності за збитки.

**13. Заборона обходу, переманювання, обмежена конкуренція (5 років)**

**13.1 **Протягом строку дії та протягом 5 років після припинення Керівник проекту погоджується на:

-   заборону обходу: не обходити Сторони для захоплення Угоди, контактів, постачальників або ланцюжка виконання в особистих цілях;

-   заборону переманювання: не переманювати членів команди, агентів, підрядників або клієнтів, залучених через Угоду;

-   обмежену конкуренцію: не займатися безпосередньо конкуруючим виконанням з тими самими ключовими контрагентами/локаціями/портфелем Угоди, визначеними в Додатках А/Е, у тій мірі, в якій це є виконуваним за застосовним правом.

**13.2 **Точний обсяг (контрагенти, географія, діяльність) може бути уточнений та оновлений в AITA у вигляді версіонованого додатку для забезпечення його виконуваності.

**14. Строк та розірвання**

**14.1 **Ця Угода набирає чинності з дати підписання до завершення Угоди та врегулювання всіх зобов\'язань, якщо не буде розірвана раніше.

**14.2 **Засновник та Генеральний директор можуть розірвати угоду негайно за суттєве порушення (порушення NDA, обхід, систематичні порушення режиму лише цифрового формату, саботаж).

**14.3 **У разі розірвання через порушення невиплачений Гонорар за успіх керівника втрачається.

**15. Застосовне право та вирішення спорів**

**15.1 **Застосовне право: Іспанія, якщо інше не погоджено.

**15.2 **Спори: 10 днів переговорів, після чого --- Corte de Arbitraje de Madrid (CAM), місце арбітражу --- Мадрид, відповідно до Арбітражного регламенту CAM.

**19. Заключні положення**

**19.1 **Затвердження та версіоновані оновлення, зафіксовані в AITA, визнаються письмовими підтвердженнями між Сторонами для оперативного управління.

**16.2 **Будь-яка зміна до цієї Угоди повинна бути оформлена в письмовій формі (підписаний додаток або рішення AITA, підписаний/затверджений Засновником та Генеральним директором).

**. Додатки (підтримуються в AITA)**

Додаток А --- Паспорт угоди

Додаток Б --- Формула прибутку та резерви

Додаток В --- Стратегія та кордони (Матриця затверджень, Версіонування)

(Необов\'язково) Додаток Е --- Карта обмежень (Контрагенти / Локації / Обсяг)

**. Підписи**

+--------------------------------------------------------------------+--------------------------------------------------------------------+--------------------------------------------------------------------+
| **ЗАСНОВНИК**                                                      | **ГЕНЕРАЛЬНИЙ ДИРЕКТОР**                                           | **КЕРІВНИК ПРОЕКТУ**                                               |
|                                                                    |                                                                    |                                                                    |
| Іван Шумлянський                                                   | Дмитро Мехед                                                       | Катерина Абрамова                                                  |
|                                                                    |                                                                    |                                                                    |
| _________________________________ | _________________________________ | _________________________________ |
|                                                                    |                                                                    |                                                                    |
| Дата: _____________________________   | Дата: _____________________________   | Дата: _____________________________   |
+--------------------------------------------------------------------+--------------------------------------------------------------------+--------------------------------------------------------------------+


---

# ═══ PROFILE 6 — SALES AGENT: Agent Agreement (EN) ═══

**AGENT AGREEMENT**

**AITA Agent Network**

*Non-Exclusive B2B Sales Agency Agreement*

This Agent Agreement (\"Agreement\") is entered into as of _____________ (the \"Effective Date\"), between:

+-------------------------------------+--------------------------------------------------------------------------------+
| **AITA WORLD, S.L.**                | **AGENT**                                                                      |
|                                     |                                                                                |
| Role: Principal / Platform Operator | Role: Independent Sales Agent                                                  |
|                                     |                                                                                |
| CIF: B75859744                      | [Full Name / Legal Name:                                    ]      |
|                                     |                                                                                |
| Address: Sabino Arana, 8-2          | [Country:                                                        ] |
|                                     |                                                                                |
| 48013 Bilbao, Bizkaia, España       | [ID / Tax Number:                                            ]     |
|                                     |                                                                                |
| Email: d.mekhed\@aita.world         | [Contact Email:                                              ]     |
|                                     |                                                                                |
|                                     | [Telegram Handle:                                            ]     |
+-------------------------------------+--------------------------------------------------------------------------------+

**(collectively, the \"Parties\", individually a \"Party\")**

**1. Purpose and Scope**

**1.1 **AITA operates a B2B trading platform that sources products directly from manufacturers and large importers --- including solar energy equipment (panels, inverters, batteries, industrial-scale systems), industrial electrical equipment, generators, cable products, and construction/engineering materials --- and offers these to end buyers at competitive prices.

**1.2 **Agent agrees to act as a non-exclusive independent sales agent of AITA, finding and introducing qualified B2B buyers to AITA for the purpose of purchasing products from AITA\'s catalogue (the \"Products\").

**1.3 **Agent acts as an independent contractor, not as an employee, partner, or joint venture participant of AITA. Agent has no authority to bind AITA contractually unless expressly authorised in writing.

**2. Definitions**

**2.1 **Strike Price: The base price set by AITA for each product or order, representing AITA\'s procurement cost plus logistics plus AITA service margin. Communicated to Agent before submission of each client offer.

**2.2 **Client Price: The final price at which Agent\'s B2B client agrees to purchase the Products from AITA.

**2.3 **Margin: The positive difference between Client Price and Strike Price on a given order (Margin = Client Price − Strike Price).

**2.4 **Agent Level: Agent\'s tier (Level 1 / Level 2 / Level 3) based on cumulative turnover, which determines Agent\'s minimum Margin share percentage.

**2.5 **Recruiter: An Agent who has introduced and onboarded the Agent to the AITA network under a Partner Agreement. If Agent was not recruited, Recruiter = null and 100% of the 80% pool accrues to Agent.

**2.6 **Confirmed Transaction: A transaction where AITA has received full payment from Agent\'s B2B client.

**3. Agent Obligations**

**3.1 **Agent shall: (a) actively seek B2B clients with genuine demand for Products in AITA\'s catalogue; (b) submit all client inquiries and purchase requests to AITA exclusively via the designated Telegram bot or appointed AITA manager; (c) agree Client Price with the buyer only after AITA has provided the Strike Price; (d) accurately represent Products to clients and not make warranties beyond those provided by AITA; (e) maintain professional conduct and protect AITA\'s brand reputation.

**3.2 **Agent shall not: (a) quote prices below the Strike Price; (b) accept payments from clients directly (all payments flow through AITA); (c) commit to delivery timelines, specifications, or terms not confirmed by AITA; (d) recruit sub-agents under this Agreement (sub-agent recruitment is governed by the Partner Agreement).

**4. AITA Obligations**

**4.1 **AITA shall: (a) provide Agent with access to the product catalogue and up-to-date Strike Prices via the Telegram bot; (b) prepare commercial offers and documentation for each client lead submitted by Agent; (c) issue invoices to and collect payments from Agent\'s clients; (d) manage logistics, quality control, and warranty support for all Confirmed Transactions; (e) calculate and disburse Agent\'s Margin Share automatically following each Confirmed Transaction; (f) provide real-time Agent dashboard (Level, turnover, payout history, progress) via the Telegram bot.

**5. Sales Process**

  ---------- ----------- ----------------------------------------------------------------------------------------------------------
  **Step**   **Actor**   **Action**
  **1**      Agent       Identifies a B2B buyer with a specific product need
  2          Agent       Submits the inquiry to AITA via Telegram bot or account manager (product, volume, delivery requirements)
  3          AITA        Prepares commercial offer with Strike Price and delivery terms; sends to Agent
  4          Agent       Negotiates final Client Price with buyer (must be ≥ Strike Price); confirms order
  5          AITA        Issues invoice to client; monitors payment; arranges delivery and documentation
  6          AITA        Confirms receipt of client payment (Confirmed Transaction)
  7          AITA        Automatically calculates and pays Agent\'s Margin Share (and Recruiter share if applicable)
  ---------- ----------- ----------------------------------------------------------------------------------------------------------

**6. Compensation: Margin Split Model**

**6.1 **AITA Platform Fee: AITA retains twenty percent (20%) of the Margin from every Confirmed Transaction as the Platform Fee. This fee covers platform operations, logistics, quality control, documentation, and warranty support.

**6.2 **Agent Pool: The remaining eighty percent (80%) of the Margin constitutes the Agent Pool, which is divided between Agent and Agent\'s Recruiter (if any) as set out in §6.3--§6.4.

**6.3 **Agent Level and Minimum Share: Agent\'s minimum share of the Agent Pool is determined by Agent\'s cumulative turnover (total Client Price of all Confirmed Transactions since Agreement commencement):

  ------------- ------------------------- ----------------------------------- --------------------------------------- ----------
  **Level**     **Cumulative Turnover**   **Agent Min Share (of 80% Pool)**   **Recruiter Max Share (of 80% Pool)**   **AITA**
  **Level 1**   €0 -- €15,000             30%                                 50%                                     20%
  **Level 2**   €15,001 -- €50,000        45%                                 35%                                     20%
  **Level 3**   €50,001 +                 60%                                 20%                                     20%
  ------------- ------------------------- ----------------------------------- --------------------------------------- ----------

**6.4 **Recruiter Share: The Recruiter receives the remainder of the Agent Pool (80% Pool − Agent Share). The Recruiter may, at their discretion, set Agent\'s share above the minimum stated in §6.3 --- reducing the Recruiter\'s own share --- as a motivational tool. Any adjustment by Recruiter is communicated to Agent via the Telegram bot. If Agent has no Recruiter, Agent receives 100% of the 80% Pool.

**6.5 **Level Progression: Agent automatically advances to the next Level upon reaching the corresponding cumulative turnover threshold. Level advancement is irreversible. Agent\'s new Level and updated percentage are reflected in the Telegram bot immediately upon crossing the threshold.

**6.6 **Illustrative Example (Level 1, Margin €1,000):

  ------------- ----------------- ----------------- --------------------- ---------------- ---------------
  **Agent %**   **Recruiter %**   **Agent (EUR)**   **Recruiter (EUR)**   **AITA (EUR)**   **Comment**
  30%           50%               € 240             € 400                 € 200            Max Recruiter
  40%           40%               € 320             € 320                 € 200            Parity
  50%           30%               € 400             € 240                 € 200            Balanced
  60%           20%               € 480             € 160                 € 200            Lvl 3 max
  ------------- ----------------- ----------------- --------------------- ---------------- ---------------

**7. Payment and Payouts**

**7.1 **Payout Trigger: Agent\'s Margin Share is paid automatically after AITA confirms receipt of full client payment for a Confirmed Transaction.

**7.2 **Payout Timing: AITA shall transfer Agent\'s Margin Share within five (5) business days of the Confirmed Transaction. Automatic notifications are sent via the Telegram bot.

**7.3 **Payment Method: Bank transfer (SEPA/SWIFT) to Agent\'s bank account as registered in the AITA system. Alternative payment methods (PayPal, crypto, etc.) require prior written agreement.

**7.4 **Currency: All payouts are in EUR. If Agent\'s bank account is in a different currency, conversion fees are borne by Agent.

**7.5 **Taxes: Agent is solely responsible for declaring and paying all applicable taxes, social contributions, and withholdings on income received under this Agreement. AITA does not withhold taxes on Agent payouts.

**7.6 **Disputes: If Agent disputes a payout calculation, written notice must be submitted within ten (10) days of payout. AITA shall review and respond within five (5) business days.

**8. Agent Levels, Badges, and Gamification**

**8.1 **Telegram Bot Dashboard: Agent has real-time access to: current Level and Margin percentage; cumulative turnover and progress to next Level; passive income (if Agent is also a Recruiter); position in weekly Agent leaderboard; full payout history.

**8.2 **Performance Badges: The following automatic badges are awarded in the Telegram bot:

  ---------------- ----------------------------------------------------- ---------------------------------------------------
  **Badge**        **Trigger**                                           **Reward**
  🔥 Streak         3 consecutive Confirmed Transactions                  +5% bonus on the next transaction\'s Margin Share
  🏆 First Deal     First Confirmed Transaction                           Bonus notification + badge in Telegram profile
  ⚡ Level Up       Transition to next Level                              Notification + updated Agent card
  👑 Weekly King    \#1 on weekly turnover leaderboard                    Public highlight in the Telegram bot community
  🤝 Team Builder   5+ active agents in Agent\'s network (if Recruiter)   Special Recruiter status in the AITA system
  ---------------- ----------------------------------------------------- ---------------------------------------------------

**9. Non-Exclusivity and Flexibility**

**9.1 **Non-Exclusive: This Agreement is non-exclusive. Agent is free to engage in other commercial activities, including working for competing businesses, without AITA\'s consent.

**9.2 **No Minimum Obligation: Agent has no minimum turnover, minimum number of transactions, or minimum activity obligations. AITA has no obligation to guarantee a minimum level of inquiries or clients to Agent.

**9.3 **No Employment: Nothing in this Agreement creates an employment, partnership, or joint venture relationship. Agent does not receive salary, social benefits, or employment protections from AITA.

**10. Confidentiality**

**10.1 **Agent shall keep strictly confidential: (a) Strike Prices and AITA\'s supplier relationships; (b) client data and contact details obtained through AITA\'s platform; (c) AITA\'s margin model, Telegram bot logic, and internal processes; (d) any other information marked confidential or reasonably understood to be proprietary.

**10.2 **Confidentiality obligations survive termination of this Agreement for twenty-four (24) months.

**10.3 **Agent shall not use client data obtained through AITA for any purpose other than performing under this Agreement, including no direct sales bypassing AITA.

**11. Non-Circumvention**

**11.1 **Agent shall not, during the term of this Agreement and for twelve (12) months thereafter, directly or indirectly: (a) contact, solicit, or transact with clients introduced through AITA for the same or similar products, bypassing AITA; (b) introduce AITA\'s suppliers, products, or pricing to competitors of AITA; (c) use AITA\'s Confidential Information to facilitate a competing sales channel.

**11.2 **Breach of §11.1 shall entitle AITA to claim liquidated damages equal to the higher of (a) EUR 5,000 or (b) the total Margin AITA would have earned from the circumvented transaction(s).

**12. Term and Termination**

**12.1 **Term: This Agreement commences on the Effective Date and continues for one (1) year, unless earlier terminated. It renews automatically for successive one-year terms unless either Party gives thirty (30) days\' written notice of non-renewal.

**12.2 **Termination for Convenience: Either Party may terminate this Agreement at any time upon thirty (30) days\' written notice.

**12.3 **Immediate Termination by AITA: AITA may terminate this Agreement immediately if Agent: (a) breaches §10 (Confidentiality) or §11 (Non-Circumvention); (b) misrepresents Products to clients; (c) accepts client payments directly; (d) engages in fraudulent, dishonest, or illegal conduct.

**12.4 **Effect of Termination: Upon termination, (a) Agent\'s access to the Telegram bot is revoked; (b) any accrued but unpaid Margin Shares for Confirmed Transactions prior to termination remain payable; (c) confidentiality and non-circumvention obligations survive per §10--§11.

**13. Governing Law and Dispute Resolution**

**13.1 **This Agreement is governed by the laws of the Kingdom of Spain.

**13.2 **Disputes shall be resolved by binding arbitration under the Rules of the Corte de Arbitraje de Madrid (CAM), seated in Madrid, Spain, conducted in English (or Ukrainian / Russian by mutual agreement).

**14. Miscellaneous**

**14.1 **Entire Agreement: This Agreement, together with the current Strike Price schedule communicated via the Telegram bot, constitutes the entire agreement between the Parties regarding Agent\'s role in the AITA network.

**14.2 **Amendments: AITA may update the product catalogue, Strike Prices, and Level thresholds with seven (7) days\' notice via the Telegram bot or email. Changes to core compensation terms (§6) require written amendment.

**14.3 **Language: English is the controlling version. Ukrainian or Russian translations may be provided for convenience.

**15. Execution**

**IN WITNESS WHEREOF, the Parties have executed this Agent Agreement as of the date first written above.**

+--------------------------------------------------------------------------+--------------------------------------------------------------------------+
| **AITA WORLD, S.L. (Principal)**                                         | **AGENT**                                                                |
|                                                                          |                                                                          |
| By: _________________________________   | By: _________________________________   |
|                                                                          |                                                                          |
| Name: Dmytro Mekhed                                                      | Name:                                                                    |
|                                                                          |                                                                          |
| Title: Director                                                          | Telegram:                                                                |
|                                                                          |                                                                          |
| Date: _________________________________ | Date: _________________________________ |
+--------------------------------------------------------------------------+--------------------------------------------------------------------------+


---

# ═══ PROFILE 6 — SALES AGENT: Агентська угода (UA) ═══

**АГЕНТСЬКА УГОДА**

**AITA Agent Network**

*Невиключна агентська угода з продажу B2B*

Ця Агентська Угода (далi --- «Угода») укладена   _____________    (далi --- «Дата набрання чинності»), між:

+--------------------------------------+----------------------------------------------------------------------------+
| **AITA WORLD, S.L.**                 | **АГЕНТ**                                                                  |
|                                      |                                                                            |
| Роль: Принципал / Оператор платформи | Роль: Незалежний торговий агент                                            |
|                                      |                                                                            |
| CIF: B75859744                       | [ПІБ / Назва Суб'єкта:                               ]         |
|                                      |                                                                            |
| Sabino Arana, 8-2, 48013             | [Країна:                                                     ] |
|                                      |                                                                            |
| Bilbao, Bizkaia, Іспанія             | [ІПН / Код ПЛАТНИК:                                     ]      |
|                                      |                                                                            |
| Email: d.mekhed\@aita.world          | [Email:                                                      ] |
|                                      |                                                                            |
|                                      | [Telegram:                                                   ] |
+--------------------------------------+----------------------------------------------------------------------------+

**(разом --- «Сторони», окремо --- «Сторона»)**

**1. Предмет угоди**

**1.1 **AITA експлуатує B2B торгову платформу, яка закуповує товари безпосередньо у виробників та великих імпортерів --- без регіональних дилерів і дистрибуторських надбавок. Каталог товарів («Товари») включає: сонячне енергетичне обладнання (панелі, інвертори, акумулятори, промислові системи), промислове електрообладнання, генератори, кабельна продукція, будівельні та інженерні рішення.

**1.2 **Агент погоджується виступати невиключним незалежним торговим агентом AITA: знаходити B2B-покупців і представляти їх AITA для придбання Товарів з каталогу.

**1.3 **Агент діє як незалежний підпрядник, а не працівник, партнер чи учасник спільного підприємства AITA. Агент не має повноважень брати на себе юридичні зобов'язання від імені AITA.

**2. Визначення**

**2.1 **Страйк-прайс --- базова ціна, встановлена AITA для кожного замовлення: закупівельна ціна + логістика + сервіс AITA. Повідомляється Агенту до подачі кожної пропозиції через Telegram-бот.

**2.2 **Клієнтська ціна --- фінальна ціна, за якою B2B-покупець Агента погоджується придбати Товари у AITA.

**2.3 **Маржа --- різниця між Клієнтською ціною та Страйк-прайсом (Маржа = Клієнтська ціна − Страйк-прайс).

**2.4 **Рівень Агента --- поточний статус (Рівень 1 / 2 / 3) залежно від накопиченого обороту, що визначає мінімальну частку Маржі.

**2.5 **Рекрутер --- агент, який залучив даного Агента в мережу AITA на підставі Партнерської угоди. Якщо Агент був залучений самостійно --- 100% фонду 80% належить Агенту.

**2.6 **Підтверджена угода --- угода, за якою AITA отримала повну оплату від B2B-покупця.

**3. Обов\'язки Агента**

**3.1 **Агент зобов\'язаний: (а) активно шукати B2B-покупців з реальною потребою в Товарах із каталогу AITA; (б) передавати усі запити в AITA виключно через Telegram-бот або менеджера; (в) узгоджувати фінальну Клієнтську ціну з покупцем лише після отримання Страйк-прайсу від AITA; (г) не надавати гарантій понад тих, що підтверджені AITA; (д) підтримувати репутацію бренду AITA.

**3.2 **Агенту забороняється: (а) пропонувати ціни нижче Страйк-прайсу; (б) приймати оплату від покупців напряму (усі платежі проходять через AITA); (в) брати на себе зобов\'язання щодо термінів постачання чи специфікацій, не підтверджених AITA.

**4. Обов\'язки AITA**

**4.1 **AITA зобов'язується: (а) надати доступ до каталогу і актуальних Страйк-прайсів через Telegram-бот; (б) готувати комерційні пропозиції для кожного ліду; (в) виставляти рахунки покупцям і контролювати оплату; (г) вести логістику, контроль якості, документообіг і гарантійний супровід; (д) автоматично розраховувати і виплачувати частку Маржі Агенту після кожної Підтвердженої угоди; (е) надавати дашборд в реальному часі (Рівень, оборот, історія виплат) через Telegram-бот.

**5. Процес продажу**

  ---------- ----------- ---------------------------------------------------------------------------------------------------
  **Крок**   **Актор**   **Дія**
  **1**      Агент       Знаходить B2B-покупця з конкретною потребою в Товарах
  2          Агент       Передає запит в AITA через Telegram-бот або менеджера (продукція, об'єм, умови постачання)
  3          AITA        Готує комерційну пропозицію зі Страйк-прайсом і умовами постачання; надсилає Агенту
  4          Агент       Узгоджує фінальну Клієнтську ціну з покупцем (не нижче Страйк-прайсу); підтверджує замовлення
  5          AITA        Виставляє рахунок покупцю; супроводжує оплату, логістику, документацію, гарантію
  6          AITA        Підтверджує отримання повної оплати → Автовиплата частки Маржі Агенту (і Рекрутеру при наявності)
  ---------- ----------- ---------------------------------------------------------------------------------------------------

**6. Винагорода: модель розподілу маржі**

**6.1 **Платформовий збір AITA: AITA завжди утримує двадцять відсотків (20%) Маржі на покриття платформи, логістики, контролю якості та гарантійного супроводу.

**6.2 **Фонд Агента: залишкові вісімдесят відсотків (80%) Маржі --- «Фонд 80%» --- діляться між Агентом і Рекрутером (при наявності) згідно з §§ 6.3--6.4.

**6.3 **Рівні Агента і мінімальна частка (% від Фонду 80%):

  -------------- ------------------------ -------------------------- ------------------------------ ---------------------- -------------
  **Рівень**     **Накопичений оборот**   **Агент мін. (від 80%)**   **Рекрутер макс. (від 80%)**   **AITA (від Маржі)**   **Перехід**
  **Рівень 1**   €0 -- €15 000            30%                        50%                            20%                    авто
  **Рівень 2**   €15 001 -- €50 000       45%                        35%                            20%                    авто
  **Рівень 3**   €50 001+                 60%                        20%                            20%                    авто
  -------------- ------------------------ -------------------------- ------------------------------ ---------------------- -------------

**6.4 **Частка Рекрутера: Рекрутер отримує залишок Фонду 80% після частки Агента. Рекрутер може за власним бажанням підвищити частку Агента понад мінімум --- зменшуючи свою частку. Якщо Агент був залучений самостійно --- він отримує 100% Фонду 80%.

**6.5 **Приклад при Маржі €1 000, Рівень 1:

  ------------- ---------------- --------------- ------------------ -------------- -----------------
  **Агент %**   **Рекрутер %**   **Агент (€)**   **Рекрутер (€)**   **AITA (€)**   **Примітка**
  30%           50%              € 240           € 400              € 200          Макс. рекрутеру
  40%           40%              € 320           € 320              € 200          Паритет
  50%           30%              € 400           € 240              € 200          Баланс
  60%           20%              € 480           € 160              € 200          Макс. агенту
  ------------- ---------------- --------------- ------------------ -------------- -----------------

**7. Виплати**

**7.1 **Частка Маржі Агента виплачується автоматично після підтвердження AITA повної оплати від покупця.

**7.2 **Строк виплати: протягом п'яти (5) робочих днів з моменту Підтвердженої угоди. Автоматичне повідомлення через Telegram-бот.

**7.3 **Спосіб виплати: банківський переказ (SEPA/SWIFT) на рахунок Агента, зареєстрований в системі AITA. Інші способи оплати потребують окремої домовленості.

**7.4 **Валюта: євро (EUR). Комісія за конвертацію валют покладається на Агента.

**7.5 **Податки: Агент самостійно декларує і сплачує всі податкові зобов'язання за отриманим доходом. AITA не є податковим агентом Агента.

**8. Рівні, бейджі та гейміфікація**

**8.1 **Дашборд в Telegram-боті в реальному часі: поточний Рівень і % Маржі; накопичений оборот і прогрес до наступного рівня; пасивний дохід (якщо Агент є Рекрутером); рейтинг; історія виплат.

**8.2 **Бейджі за результатами:

  ---------------- ------------------------------ -----------------------------------------
  **Бейдж**        **Умова отримання**            **Нагорода**
  🔥 Streak         3 Підтверджені угоди поспіль   +5% бонус до наступної угоди
  🏆 First Deal     Перша Підтверджена угода       Бонусне повідомлення + значок в профілі
  ⚡ Level Up       Перехід на новий рівень        Повідомлення + оновлена картка агента
  👑 Weekly King    \#1 тижневого рейтингу         Публічне виділення в боті
  🤝 Team Builder   5+ активних агентів у мережі   Спеціальний статус рекрутера
  ---------------- ------------------------------ -----------------------------------------

**9. Невиключність і гнучкість**

**9.1 **Ця Угода є невиключною. Агент вільний поєднувати роботу в AITA з будь-якою іншою діяльністю без згоди AITA.

**9.2 **Немає мінімальних зобов'язань щодо обороту, кількості угод або активності. AITA не гарантує мінімального потоку лідів або замовлень.

**9.3 **Ця Угода не створює трудових відносин, партнерства або спільного підприємства. Агент не отримує соціальних гарантій чи зарплати від AITA.

**10. Конфіденційність**

**10.1 **Агент зобов'язаний зберігати конфіденційність: (а) Страйк-прайсів і відносин з постачальниками; (б) даних покупців; (в) моделі розподілу маржі, логіки Telegram-бота і внутрішніх процесів AITA; (г) будь-якої іншої пропрієтарної інформації AITA.

**10.2 **Обов'язок конфіденційності діє протягом 24 місяців після припинення дії Угоди.

**11. Антиобхідне застереження**

**11.1 **Протягом дії цієї Угоди та протягом 12 місяців після її припинення Агенту забороняється: (а) прямо контактувати або укладати угоди з покупцями, залученими через AITA, обходячи платформу; (б) передавати постачальників, ціни або інформацію AITA конкурентам.

**11.2 **Порушення § 11.1 дає AITA право на стягнення щтрафних санкцій в розмірі більшого з (а) €5 000 або (б) суми маржі, яку AITA отримала б з обхідної угоди.

**12. Строк дії та розірвання**

**12.1 **Ця Угода набирає чинності з Дати набрання чинності і діє один (1) рік з автоматичною пролонгацією. Будь-яка зі сторін може відмовитись від пролонгації, повідомивши за 30 днів.

**12.2 **Розірвання з ініціативи: будь-яка зі сторін може розірвати угоду з попередженням 30 днів.

**12.3 **Негайне розірвання AITA: AITA може негайно розірвати Угоду у разі порушення § 10 (конфіденційність) або § 11 (антиобхід), прийняття оплати від покупця напряму або шахрайства.

**12.4 **Наслідки: доступ до Telegram-боту відключається; нараховані, але не виплачені частки Маржі залишаються до виплати; обов'язки за § 10--11 зберігаються.

**13. Договірне право та вирішення спорів**

**13.1 **Ця Угода регулюється законодавством Королівства Іспанія.

**13.2 **Спори вирішуються шляхом обов'язкового арбітражу за Правилами Corte de Arbitraje de Madrid (CAM), місце проведення --- Мадрид. Мова арбітражу: українська або англійська --- за домовленістю сторін.

**14. Прикінцеві положення**

**14.1 **Ця Угода є повним договором між Сторонами щодо ролі Агента в мережі AITA.

**14.2 **AITA може оновлювати каталог, Страйк-прайси і пороги рівнів з попередженням 7 днів через Telegram-бот або email. Зміни до умов винагороди (§ 6) потребують письмової згоди.

**14.3 **Українська версія є основною. У разі розбіжностей між мовними версіями перевагу має українська.

**15. Підписання**

**Цію Агентську угоду укладено Сторонами станом на дату, зазначену вище.**

+----------------------------------------------------------------------------+----------------------------------------------------------------------------+
| **AITA WORLD, S.L. (Принципал)**                                           | **АГЕНТ**                                                                  |
|                                                                            |                                                                            |
| Підпис: _________________________________ | Підпис: _________________________________ |
|                                                                            |                                                                            |
| Ім'я: Dmytro Mekhed                                                        | Ім'я:                                                                      |
|                                                                            |                                                                            |
| Посада: Director                                                           | Telegram:                                                                  |
|                                                                            |                                                                            |
| Дата: _________________________________   | Дата: _________________________________   |
+----------------------------------------------------------------------------+----------------------------------------------------------------------------+


---

# ═══ PROFILE 7 — RECRUITER: Partner Agreement (EN) ═══

**PARTNER AGREEMENT**

**AITA Agent Network --- Recruiter / Network Partner**

*Passive Income and Agent Network Management Agreement*

This Partner Agreement (\"Agreement\") is entered into as of _____________ (the \"Effective Date\"), between:

+-----------------------------------------+--------------------------------------------------------------------------------+
| **AITA WORLD, S.L.**                    | **PARTNER (RECRUITER)**                                                        |
|                                         |                                                                                |
| Role: Platform Operator                 | Role: Network Partner / Recruiter                                              |
|                                         |                                                                                |
| CIF: B75859744                          | [Full Name / Legal Name:                                    ]      |
|                                         |                                                                                |
| Sabino Arana, 8-2, 48013 Bilbao, España | [Country:                                                        ] |
|                                         |                                                                                |
| Email: d.mekhed\@aita.world             | [ID / Tax Number:                                            ]     |
|                                         |                                                                                |
|                                         | [Contact Email:                                              ]     |
|                                         |                                                                                |
|                                         | [Telegram Handle:                                            ]     |
+-----------------------------------------+--------------------------------------------------------------------------------+

**1. Purpose and Scope**

**1.1 **AITA operates a B2B trading platform with a multi-level agent network. Under the Agent Agreement, individual Agents find B2B buyers for AITA\'s product catalogue (solar energy equipment, industrial equipment, construction and engineering materials) and earn a share of the transaction margin.

**1.2 **Partner (Recruiter) agrees to recruit, onboard, and support independent Agents into the AITA network (\"Partner\'s Agent Network\") and, in return, earns a passive Recruiter Share from every Confirmed Transaction closed by Agents in their network.

**1.3 **Partner may simultaneously hold an active Agent Agreement with AITA and personally close transactions. This Agreement governs only the Recruiter function and passive income mechanics.

**2. Definitions**

**2.1 **Agent: An individual who has signed a valid Agent Agreement with AITA and has been onboarded to the AITA network by or under Partner.

**2.2 **Partner\'s Agent Network: All Agents onboarded by Partner (direct recruits). Does not include Agents recruited by Partner\'s Agents (no multi-level chaining beyond one degree).

**2.3 **Confirmed Transaction: A transaction by any Agent in Partner\'s Agent Network where AITA has received full client payment.

**2.4 **Margin: Client Price minus Strike Price on a given transaction (defined per Agent Agreement §2.3).

**2.5 **AITA Platform Fee: 20% of Margin, always retained by AITA.

**2.6 **Agent Pool: 80% of Margin (Margin minus AITA Platform Fee), split between Agent and Partner (Recruiter).

**2.7 **Recruiter Share: Partner\'s share of the Agent Pool. Partner determines the exact split for each Agent within the bounds set by the Agent\'s Level (see §4).

**3. Partner Obligations**

**3.1 **Partner shall: (a) recruit Agents by introducing them to AITA and facilitating their Agent Agreement signing; (b) onboard new Agents to the Telegram bot and explain the AITA agent model; (c) set and communicate each Agent\'s initial Margin share percentage at onboarding; (d) provide reasonable guidance and motivation to Agents in their network; (e) ensure Agents in their network comply with AITA\'s product, pricing, and conduct policies.

**3.2 **Partner shall not: (a) promise Agents guaranteed income or minimum earnings; (b) allow sub-recruitment (Agents recruited by Partner\'s Agents earn Recruiter Share for Partner, not a third level); (c) grant Agents access credentials or technical tools beyond those provided by AITA.

**4. Recruiter Share Model**

**4.1 **On every Confirmed Transaction by any Agent in Partner\'s Agent Network, the Agent Pool (80% of Margin) is split as follows:

  ----------------- -------------------- ------------------------ ---------------------------- ---------------------- ------------------------------
  **Agent Level**   **Agent Turnover**   **Agent Min (of 80%)**   **Recruiter Max (of 80%)**   **AITA (of Margin)**   **Recruiter Can Give More?**
  **Level 1**       €0 -- €15,000        30%                      50%                          20%                    Yes
  **Level 2**       €15,001 -- €50,000   45%                      35%                          20%                    Yes
  **Level 3**       €50,001 +            60%                      20%                          20%                    Yes
  ----------------- -------------------- ------------------------ ---------------------------- ---------------------- ------------------------------

**4.2 **Recruiter Flexibility: Partner may increase an Agent\'s share above the minimum stated in §4.1, thereby reducing Partner\'s own Recruiter Share. This is Partner\'s primary tool for motivating high-performing Agents. Any adjustment is made via the Telegram bot and takes effect immediately for future transactions.

**4.3 **No Chaining: Partner earns Recruiter Share only from Agents they directly recruited. Agents in Partner\'s network who themselves recruit new Agents become Recruiters in their own right under separate Partner Agreements. There is no cascading or multi-level passive income between Recruiters.

**4.4 **Illustrative Network Earnings (monthly, 10 active Agents):

  ---------------------------------- ----------- ---------------------------------- ---------------------- ------------------------ --------------------------
  **Agent Group**                    **Level**   **Avg Monthly Turnover / Agent**   **Avg Margin (15%)**   **Recruiter % of 80%**   **Partner Passive / mo**
  5 Agents                           Level 1     €5,000                             €750                   50%                      €375 × 5 = €1,875
  3 Agents                           Level 2     €12,000                            €1,800                 35%                      €630 × 3 = €1,890
  2 Agents                           Level 3     €25,000                            €3,750                 20%                      €750 × 2 = €1,500
  **TOTAL passive income / month**                                                  **€5,265**                                      
  ---------------------------------- ----------- ---------------------------------- ---------------------- ------------------------ --------------------------

Note: The above is illustrative. Actual earnings depend on Agent activity, margin achieved, and Partner\'s chosen split settings.

**5. Team Builder Status**

**5.1 **Partner automatically receives \"Team Builder\" status in the AITA Telegram bot upon reaching five (5) or more active Agents in their network (at least one Confirmed Transaction per Agent within the last 90 days).

**5.2 **Team Builder benefits include: (a) special badge and designation in the Telegram bot; (b) priority access to new product launches and promotional pricing for their Agent network; (c) dedicated AITA account manager contact for network support.

**6. Passive Income Payouts**

**6.1 **Partner\'s Recruiter Share is calculated automatically for each Confirmed Transaction by Agents in Partner\'s network and paid within five (5) business days of transaction confirmation.

**6.2 **Notifications: Partner receives automatic Telegram bot notification for each passive income payout: \"💸 Your agent \[Name\] closed a deal. Your passive income: +€\[amount\].\"

**6.3 **Payment method, currency, and tax treatment are as per Agent Agreement §7.3--§7.5 (if Partner holds a concurrent Agent Agreement) or as agreed in writing.

**7. Confidentiality and Non-Circumvention**

**7.1 **All confidentiality obligations from Agent Agreement §10 apply in full to Partner, with respect to AITA\'s pricing, supplier relationships, margin model, and client data.

**7.2 **Partner shall not use knowledge of AITA\'s agent network structure, client base, or pricing to build or operate a competing platform or supply chain.

**7.3 **Partner shall not poach Agents from AITA\'s network for a competing platform during the term of this Agreement and for twelve (12) months after termination.

**8. Term and Termination**

**8.1 **This Agreement commences on the Effective Date and continues for one (1) year, with automatic annual renewal unless either Party gives thirty (30) days\' written notice of non-renewal.

**8.2 **AITA may terminate this Agreement immediately if Partner: (a) breaches confidentiality (§7); (b) engages in fraud or misrepresentation; (c) attempts to poach Agents from AITA\'s network.

**8.3 **Upon termination: (a) Partner ceases to receive Recruiter Shares for transactions occurring after the termination date; (b) accrued but unpaid Recruiter Shares for Confirmed Transactions prior to termination remain payable; (c) Agents previously recruited by Partner retain their Agent Agreements independently.

**9. Governing Law and Dispute Resolution**

**9.1 **This Agreement is governed by the laws of the Kingdom of Spain.

**9.2 **Any disputes shall be resolved by binding arbitration under the Rules of the Corte de Arbitraje de Madrid (CAM), Madrid, Spain, in English (or Ukrainian / Russian by mutual agreement).

**10. Execution**

**IN WITNESS WHEREOF, the Parties have executed this Partner Agreement as of the date first written above.**

+--------------------------------------------------------------------------+--------------------------------------------------------------------------+
| **AITA WORLD, S.L.**                                                     | **PARTNER (RECRUITER)**                                                  |
|                                                                          |                                                                          |
| By: _________________________________   | By: _________________________________   |
|                                                                          |                                                                          |
| Name: Dmytro Mekhed                                                      | Name:                                                                    |
|                                                                          |                                                                          |
| Title: Director                                                          | Telegram:                                                                |
|                                                                          |                                                                          |
| Date: _________________________________ | Date: _________________________________ |
+--------------------------------------------------------------------------+--------------------------------------------------------------------------+


---

# ═══ PROFILE 7 — RECRUITER: Партнерська угода (UA) ═══

**ПАРТНЕРСЬКА УГОДА**

**AITA Agent Network --- Рекрутер / Мережевий партнер**

*Угода про пасивний дохід та управління агентською мережею*

Ця Партнерська угода («Угода») укладена   _____________    («Дата набрання чинності»), між:

+------------------------------------------+----------------------------------------------------------------------------+
| **AITA WORLD, S.L.**                     | **ПАРТНЕР (РЕКРУТЕР)**                                                     |
|                                          |                                                                            |
| Роль: Оператор платформи                 | Роль: Мережевий партнер / Рекрутер                                         |
|                                          |                                                                            |
| CIF: B75859744                           | [ПІБ / Назва:                                            ]     |
|                                          |                                                                            |
| Sabino Arana, 8-2, 48013 Bilbao, Іспанія | [Країна:                                                     ] |
|                                          |                                                                            |
| Email: d.mekhed\@aita.world              | [ІПН / Податковий номер:                               ]       |
|                                          |                                                                            |
|                                          | [Email:                                                      ] |
|                                          |                                                                            |
|                                          | [Telegram:                                                   ] |
+------------------------------------------+----------------------------------------------------------------------------+

**1. Предмет та сфера дії**

**1.1 **AITA експлуатує B2B торгову платформу з багаторівневою агентською мережею. За Агентською угодою індивідуальні Агенти знаходять B2B-покупців для товарів із каталогу AITA (сонячне енергетичне обладнання, промислове електрообладнання, будівельні та інженерні матеріали) і отримують частку маржі з угоди.

**1.2 **Партнер (Рекрутер) зобов'язується залучати, адаптувати та підтримувати незалежних Агентів в мережу AITA («Мережа Партнера») і отримувати за це пасивну частку Рекрутера з кожної Підтвердженої угоди, укладеної Агентами з його мережі.

**1.3 **Партнер може одночасно мати Діючу Агентську угоду з AITA і особисто укладати угоди. Ця Угода регулює виключно функцію Рекрутера і пасивний дохід.

**2. Визначення**

**2.1 **Агент --- фізична особа, яка підписала чинну Агентську угоду з AITA і залучена до мережі AITA Партнером.

**2.2 **Мережа Партнера --- усі Агенти, набрані безпосередньо Партнером (прямі рекрути). Не включає Агентів, набраних Агентами Партнера (без багаторівневого ланцюжуцю).

**2.3 **Підтверджена угода --- угода будь-якого Агента з Мережі Партнера, за якою AITA отримала повну оплату від B2B-покупця.

**2.4 **Маржа --- різниця між Клієнтською ціною та Страйк-прайсом (визначено в Агентській угоді §2.3).

**2.5 **Платформовий збір AITA: 20% Маржі, завжди утримується AITA.

**2.6 **Фонд 80% --- 80% Маржі (Маржа мінус Платформовий збір AITA), які діляться між Агентом і Партнером.

**2.7 **Частка Рекрутера --- частка Фонду 80%, яку отримує Партнер. Партнер самостійно визначає розподіл для кожного Агента в межах, встановлених Рівнем Агента (див. §4).

**3. Обов\'язки Партнера**

**3.1 **Партнер зобов\'язаний: (а) залучати Агентів, ознайомлюючи їх з AITA і сприяючи підписанню Агентської угоди; (б) адаптувати нових Агентів до Telegram-боту і пояснювати модель AITA; (в) встановлювати та повідомляти про початковий відсоток частки Маржі кожного Агента при онбордингу; (г) надавати розумну підтримку та мотивацію Агентам у своїй мережі; (д) стежити за дотриманням Агентами політики AITA.

**3.2 **Партнеру забороняється: (а) обіцяти Агентам гарантований дохід або мінімальні виплати; (б) дозволяти суб-рекрутинг (Агенти, набрані Агентами Партнера, стають Рекрутерами в рамках окремих Партнерських угод; багаторівневого ланцюжуцю немає); (в) надавати Агентам доступ або інструменти, не надані AITA.

**4. Модель частки Рекрутера**

**4.1 **З кожної Підтвердженої угоди будь-якого Агента з Мережі Партнера, Фонд 80% (Маржа мінус 20% AITA) ділиться наступним чином:

  ------------------- -------------------- -------------------------- ------------------------------ ---------------------- -------------------------------
  **Рівень Агента**   **Оборот Агента**    **Агент мін. (від 80%)**   **Рекрутер макс. (від 80%)**   **AITA (від Маржі)**   **Партнер може дати більше?**
  **Рівень 1**        €0 -- €15 000        30%                        50%                            20%                    Так
  **Рівень 2**        €15 001 -- €50 000   45%                        35%                            20%                    Так
  **Рівень 3**        €50 001+             60%                        20%                            20%                    Так
  ------------------- -------------------- -------------------------- ------------------------------ ---------------------- -------------------------------

**4.2 **Гнучкість Рекрутера: Партнер може підвищити частку Агента понад мінімум, зменшуючи власну частку. Це --- головний інструмент мотивації Агентів. Будь-яке коригування здійснюється через Telegram-бот і набирає чинності негайно для майбутніх угод.

**4.3 **Без ланцюжуцю: Партнер отримує Частку Рекрутера лише від Агентів, яких він залучив особисто. Агенти з Мережі Партнера, які самі рекрутують інших, стають Рекрутерами за окремими Партнерськими угодами.

**4.4 **Орієнтовний приклад заробітку мережі (місяць, 10 активних агентів):

  ------------------------------------- ------------ ---------------------- ---------------------- -------------------------------- -----------------------------
  **Група агентів**                     **Рівень**   **Сер. міс. оборот**   **Сер. Маржа (15%)**   **Частка Рекрутера % від 80%**   **Пасивний дохід Партнера**
  5 агентів                             Рівень 1     €5 000                 €750                   50%                              €375 × 5 = €1 875
  3 агенти                              Рівень 2     €12 000                €1 800                 35%                              €630 × 3 = €1 890
  2 агенти                              Рівень 3     €25 000                €3 750                 20%                              €750 × 2 = €1 500
  **ЗАГАЛОМ пасивного доходу / міс.**                                       **€5 265**                                              
  ------------------------------------- ------------ ---------------------- ---------------------- -------------------------------- -----------------------------

Примітка: наведені цифри є орієнтовними. Фактичний дохід залежить від активності Агентів, досягнутої маржі та налаштувань розподілу Партнера.

**5. Статус «Будівник команди» (Team Builder)**

**5.1 **Партнер автоматично отримує статус «Будівник» після досягнення п'яти (5) або більше активних Агентів (щонайменше одна Підтверджена угода за останні 90 днів).

**5.2 **Переваги статусу «Будівник»: (а) спеціальний значок і означення в Telegram-боті; (б) пріоритетний доступ до нових продуктів і акційних цін для своєї мережі; (в) дедикований менеджер з боку AITA для підтримки мережі.

**6. Виплати пасивного доходу**

**6.1 **Частка Рекрутера автоматично розраховується для кожної Підтвердженої угоди та виплачується протягом п'яти (5) робочих днів з моменту її підтвердження.

**6.2 **Повідомлення: Партнер отримує автоматичне повідомлення Telegram-боту за кожну виплату: «💸 Ваш агент \[Name\] уклав угоду. Ваш пасивний дохід: +€\[sum\].»

**6.3 **Спосіб виплати, валюта і податковий режим аналогічні §7.3--7.5 Агентської угоди або погоджені письмово.

**7. Конфіденційність і антиобхідне застереження**

**7.1 **Всі зобов\'язання щодо конфіденційності з Агентської угоди §10 повною мірою стосуються Партнера щодо цін утворення, відносин з постачальниками, моделі маржі та даних клієнтів.

**7.2 **Партнер не має права використовувати інформацію про структуру мережі, клієнтську базу або ціноутворення AITA для будівництва або експлуатації конкурентної платформи.

**7.3 **Партнер не має права переманювати Агентів з мережі AITA на конкурентну платформу протягом дії цієї Угоди та 12 місяців після її припинення.

**8. Строк дії та розірвання**

**8.1 **Ця Угода набирає чинності з Дати набрання чинності і діє один (1) рік з автоматичною пролонгацією. Будь-яка зі сторін може відмовитись від пролонгації, попередивши за 30 днів.

**8.2 **Негайне розірвання AITA: AITA може негайно розірвати Угоду у разі порушення Партнером: (а) конфіденційності (§7); (б) шахрайства або введення в оману; (в) переманювання Агентів.

**8.3 **Наслідки: (а) Партнер перестає отримувати Частку Рекрутера за угодами, укладеними після дати припинення; (б) нараховані, але не виплачені частки залишаються до виплати; (в) Агенти зберігають свої Агентські угоди у повному обсязі.

**9. Договірне право та вирішення спорів**

**9.1 **Ця Угода регулюється законодавством Королівства Іспанія.

**9.2 **Спори вирішуються шляхом обов'язкового арбітражу за Правилами Corte de Arbitraje de Madrid (CAM), місце проведення --- Мадрид. Мова: українська або англійська --- за домовленістю сторін.

**10. Підписання**

**Цю Партнерську угоду укладено Сторонами станом на дату, зазначену вище.**

+----------------------------------------------------------------------------+----------------------------------------------------------------------------+
| **AITA WORLD, S.L.**                                                       | **ПАРТНЕР (РЕКРУТЕР)**                                                     |
|                                                                            |                                                                            |
| Підпис: _________________________________ | Підпис: _________________________________ |
|                                                                            |                                                                            |
| Ім'я: Dmytro Mekhed                                                        | Ім'я:                                                                      |
|                                                                            |                                                                            |
| Посада: Director                                                           | Telegram:                                                                  |
|                                                                            |                                                                            |
| Дата: _________________________________   | Дата: _________________________________   |
+----------------------------------------------------------------------------+----------------------------------------------------------------------------+


---

# ═══ PROFILE 8 — MARKETING: Marketing Pool Agreement (EN) ═══

**MARKETING POOL MEMBERSHIP AGREEMENT**

*Pooled Marketing Investment & Lead Allocation*

+----------------------------------------+-------------------------------------------+
| **AITA WORLD, S.L.**                   | **MEMBER**                                |
|                                        |                                           |
| *Service Provider*                     | \[Company / Full name: ________\] |
|                                        |                                           |
| CIF: B75859744                         | \[Country: ________\]             |
|                                        |                                           |
| Sabino Arana, 8-2, 48013 Bilbao, Spain | \[Reg. / Tax No.: ________\]      |
|                                        |                                           |
| Email: d.mekhed\@aita.world            | \[Representative: ________\]      |
|                                        |                                           |
| Web: aita.world                        | \[Email: ________\]               |
+----------------------------------------+-------------------------------------------+

*(together --- \"Parties\", each individually --- \"Party\")*

**1. Subject Matter**

**1.1.** AITA operates a pooled marketing fund (the \"Marketing Pool\") for participants in the AITA renewable energy ecosystem. The Marketing Pool replaces the individual Lead-as-a-Service model with a collective investment and lead distribution mechanism.

**1.2.** The Member undertakes to make periodic Pool Contributions and in return receives allocated Qualified Leads and business opportunities in accordance with the Allocation Policy (Annex 1).

**1.3.** Territory: as specified in the applicable Contribution Order. Expansion is possible upon mutual agreement.

**2. Definitions**

**2.1. Marketing Pool** --- a collective fund formed by Contributions from all Members, managed by AITA for the purpose of lead generation, advertising campaigns, and demand creation across the AITA ecosystem.

**2.2. Pool Contribution** --- a periodic monetary payment made by the Member into the Marketing Pool, as defined in the Contribution Order.

**2.3. Allocation Policy** --- the rules governing the distribution of leads and opportunities among Pool Members, including fairness criteria, SLA, and discipline rules (Annex 1).

**2.4. Qualified Lead** --- a B2B or B2C contact that has passed the AITA automated qualification funnel (location, energy needs, readiness to engage) and has been delivered to the Member via the AITA platform.

**2.5. Contribution Order** --- a signed order form specifying the Member\'s contribution amount, payment schedule, territory, and allocated lead volume range (Annex 2).

**2.6. Lead Allocator** --- the automated AITA platform module that distributes incoming leads among Members based on Allocation Policy parameters.

**2.7. Pool Membership Status** --- the Member\'s active status in the Marketing Pool, contingent on timely Contributions and compliance with the Allocation Policy SLA.

**2.8. Success Fee (Optional)** --- a commission of 1.5% of the deal value, applicable only if explicitly activated in the Contribution Order. Accrued after actual payment by the end client.

**3. Marketing Pool Mechanism**

**3.1.** Pool Formation. AITA aggregates all Member Contributions into a single Marketing Pool fund. AITA manages the Pool exclusively for lead generation, advertising campaigns (Google, Meta, LinkedIn, Telegram), content marketing, and demand creation activities.

**3.2.** Pool Allocation. Incoming leads and opportunities generated through Pool-funded activities are distributed among Members via the Lead Allocator module in accordance with the Allocation Policy (Annex 1).

**3.3.** Fairness & SLA. The Allocation Policy ensures:

-   Proportional distribution based on Contribution size and territory

-   Lead response SLA (Member must respond within 24 hours of allocation)

-   Discipline: failure to respond within SLA results in lead reallocation and potential penalty per Annex 1

-   Transparency: Member has real-time access to Pool performance dashboard (spend, leads generated, allocation, conversion)

**3.4.** No Individual Landing Pages. AITA does not create or host individual landing pages for Members (FF:disable_landing_pages). All lead generation flows through the centralized Pool infrastructure.

**3.5.** Token-Ready. Pool Contributions may be paid in fiat (EUR) or, when enabled, via AITA Credits. The underlying mechanism wraps PayWithFiat() or BuyCreditsThenPay() without altering the Pool formula.

**4. Contribution & Payment**

**4.1.** The Member\'s Pool Contribution amount and schedule are defined in the Contribution Order (Annex 2).

**4.2.** Payment schedule:

  ------------------------ -------------------------------------------------------------
  **Parameter**            **Terms**
  Pool Contribution        As per Contribution Order (monthly / quarterly)
  Payment event            Advance payment before the campaign period
  Success Fee (optional)   1.5% of deal value, 14 calendar days after client payment
  Currency                 EUR. Conversion costs borne by the Member
  Payment method           Bank transfer (SEPA/SWIFT) or AITA Credits (when available)
  ------------------------ -------------------------------------------------------------

**4.3.** Unspent Pool balance at period end carries over to the next period. AITA provides a monthly Pool spend report.

**4.4.** AITA reserves the right to set a minimum Pool Contribution threshold, published in the current Contribution Order template.

**5. Platform Services Included**

Members of the Marketing Pool receive the following platform services at no additional charge:

  ---------------------------- --------------------------------------------------------------------------------------------------------------
  **Service**                  **Description**
  Sales Node (Telegram Bot)    Auto-collection of buyer data, Deal_ID creation, PDF proposals with 3 price tiers. Up to 7 bots per Member.
  Pool Performance Dashboard   Real-time reporting: spend, CPL, leads generated, allocation, conversion rates.
  Lead Allocator               Automated lead distribution based on Allocation Policy parameters.
  Agent Commission Engine      Automated agent commission calculation if Member uses AITA Agent Network.
  Lot Aggregation              Combining small orders into batches for price optimization (up to 7% savings).
  ---------------------------- --------------------------------------------------------------------------------------------------------------

> *AITA Workspace (AI-CRM + IP telephony) is available as a separate subscription at €25/user/month if required.*

**6. Rights and Obligations**

**6.1. AITA undertakes to:**

-   Manage the Marketing Pool funds exclusively for lead generation and demand creation activities

-   Distribute leads in accordance with the Allocation Policy (Annex 1)

-   Provide monthly Pool spend and performance reports

-   Maintain and optimize advertising campaigns continuously

-   Deliver Qualified Leads within 24 hours of entering the funnel

-   Provide technical support and regular platform updates

**6.2. The Member undertakes to:**

-   Make timely Pool Contributions in accordance with the Contribution Order

-   Respond to allocated leads within the SLA timeframe (24 hours)

-   Process leads in the AITA platform and update deal statuses

-   Notify AITA of closed deals for Success Fee accrual (if applicable)

-   Provide AITA with necessary materials for campaign setup (logo, marketing materials, product catalog)

**7. Confidentiality**

**7.1.** Each Party undertakes to maintain strict confidentiality of any proprietary and commercial information received in connection with this Agreement, including: Pool Contribution amounts, allocation algorithms, targeting parameters, lead data, and client data.

**7.2.** Confidentiality obligations remain in effect for 2 (two) years after termination of this Agreement.

**8. Non-Circumvention**

**8.1.** The Member shall not, directly or through third parties, contact or engage any lead, client, partner, or supplier introduced by AITA through the Marketing Pool, bypassing the AITA platform. This obligation applies for 12 (twelve) months from the last lead delivery.

**8.2.** Breach of this clause entitles AITA to a contractual penalty of €5,000 per incident, without prejudice to further damages.

**9. Data Protection**

**9.1.** The Parties agree to process personal data in compliance with Regulation (EU) 2016/679 (GDPR). AITA acts as Data Controller for lead data; the Member acts as Data Controller for its own client data received through the platform.

**9.2.** A Data Processing Addendum (DPA) shall be executed separately if required by the nature or volume of data processing.

**10. Term and Termination**

**10.1.** This Agreement enters into force on the Effective Date and is valid for 6 (six) months with automatic renewal for successive 6-month periods. Either Party may opt out of renewal with 30 days\' written notice.

**10.2.** Termination for convenience: either Party may terminate with 30 days\' written notice. The Member\'s Contribution for the current period is non-refundable.

**10.3.** Immediate termination by AITA: in case of (a) overdue Contribution by more than 14 calendar days; (b) breach of confidentiality or non-circumvention; (c) fraud or provision of false information.

**10.4.** Post-termination: accrued but unpaid Success Fees (if applicable) and any allocated but unprocessed leads remain subject to this Agreement\'s terms.

**11. Force Majeure**

**11.1.** Neither Party shall be liable for failure or delay in performing its obligations due to circumstances beyond its reasonable control (\"Force Majeure\"), including but not limited to: natural disasters, war, terrorism, pandemics, changes in applicable law, sanctions, or failure of third-party advertising platforms.

**11.2.** The affected Party shall notify the other Party within 5 business days. If Force Majeure persists for more than 60 days, either Party may terminate this Agreement.

**12. Liability**

**12.1.** AITA does not guarantee a specific volume of leads or deal closures, but undertakes to maintain active campaigns, continuously optimize targeting, and distribute leads fairly in accordance with the Allocation Policy.

**12.2.** AITA\'s total liability is limited to the amount of Pool Contributions actually paid by the Member for the relevant period.

**12.3.** AITA bears no liability for: (a) actions of third-party advertising platforms (Google, Meta, LinkedIn); (b) lead behaviour after delivery; (c) Force Majeure circumstances.

**13. Governing Law and Dispute Resolution**

**13.1.** This Agreement is governed by the laws of the Kingdom of Spain.

**13.2.** The Parties shall seek to resolve disputes amicably within 30 calendar days. If unresolved, the dispute is referred to the Corte de Arbitraje de Madrid (CAM), seated in Madrid. Arbitration language: English or Ukrainian --- as agreed by the Parties.

**14. Language**

**14.1.** This Agreement is executed in English and Ukrainian. In case of discrepancy, the English version shall prevail unless the Parties agree otherwise in writing.

**15. Miscellaneous**

**15.1.** Amendments to this Agreement shall be made in writing and signed by both Parties.

**15.2.** If any provision of this Agreement is held invalid, the remaining provisions shall remain in full force.

**15.3.** This Agreement, together with its Annexes, constitutes the entire agreement between the Parties regarding Marketing Pool membership.

**Annexes**

**Annex 1 --- Allocation Policy (fairness criteria, SLA, discipline, reallocation rules)**

**Annex 2 --- Contribution Order Template (amount, schedule, territory, lead volume range)**

**Signatures**

+-----------------------------------------------------+--------------------------------------------------------+
| **AITA WORLD, S.L.**                                | **MEMBER**                                             |
|                                                     |                                                        |
| Signature: ____________________ | Signature: ____________________    |
|                                                     |                                                        |
| Name: Dmytro Mekhed                                 | Name / Title: ____________________ |
|                                                     |                                                        |
| Title: Director                                     | Company: ____________________      |
|                                                     |                                                        |
| Date: ____________________      | Date: ____________________         |
+-----------------------------------------------------+--------------------------------------------------------+


---

# ═══ PROFILE 8 — MARKETING: Договір Маркетинговий Пул (UA) ═══

**ДОГОВІР УЧАСТІ В МАРКЕТИНГОВОМУ ПУЛІ**

*Пайова маркетингова інвестиція та розподіл лідів*

+----------------------------------------+-------------------------------------------+
| **AITA WORLD, S.L.**                   | **УЧАСНИК**                               |
|                                        |                                           |
| *Постачальник послуг*                  | \[Компанія / ПІБ: ________\]      |
|                                        |                                           |
| CIF: B75859744                         | \[Країна: ________\]              |
|                                        |                                           |
| Sabino Arana, 8-2, 48013 Bilbao, Spain | \[Реєстр. / Податк. №: ________\] |
|                                        |                                           |
| Email: d.mekhed\@aita.world            | \[Представник: ________\]         |
|                                        |                                           |
| Web: aita.world                        | \[Email: ________\]               |
+----------------------------------------+-------------------------------------------+

*(разом --- «Сторони», кожна окремо --- «Сторона»)*

**1. Предмет договору**

**1.1.** AITA оперує спільним маркетинговим фондом («Маркетинговий Пул») для учасників екосистеми відновлюваної енергетики AITA. Маркетинговий Пул замінює індивідуальну модель Lead-as-a-Service на механізм колективного інвестування та розподілу лідів.

**1.2.** Учасник зобов'язується здійснювати періодичні Пайові Внески до Пулу та натомість отримує розподілені Кваліфіковані Ліди та бізнес-можливості відповідно до Політики Розподілу (Додаток 1).

**1.3.** Територія: згідно з відповідним Замовленням на Внесок. Розширення можливе за взаємною домовленістю.

**2. Визначення**

**2.1. Маркетинговий Пул** --- колективний фонд, сформований Внесками всіх Учасників, яким управляє AITA з метою лідогенерації, рекламних кампаній та створення попиту в екосистемі AITA.

**2.2. Пайовий Внесок** --- періодичний грошовий платіж Учасника до Маркетингового Пулу, визначений у Замовленні на Внесок.

**2.3. Політика Розподілу** --- правила розподілу лідів та можливостей між Учасниками Пулу, включаючи критерії справедливості, SLA та дисциплінарні правила (Додаток 1).

**2.4. Кваліфікований Лід** --- B2B або B2C контакт, який пройшов автоматизовану воронку кваліфікації AITA (локація, енергетичні потреби, готовність до взаємодії) та був доставлений Учаснику через платформу AITA.

**2.5. Замовлення на Внесок** --- підписана форма замовлення, що визначає суму Внеску, графік платежів, територію та орієнтовний діапазон обсягу лідів (Додаток 2).

**2.6. Розподільник Лідів** --- автоматизований модуль платформи AITA, який розподіляє вхідні ліди між Учасниками на основі параметрів Політики Розподілу.

**2.7. Статус Учасника Пулу** --- активний статус Учасника в Маркетинговому Пулі, обумовлений своєчасністю Внесків та дотриманням SLA Політики Розподілу.

**2.8. Success Fee (опціонально)** --- комісія 1,5% від суми угоди, застосовна лише якщо явно активована у Замовленні на Внесок. Нараховується після фактичної оплати кінцевим клієнтом.

**3. Механізм Маркетингового Пулу**

**3.1.** Формування Пулу. AITA агрегує всі Внески Учасників в єдиний фонд Маркетингового Пулу. AITA управляє Пулом виключно для лідогенерації, рекламних кампаній (Google, Meta, LinkedIn, Telegram), контент-маркетингу та створення попиту.

**3.2.** Розподіл із Пулу. Вхідні ліди та можливості, згенеровані через діяльність, фінансовану Пулом, розподіляються між Учасниками через модуль Розподільника Лідів відповідно до Політики Розподілу (Додаток 1).

**3.3.** Справедливість та SLA. Політика Розподілу забезпечує:

-   Пропорційний розподіл на основі розміру Внеску та території

-   SLA реагування на ліди (Учасник має відповісти протягом 24 годин з моменту розподілу)

-   Дисципліна: невідповідність SLA призводить до перерозподілу ліда та можливого штрафу згідно Додатку 1

-   Прозорість: Учасник має доступ у реальному часі до дашборду ефективності Пулу (витрати, ліди, розподіл, конверсія)

**3.4.** Без індивідуальних лендінгів. AITA не створює та не хостить індивідуальні лендінг-сторінки для Учасників (FF:disable_landing_pages). Уся лідогенерація проходить через централізовану інфраструктуру Пулу.

**3.5.** Token-Ready. Пайові Внески можуть бути сплачені у фіаті (EUR) або, за наявності, через AITA Credits. Базовий механізм обгортає PayWithFiat() або BuyCreditsThenPay() без зміни формули Пулу.

**4. Внесок та оплата**

**4.1.** Розмір та графік Пайового Внеску Учасника визначаються в Замовленні на Внесок (Додаток 2).

**4.2.** Графік платежів:

  -------------------- ------------------------------------------------------------------
  **Параметр**         **Умови**
  Пайовий Внесок       Згідно Замовлення на Внесок (щомісячно / щоквартально)
  Подія оплати         Авансовий платіж перед кампанійним періодом
  Success Fee (опц.)   1,5% від суми угоди, 14 календарних днів після оплати клієнтом
  Валюта               EUR. Витрати на конвертацію несе Учасник
  Спосіб оплати        Банківський переказ (SEPA/SWIFT) або AITA Credits (за наявності)
  -------------------- ------------------------------------------------------------------

**4.3.** Невитрачений залишок Пулу на кінець періоду переноситься на наступний період. AITA надає щомісячний звіт про витрати Пулу.

**4.4.** AITA залишає за собою право встановити мінімальний поріг Пайового Внеску, опублікований у поточному шаблоні Замовлення на Внесок.

**5. Послуги платформи, що включені**

Учасники Маркетингового Пулу отримують наступні послуги платформи без додаткової оплати:

  ----------------------------- -------------------------------------------------------------------------------------------------------------------
  **Послуга**                   **Опис**
  Sales Node (Telegram Bot)     Автоматичний збір даних покупця, створення Deal_ID, PDF-пропозиції з 3 ціновими рівнями. До 7 ботів на Учасника.
  Дашборд ефективності Пулу     Звітність у реальному часі: витрати, CPL, згенеровані ліди, розподіл, конверсія.
  Розподільник Лідів            Автоматизований розподіл лідів за параметрами Політики Розподілу.
  Калькулятор комісій агентів   Автоматичний розрахунок агентських комісій, якщо Учасник використовує Агентську Мережу AITA.
  Агрегація лотів               Об'єднання малих замовлень у партії для оптимізації ціни (до 7% економії).
  ----------------------------- -------------------------------------------------------------------------------------------------------------------

> *AITA Workspace (AI-CRM + IP-телефонія) доступний як окрема підписка за €25/користувач/місяць за потреби.*

**6. Права та обов'язки**

**6.1. AITA зобов'язується:**

-   Управляти коштами Маркетингового Пулу виключно для лідогенерації та створення попиту

-   Розподіляти ліди відповідно до Політики Розподілу (Додаток 1)

-   Надавати щомісячні звіти про витрати та ефективність Пулу

-   Підтримувати та безперервно оптимізувати рекламні кампанії

-   Доставляти Кваліфіковані Ліди протягом 24 годин після входу у воронку

-   Забезпечувати технічну підтримку та регулярні оновлення платформи

**6.2. Учасник зобов'язується:**

-   Своєчасно здійснювати Пайові Внески відповідно до Замовлення на Внесок

-   Реагувати на розподілені ліди в межах SLA (24 години)

-   Обробляти ліди на платформі AITA та оновлювати статуси угод

-   Повідомляти AITA про закриті угоди для нарахування Success Fee (за наявності)

-   Надавати AITA необхідні матеріали для налаштування кампаній (логотип, маркетингові матеріали, каталог продукції)

**7. Конфіденційність**

**7.1.** Кожна Сторона зобов'язується дотримуватись суворої конфіденційності щодо будь-якої комерційної інформації, отриманої у зв'язку з цим Договором, включаючи: розміри Пайових Внесків, алгоритми розподілу, параметри таргетингу, дані лідів та дані клієнтів.

**7.2.** Зобов'язання щодо конфіденційності залишаються чинними протягом 2 (двох) років після припинення дії цього Договору.

**8. Незаперечення (Non-Circumvention)**

**8.1.** Учасник не має права, прямо чи через третіх осіб, контактувати або залучати будь-який лід, клієнта, партнера чи постачальника, представленого AITA через Маркетинговий Пул, оминаючи платформу AITA. Це зобов'язання діє протягом 12 (дванадцяти) місяців з моменту останньої доставки ліда.

**8.2.** Порушення цього пункту надає AITA право на договірний штраф у розмірі €5 000 за кожний випадок, без шкоди для подальших вимог щодо відшкодування збитків.

**9. Захист даних**

**9.1.** Сторони погоджуються обробляти персональні дані відповідно до Регламенту (ЄС) 2016/679 (GDPR). AITA виступає Контролером Даних щодо даних лідів; Учасник виступає Контролером Даних щодо власних клієнтських даних, отриманих через платформу.

**9.2.** Додаток про обробку даних (DPA) укладається окремо, якщо це необхідно з огляду на характер або обсяг обробки даних.

**10. Строк та припинення**

**10.1.** Цей Договір набуває чинності з Дати Підписання та діє протягом 6 (шести) місяців з автоматичним продовженням на наступні 6-місячні періоди. Будь-яка Сторона може відмовитись від продовження за 30 днів письмового повідомлення.

**10.2.** Дострокове припинення: будь-яка Сторона може припинити Договір за 30 днів письмового повідомлення. Внесок Учасника за поточний період не підлягає поверненню.

**10.3.** Негайне припинення з боку AITA: у разі (а) прострочення Внеску більш ніж на 14 календарних днів; (б) порушення конфіденційності або незаперечення; (в) шахрайства або надання неправдивої інформації.

**10.4.** Після припинення: нараховані але несплачені Success Fee (за наявності) та будь-які розподілені але необроблені ліди залишаються предметом умов цього Договору.

**11. Форс-мажор**

**11.1.** Жодна Сторона не несе відповідальності за невиконання або затримку виконання своїх зобов'язань внаслідок обставин, що перебувають поза її розумним контролем («Форс-мажор»), включаючи, але не обмежуючись: стихійні лиха, війну, тероризм, пандемії, зміни законодавства, санкції або збої сторонніх рекламних платформ.

**11.2.** Постраждала Сторона повідомляє іншу Сторону протягом 5 робочих днів. Якщо Форс-мажор триває понад 60 днів, будь-яка Сторона може припинити цей Договір.

**12. Відповідальність**

**12.1.** AITA не гарантує конкретний обсяг лідів або закриття угод, але зобов'язується підтримувати активні кампанії, безперервно оптимізувати таргетинг та справедливо розподіляти ліди відповідно до Політики Розподілу.

**12.2.** Загальна відповідальність AITA обмежена сумою Пайових Внесків, фактично сплачених Учасником за відповідний період.

**12.3.** AITA не несе відповідальності за: (а) дії сторонніх рекламних платформ (Google, Meta, LinkedIn); (б) поведінку ліда після доставки; (в) обставини Форс-мажору.

**13. Застосовне право та вирішення спорів**

**13.1.** Цей Договір регулюється законодавством Королівства Іспанія.

**13.2.** Сторони намагаються вирішити спори мирним шляхом протягом 30 календарних днів. За відсутності врегулювання спір передається до Corte de Arbitraje de Madrid (CAM), місце проведення --- Мадрид. Мова арбітражу: англійська або українська --- за домовленістю Сторін.

**14. Мова**

**14.1.** Цей Договір укладено англійською та українською мовами. У разі розбіжностей англійська версія має перевагу, якщо Сторони не домовились іншим чином письмово.

**15. Інше**

**15.1.** Зміни до цього Договору вносяться письмово та підписуються обома Сторонами.

**15.2.** Якщо будь-яке положення цього Договору визнано недійсним, решта положень залишаються чинними.

**15.3.** Цей Договір разом із Додатками становить повну домовленість між Сторонами щодо участі в Маркетинговому Пулі.

**Додатки**

**Додаток 1 --- Політика Розподілу (критерії справедливості, SLA, дисципліна, правила перерозподілу)**

**Додаток 2 --- Шаблон Замовлення на Внесок (сума, графік, територія, орієнтовний обсяг лідів)**

**Підписи**

+--------------------------------------------------+---------------------------------------------------------+
| **AITA WORLD, S.L.**                             | **УЧАСНИК**                                             |
|                                                  |                                                         |
| Підпис: ____________________ | Підпис: ____________________        |
|                                                  |                                                         |
| Ім'я: Dmytro Mekhed                              | Ім'я / Посада: ____________________ |
|                                                  |                                                         |
| Посада: Director                                 | Компанія: ____________________      |
|                                                  |                                                         |
| Дата: ____________________   | Дата: ____________________          |
+--------------------------------------------------+---------------------------------------------------------+

