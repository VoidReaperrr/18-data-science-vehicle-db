# collisions (информация о происшествиях)

## Основная таблица происшествий

| Описание | Обозначение в таблице | Подробнее |
|----------|----------------------|-----------|
| Идентификационный номер в базе данных | `CASE_ID` | Уникальный номер для зарегистрированного происшествия в таблице происшествий |
| Дата происшествия | `COLLISION_DATE` | Формат год/месяц/день |
| Время происшествия | `COLLISION_TIME` | Формат: 24-часовой |
| Является ли место происшествия перекрёстком | `INTERSECTION` | Y — Intersection (перекрёсток)<br>N — Not Intersection (не перекрёсток)<br>-- — Not stated (Не указано) |
| Погода | `WEATHER_1` | A — Clear (Ясно)<br>B — Cloudy (Облачно)<br>C — Raining (Дождь)<br>D — Snowing (Снегопад)<br>E — Fog (Туман)<br>F — Other (Другое)<br>G — Wind (Ветер)<br>- — Not Stated (Не указано) |
| Серьёзность происшествия | `COLLISION_DAMAGE` | 1 — FATAL ТС (Не подлежит восстановлению)<br>2 — SEVERE DAMAGE (Серьёзный ремонт)<br>3 — MIDDLE DAMAGE (Средний ремонт)<br>4 — SMALL DAMAGE (Незначительный ремонт)<br>0 — SCRATCH (Царапина) |
| Основной фактор аварии | `PRIMARY_COLLISION_FACTOR` | A — Code Violation (Нарушение ПДД)<br>B — Other Improper Driving<br>C — Other Than Driver<br>D — Unknown<br>E — Fell Asleep (Заснул)<br>- — Not Stated |
| Состояние дороги | `ROAD_SURFACE` | A — Dry (Сухая)<br>B — Wet (Мокрая)<br>C — Snowy or Icy (Заснеженная)<br>D — Slippery (Скользкая)<br>- — Not Stated |
| Освещение | `LIGHTING` | A — Daylight (Дневной свет)<br>B — Dusk-Dawn (Сумерки-Рассвет)<br>C — Dark-Street Lights (Темно с фонарями)<br>D — Dark-No Street Lights (Темно без фонарей)<br>E — Dark-Street Lights Not Functioning<br>- — Not Stated |
| Номер географических районов | `COUNTY_CITY_LOCATION` | число |
| Названия географических районов | `COUNTY_LOCATION` | категориальный тип данных |
| Направление движения | `DIRECTION` | N — North<br>E — East<br>S — South<br>W — West<br>- or blank — Not State |
| Расстояние от главной дороги (метры) | `DISTANCE` | число |
| Тип дороги | `LOCATION_TYPE` | H — Highway (Шоссе)<br>I — Intersection (Перекрёсток)<br>R — Ramp (or Collector) (Рампа)<br>- or blank — Not State Highway |
| Количество участников | `PARTY_COUNT` | число |
| Категория нарушения | `PCF_VIOLATION_CATEGORY` | 01-24 — различные категории нарушений<br>00 — Unknown<br>- — Not Stated |
| Тип аварии | `TYPE_OF_COLLISION` | A — Head-On (Лоб в лоб)<br>B — Sideswipe (Сторона)<br>C — Rear End (Столкновение задней частью)<br>D — Broadside (Боковой удар)<br>E — Hit Object (Удар объекта)<br>F — Overturned (Опрокинутый)<br>G — Vehicle/Pedestrian<br>H — Other<br>- — Not Stated |
| Дополнительные участники ДТП | `MOTOR_VEHICLE_INVOLVED_WITH` | Other motor vehicle, Fixed object, Pedestrian, Bicycle, Animal, Train и др. |
| Дорожное состояние | `ROAD_CONDITION_1` | A — Holes, Deep Ruts (Ямы)<br>B — Loose Material on Roadway<br>C — Obstruction on Roadway<br>D — Construction or Repair Zone<br>E — Reduced Roadway Width<br>F — Flooded (Затоплено)<br>G — Other<br>H — No Unusual Condition<br>- — Not Stated |

## Таблица Parties (участники происшествия)

| Описание | Обозначение в таблице | Подробнее |
|----------|----------------------|-----------|
| Идентификационный номер в базе данных | `CASE_ID` | Уникальный номер для зарегистрированного происшествия |
| Номер участника происшествия | `PARTY_NUMBER` | От 1 до N — по числу участников |
| Тип участника происшествия | `PARTY_TYPE` | 1 — Car (Авто)<br>2 — Road bumper (Отбойник)<br>3 — Building (Строения)<br>4 — Road signs (Дорожные знаки)<br>5 — Other (Другое)<br>6 — Operator (Оператор)<br>- — Not Stated |
| Виновность участника | `AT_FAULT` | 0/1 |
| Сумма страховки (тыс. $) | `INSURANCE_PREMIUM` | число |
| Состояние участника | `PARTY_DRUG_PHYSICAL` | E — Under Drug Influence<br>F — Impairment — Physical<br>G — Impairment Unknown<br>H — Not Applicable<br>I — Sleepy/Fatigued<br>- — Not Stated |
| Трезвость участника | `PARTY_SOBRIETY` | A — Had Not Been Drinking<br>B — Had Been Drinking, Under Influence<br>C — Had Been Drinking, Not Under Influence<br>D — Had Been Drinking, Impairment Unknown<br>G — Impairment Unknown<br>H — Not Applicable<br>- — Not Stated |
| Наличие телефона в автомобиле | `CELLPHONE_IN_USE` | 0/1 |

## Таблица Vehicles (автомобили)

| Описание | Обозначение в таблице | Подробнее |
|----------|----------------------|-----------|
| Индекс текущей таблицы | `ID` | Номер в таблице |
| Идентификационный номер в базе данных | `CASE_ID` | Уникальный номер для зарегистрированного происшествия |
| Номер участника происшествия | `PARTY_NUMBER` | От 1 до N — по числу участников |
| Тип кузова | `VEHICLE_TYPE` | MINIVAN, COUPE, SEDAN, HATCHBACK, OTHER |
| Тип КПП | `VEHICLE_TRANSMISSION` | auto (Автоматическая)<br>manual (Ручная)<br>- — Not Stated |
| Возраст автомобиля (в годах) | `VEHICLE_AGE` | число |
