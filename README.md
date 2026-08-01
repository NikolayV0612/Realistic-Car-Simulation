# Realistic Car Simulation

Максимально реалистичная автомобильная симуляция на Unreal Engine 5.

**Локальный путь на машине пользователя:**  
`D:\Projects\Grok\Realistic Car Simulation\`

**Путь в sandbox агента:**  
`/home/workdir/artifacts/Realistic Car Simulation/`

## Структура проекта

```
Realistic Car Simulation/
├── 01_Vision_and_Scope.md          # Цель, MVP, контрольные точки (KT)
├── 02_Реестр_ошибок.md             # Обязательный реестр ошибок
├── 03_Необходимое_ПО.md            # Стек (UE5, Blender, Substance…)
├── 04_High-Level_Architecture.md   # Менеджеры, Vehicle Actor, интерфейсы
├── 05_Imagine_Prompts.md           # Промпты для референсов
├── 06_NewCarPipeline.md            # Процесс добавления нового авто
├── 07_Skills_and_Automations.md    # Skills, скрипты, коннекторы
├── README.md                       # Этот файл
├── .gitignore
├── skills/                         # Все проектные навыки (skills)
│   ├── realistic-car-sim/
│   ├── vehicle-physics-tuner/
│   ├── dashboard-generator/
│   └── vehicle-door-system/
└── Cars/                           # (создаётся при добавлении авто)
    └── <CarName>/
        ├── Physics_Checklist.md
        ├── Doors_Checklist.md
        ├── Dashboard_Checklist.md
        └── README.md
```

## Быстрый старт

1. Прочитать `01_Vision_and_Scope.md` и `04_High-Level_Architecture.md`.
2. Перед любой задачей — `02_Реестр_ошибок.md`.
3. Добавление нового автомобиля — следовать `06_NewCarPipeline.md`.

## Контрольные точки

| KT | Критерий |
|----|----------|
| KT-0 | Vision + архитектура согласованы |
| KT-1 | Базовый автомобиль едет, чувствует покрытия |
| KT-2 | Двери полностью интерактивны |
| KT-3 | Панель приборов + 4+ камеры |
| KT-4 | Локации (гараж, АЗС, мойка) работают |
| KT-5 | MVP Ready |

## Git

Репозиторий инициализирован на ветке `main`.  
После подключения GitHub-коннектора:

```bash
git remote add origin <url>
git push -u origin main
```
