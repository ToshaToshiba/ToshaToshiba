<h1 align="center">DevUnit Lab 🔬</h1>

<p align="center">
  <img src="https://readme-typing-svg.herokuapp.com?font=Fira+Code&pause=1000&color=58A6FF&center=true&vCenter=true&width=480&lines=Engineering+Software+Unit;Telegram+Billing+%26+Ticket+Systems;Distributed+VPN+Infrastructure;DevOps+%2F+Python+%2F+n8n" alt="Typing SVG" />
</p>

<p align="center">
  <b>Антон Сергеев</b> — backend & infrastructure engineer, DevUnit Lab<br/>
  <a href="https://devunit-lab.ru">🇷🇺 devunit-lab.ru</a> • <a href="https://devunit-lab.business">🌍 devunit-lab.business</a><br/>
  <i>Moscow & Chisinau</i>
</p>

<p align="center">
  <a href="https://t.me/tosha_DevUnit">
    <img src="https://img.shields.io/badge/Telegram-tosha__DevUnit-2CA5E0?style=for-the-badge&logo=telegram&logoColor=white" alt="Telegram"/>
  </a>
</p>

---

### Чем занимаюсь

Строю системы, которые работают без меня: принимают деньги, ведут учёт, чинят себя по расписанию и присылают отчёт, когда что-то идёт не так.

Специализация — **асинхронные Telegram-сервисы с реальной бизнес-логикой**: биллинг, подписки, тикет-системы, корпоративный учёт. Это не боты-визитки — это продакшен с транзакциями, миграциями и живыми пользователями.

Отдельное направление — **суверенная сетевая инфраструктура**: распределённые VPN-трассы, маршрутизация трафика, администрирование узлов.

---

### 🛠 Технический арсенал

<p align="center">
  <img src="https://img.shields.io/badge/Python-3.11+-3776AB?style=for-the-badge&logo=python&logoColor=white" alt="Python"/>
  <img src="https://img.shields.io/badge/aiogram-3.x-2CA5E0?style=for-the-badge&logo=telegram&logoColor=white" alt="aiogram"/>
  <img src="https://img.shields.io/badge/asyncio-Concurrency-306998?style=for-the-badge&logo=python&logoColor=white" alt="asyncio"/>
  <br/>
  <img src="https://img.shields.io/badge/MariaDB-003545?style=for-the-badge&logo=mariadb&logoColor=white" alt="MariaDB"/>
  <img src="https://img.shields.io/badge/PostgreSQL-4169E1?style=for-the-badge&logo=postgresql&logoColor=white" alt="PostgreSQL"/>
  <img src="https://img.shields.io/badge/SQLAlchemy-2.0_async-D71F00?style=for-the-badge&logo=sqlalchemy&logoColor=white" alt="SQLAlchemy"/>
  <img src="https://img.shields.io/badge/Alembic-6BA81E?style=for-the-badge" alt="Alembic"/>
  <br/>
  <img src="https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white" alt="Docker"/>
  <img src="https://img.shields.io/badge/Nginx-009639?style=for-the-badge&logo=nginx&logoColor=white" alt="Nginx"/>
  <img src="https://img.shields.io/badge/Linux-FCC624?style=for-the-badge&logo=linux&logoColor=black" alt="Linux"/>
  <img src="https://img.shields.io/badge/Marzban-VLESS_Core-000000?style=for-the-badge&logo=v&logoColor=white" alt="Marzban"/>
  <br/>
  <img src="https://img.shields.io/badge/n8n-FF6584?style=for-the-badge&logo=n8n&logoColor=white" alt="n8n"/>
  <img src="https://img.shields.io/badge/C++-00599C?style=for-the-badge&logo=cplusplus&logoColor=white" alt="C++"/>
  <img src="https://img.shields.io/badge/Redis-DC382D?style=for-the-badge&logo=redis&logoColor=white" alt="Redis"/>
</p>

**Экспертиза:**

- **Асинхронный Python** — aiogram 3, asyncio, пулы соединений, фоновые задачи на APScheduler
- **Проектирование БД** — нормализация под реальную предметную область, идемпотентные миграции, транзакционная целостность на уровне СУБД (`SELECT ... FOR UPDATE`), а не на уровне договорённостей в коде
- **Биллинг и подписки** — платёжные потоки с ручной модерацией, компенсирующие откаты при отказе внешнего API, скидки, промокоды, реферальные программы, акты сверки
- **Сетевая инфраструктура** — Marzban / Xray, VLESS + Reality, схема «входной узел РФ → выходной узел ЕС», мониторинг живости трассы
- **DevOps** — Docker Compose, healthcheck-зависимости между сервисами, автобэкапы с ротацией, деплой и сопровождение на bare-metal

---

### 🚀 Флагманские проекты

<table>
<tr>
<td width="50%" valign="top">

#### 🛡 Tech Poly VPN

**Telegram-биллинг поверх Marzban.**

Полный жизненный цикл платного VPN-доступа: от заявки на оплату до ежемесячного акта сверки с корпоративным клиентом. Marzban управляет трафиком, бот — источник истины по деньгам и срокам.

- Атомарное подтверждение платежа через блокировку строки — двойное начисление невозможно даже при одновременной работе двух админов
- Компенсирующий откат, если панель не ответила после списания
- Динамические цены по группам, промокоды, реферальные скидки
- Корпоративный контур: реселлеры, ключи для сотрудников без привязки к Telegram, append-only журнал начислений
- Резервная выдача конфигов через VK, если Telegram недоступен
- Мониторинг трассы, автобэкапы, акты по расписанию

`Python` `aiogram 3` `MariaDB` `Marzban API` `APScheduler` `Docker`

</td>
<td width="50%" valign="top">

#### 🎫 Help Desk Bunker

**Тикет-система для внутреннего IT-отдела.**

Превращает Telegram в полноценный хелпдеск: структурированные заявки, маршрутизация в чат отдела, двусторонняя переписка, отчётность для руководства.

- Семь статусов с явными переходами; **закрытие подтверждает пользователь, а не исполнитель**
- Карточка заявки редактируется на месте — в чате не растёт лента дублей
- Reply-переписка с маппингом в БД, переживающим рестарт сервиса
- Договорённость о времени визита прямо в карточке
- Оценка работы 1–10 с защитой от промаха
- Автоматика: напоминания о «зависших» заявках, CSV-отчёт 1-го числа, еженедельный дамп БД

`Python` `aiogram 3` `SQLAlchemy 2.0 async` `Alembic` `MariaDB` `Docker`

</td>
</tr>
</table>

---

### ⚙️ Другие направления

| Направление | Проект | Стек |
| :--- | :--- | :--- |
| **Automation** | Узел автоматизации n8n: синхронизация CRM, Telegram и Google Sheets, обработка платёжных вебхуков | `n8n` `Webhooks` `Node.js` |
| **EdTech** | QueueBot — система управления потоками сдачи лабораторных работ, ролевая модель, экспорт в Excel | `Python` `SQLAlchemy` `PostgreSQL` |
| **CAD** | Industrial Box Calc — расчёт геометрии упаковки (FEFCO), оптимизация раскроя | `C++` `CMake` |
| **AI** | Voice-to-Text Unit — транскрибация и саммаризация медиа через LLM | `Python` `FFmpeg` `LLM API` |
| **Web** | Корпоративные сайты и лендинги: семантическая вёрстка, Schema.org, оптимизация под поиск | `HTML` `CSS` `JS` |

---

### 📊 Статус

<p align="center">
  <i>⚠️ Основная разработка ведётся в приватных репозиториях (коммерческие проекты, NDA).<br/>
  Здесь — Open Source компоненты, документация и публичные демо-стенды.</i>
</p>

---

<p align="center">
  <b>Открыт к сотрудничеству</b><br/>
  Разработка Telegram-сервисов · Биллинг и автоматизация · Сетевая инфраструктура<br/><br/>
  <a href="https://t.me/tosha_DevUnit">
    <img src="https://img.shields.io/badge/Написать_в_Telegram-2CA5E0?style=for-the-badge&logo=telegram&logoColor=white" alt="Telegram"/>
  </a>
</p>
