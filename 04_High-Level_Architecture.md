# High-Level Architecture

```
GameInstance / GameMode
├── VehicleManager          (выбор, спавн, сохранение состояния автомобилей)
├── WorldManager            (время суток, погода, дорожные условия)
├── LocationManager         (гараж, АЗС, мойка, магазины)
├── EconomyManager          (топливо, деньги, состояние авто)
└── CameraManager           (переключение видов)

Vehicle Actor
├── Chassis / Skeletal Mesh
├── Physics Vehicle Component (колёса, подвеска, двигатель, трансмиссия)
├── Door System (Door Component × N)
├── Dashboard Component
├── Fuel System
├── Audio Component
└── Interaction Component

Camera System
├── Interior
├── Exterior Follow / Chase
├── Free Look
├── Hood / Bumper
└── Cinematic

Environment
├── Road Network (Spline + Physical Materials)
├── Locations (Garage, GasStation, CarWash, Shop)
└── Weather / TimeOfDay
```

## Ключевые интерфейсы
- `IInteractable` — двери, заправка, мойка, ворота гаража
- `IVehicleDataProvider` — данные для панели приборов
- `ILocationService` — услуги локаций
