# Автоматизация: New Car Pipeline

При добавлении нового автомобиля выполнять **строго по порядку**:

1. Создать запись в VehicleDataTable (масса, мощность, КПП, привод, момент и т.д.).
2. Запустить навык **vehicle-physics-tuner** с характеристиками автомобиля.
3. Выполнить скрипт инициализации (из корня проекта):
   ```bash
   bash skills/realistic-car-sim/scripts/new-car-init.sh <ИмяАвто>
   ```
   (создаёт `Cars/<ИмяАвто>/` + Physics/Doors/Dashboard checklists + README)
4. Добавить заготовку Dashboard через навык **dashboard-generator**.
5. Реализовать двери через навык **vehicle-door-system** (когда дойдём до Фазы 2).
6. Обновить Реестр ошибок при необходимости.

## Связанные навыки (skills)

Все skills находятся внутри проекта:

| Навык | Путь | Назначение |
|-------|------|------------|
| `realistic-car-sim` | `skills/realistic-car-sim/` | Общий workflow, KT, реестр, архитектура |
| `vehicle-physics-tuner` | `skills/vehicle-physics-tuner/` | Настройка Chaos Vehicle, Physical Materials, чек-листы физики |
| `dashboard-generator` | `skills/dashboard-generator/` | Панель приборов, data binding, day/night |
| `vehicle-door-system` | `skills/vehicle-door-system/` | Интерактивные двери, капот, багажник, speed lockout |

На пользовательской машине корень проекта соответствует:
`D:\Projects\Grok\Realistic Car Simulation\`
