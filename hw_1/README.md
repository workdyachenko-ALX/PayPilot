# PayPilot — Quality Bar Proposal (Homework #1)

Репозиторій містить матеріали для домашнього завдання №1 (L01 + L02) по проекту PayPilot.

## Вимоги та конфігурація стенду

Для оцінки якості та відтворення результатів використовуються наступні параметри:

* **Модель агента (`AGENT_MODEL`):** `claude-haiku-5-5` (Anthropic)
* **Модель судді (`JUDGE_MODEL`):** `claude-haiku-5-5` (Anthropic)
* **Профілі оцінки:** 
  * `clean` (Baseline configuration, 2 прогони)
  * `lesson-02` (Defect profile: D04, D05, D16, D19, D20, D25, 3 прогони)
* **Фиксований час (`CLOCK_OVERRIDE`):** `2026-09-15T10:00:00Z`
* **Канонічний звіт:** `reports/l02-clean-lesson-02-20261103-190418.json`

## Відтворення прогону

Для запуску автотестів та генерації звіту виконайте команду:

```bash
CLOCK_OVERRIDE=2026-09-15T10:00:00Z docker compose run --rm eval --runs 3 --baseline-runs 2
```