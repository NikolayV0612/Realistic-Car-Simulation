# Skills, Automations & Connectors

**Дата настройки:** 2026-07-31  
**Последнее обновление:** 2026-08-01  
**Корень проекта (пользователь):** `D:\Projects\Grok\Realistic Car Simulation\`  
**Корень проекта (sandbox):** `/home/workdir/artifacts/Realistic Car Simulation/`

## Активные навыки проекта (внутри репозитория)

| Skill | Путь | Назначение | Статус |
|-------|------|------------|--------|
| realistic-car-sim | `skills/realistic-car-sim/` | Workflow, KT, Error Registry, New Car Pipeline, архитектура | Готов |
| vehicle-physics-tuner | `skills/vehicle-physics-tuner/` | Chaos Vehicle tuning, Physical Materials, physics checklists | Готов |
| dashboard-generator | `skills/dashboard-generator/` | Панель приборов, gauges, data binding, day/night | Готов |
| vehicle-door-system | `skills/vehicle-door-system/` | Интерактивные двери/капот/багажник, state machine, speed lock | Готов |

### Bundled skills (системные, уже доступны агенту)

- `xlsx` — VehicleDataTable, балансировка
- `docx` / `pdf` / `pptx` — документация и презентации
- `skill-creator` — создание новых навыков
- `tasks` — scheduled tasks / напоминания
- `mcp` / GitHub connected tools — внешние коннекторы

## Автоматизации

### 1. New Car Scaffold
Из корня проекта:
```bash
bash skills/realistic-car-sim/scripts/new-car-init.sh <CarName>
```
Создаёт:
- `Cars/<CarName>/`
- Physics_Checklist.md
- Doors_Checklist.md
- Dashboard_Checklist.md
- README.md

### 2. Правила автоматического создания новых skills
По мере появления повторяющихся нетривиальных процедур создавать новый skill через `skill-creator` и размещать его в `skills/<name>/`, затем регистрировать в этом файле.

### 3. Git / GitHub
- Локальная ветка: `main`
- Remote: https://github.com/NikolayV0612/Realistic-Car-Simulation
- GitHub connector: **подключён** (аккаунт NikolayV0612)

## Коннекторы (MCP) — GitHub

| Компонент | Статус | Комментарий |
|-----------|--------|-------------|
| GitHub connector | **Подключён** | Аккаунт NikolayV0612 |
| Репозиторий | https://github.com/NikolayV0612/Realistic-Car-Simulation | public |
| Локальный git | Готов | ветка main |

## Планируемые skills

| Приоритет | Название | Фаза | Назначение |
|-----------|----------|------|------------|
| Высокий | location-service | 4 | Гараж, АЗС, мойка, магазины |
| Высокий | camera-manager | 3 | 4+ вида камер |
| Средний | road-network | 1/4 | Spline roads + Physical Materials |
| Средний | fuel-economy | 1/4 | Расход топлива |
| Низкий | weather-timeofday | 4 | День/ночь, дождь |
| Низкий | vehicle-audio | 1+ | MetaSounds / Wwise |

## Правило

Перед началом любой новой крупной задачи:
1. Прочитать `02_Реестр_ошибок.md`
2. Проверить, есть ли уже подходящий skill в `skills/`
3. Если процедуры повторяются — сразу создать skill внутри `skills/`
