# Weekly Productivity Audit — Source of Truth

> Этот файл — основной markdown-документ аудита. HTML-страница генерируется из этих данных.
> Обновляется еженедельно скиллом `/weekly-audit`.

---

## Метаданные

- **Период:** Неделя 9 (2-8 апреля 2026)
- **Дата генерации:** 2026-04-10
- **Аудит начат:** 2026-02-05 (установка Claude Code)

---

## Revenue

### Источники дохода

| Источник | Тип | MRR | Статус |
|----------|-----|-----|--------|
| СБОРКА | Подписки студентов | ~$500 | Active |
| Консультации | Почасовые ($200+/час) | ~$1,000 | Active |
| Marshall | Консалтинг спринты | ~$500 | Active |
| MentalStab | Tribute сессии | ~$100 | Early |
| Antaria | Рамочный + допник почасовая | Pipeline | Negotiated |
| Проект Егора | Broker content | Pipeline | Active |
| LH (Роман) | Trend intelligence | Pipeline | Handoff sent |

### Целевой MRR: $10,000

### Текущий MRR: ~$2,100 (последнее известное значение из Недели 6)

> ⚠️ **Нет свежих revenue-данных** за недели 7-9. Требуется запустить revenue-pulse audit для актуализации (Tribute webhooks, банк, PayPal).

### Прогресс к цели: 21%

---

## Активность по неделям

| Неделя | Дата | Коммиты | Активные репо | Revenue |
|--------|------|---------|---------------|---------|
| 1 | 5-11 фев | 15 | 4 | $0 |
| 2 | 12-18 фев | 12 | 5 | $200 |
| 3 | 19-25 фев | 8 | 5 | $400 |
| 4 | 26 фев-4 мар | 25 | 7 | $800 |
| 5 | 5-11 мар | 60 | 9 | $1,200 |
| 6 | 12-18 мар | 35 | 7 | $2,100 |
| 7 | 19-25 мар | 301 | 32 | нет данных |
| 8 | 26 мар-1 апр | 204 | 23 | нет данных |
| 9 | 2-8 апр | 259 | 16 | нет данных |

**Инсайт:** взрывной рост активности с недели 7 (x8 по коммитам, x4 по активным репо). Причина — переход на parallel sessions + slave-mode workflow (Opus master / MiniMax slave).

---

## Активные проекты (Неделя 9)

Проекты с коммитами за 2-8 апреля 2026 (16 репо):

| Проект | Коммиты (нед 9) | Статус |
|--------|----------------|--------|
| afterhumans | топ-1 | 🟢 Active — Unity narrative walker |
| memory | топ-2 | 🟢 Ежедневные обновления |
| career-ops | высокий | 🟢 AI job search pipeline |
| timmyzinin.github.io | высокий | 🟢 Лендинги, GitHub Pages |
| space-shooter-unity | средний | 🟢 Unity игра |
| friends | средний | 🟢 Friends Protocol (SDD, wiki) |
| egor-project | средний | 🟢 Broker content |
| claude-partner | средний | 🟢 Утилиты |
| antaria-project | средний | 🟢 Кипр недвижимость |
| hh-outreach | низкий | 🟢 Lead gen |
| yacht-sim | низкий | 🔵 Экспериментальный |
| kariyer-outreach | низкий | 🟢 Турция lead gen |
| game-research | низкий | 🔵 Ресёрч |
| LH | низкий | 🟢 Trend intel (Роман) |
| sborka-lecture | низкий | 🟢 СБОРКА лекции |
| botanica-backlog | низкий | 🟢 Ботаника |

---

## Инфраструктура

- **Contabo VPS 30:** 31 Docker-контейнер, uptime 28 дней, load avg 0.35-0.57
- **SSH:** publickey only, fail2ban активен
- **Домены:** timzinin.com (GitHub Pages), sborka.work, n8n.timzinin.com, langfuse.timzinin.com
- **MCP серверов:** ~16 активных

---

## Инструменты в production

### Текущий стек
- Claude Code CLI (Opus 4.6) — ежедневно, parallel sessions
- MiniMax M2.5 slave sessions (`/mm`, `/mm-review`)
- Codex CLI для independent review (`/codex-review`, `/codex-adversarial`, `/combo-review`)
- n8n self-hosted (n8n.timzinin.com)
- Langfuse (langfuse.timzinin.com) — мониторинг AI агентов
- LangGraph scaffold
- CrewAI + Paperclip
- 80+ скиллов, 41 агент в пуле, 12 хуков
- Contabo VPS 30 (31 Docker контейнеров)
- Hammerspoon + HyperKey

---

## Инсайты недели

1. **Parallel sessions** стали нормой — активных репо x2 по сравнению с неделями 1-6
2. **Slave-workflow (MiniMax)** разгружает Opus, стоимость падает, throughput растёт
3. **Lead-generation пайплайны** (HH, Kariyer, LH, Antaria) запущены параллельно — диверсификация
4. **Нет свежих revenue-данных** — это главный gap. Метрика коммитов растёт, но без revenue-pulse непонятна конверсия в деньги
5. **Game dev эксперименты** (afterhumans Unity, yacht-sim, space-shooter, web-games) — возможная новая вертикаль или distraction?

---

## Action Items (эта неделя)

- [ ] **КРИТИЧНО:** запустить revenue-pulse audit — актуализировать MRR за недели 7-9 (Tribute, банк, PayPal)
- [ ] **Фокус-проверка:** 16 активных репо за неделю = распыление? Оценить через `/focus-coach`
- [ ] **Навести порядок со скиллами** — сейчас 80+ скиллов, многие не используются (начато в текущей сессии)
- [ ] Следить за ответом Романа (LH) в TG → MVP Signal Layer
- [ ] Антария: следующие шаги после встречи с Мариной
- [ ] Проект Егора: завершить черновик, отправить клиенту
