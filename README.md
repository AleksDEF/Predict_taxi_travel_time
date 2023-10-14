# Продолжительность поездки на такси в Нью-Йорке.

## Оглавление 
[1. Описание проекта](https://github.com/AleksDEF/Predict_taxi_travel_time/blob/main/README.md#Описание-проекта)

[2. Какой кейс решаем?](https://github.com/AleksDEF/Predict_taxi_travel_time/blob/main/README.md#Какой-кейс-решаем)

[3. Кратнкая информация о данных](https://github.com/AleksDEF/Predict_taxi_travel_time/blob/main/README.md#Кратнкая-информация-о-данных)

[4. Этапы работы над проектом](https://github.com/AleksDEF/Predict_taxi_travel_time/blob/main/README.md#Этапы-работы-над-проектом)

[5. Результат](https://github.com/AleksDEF/Predict_taxi_travel_time/blob/main/README.md#Результат)

[6. Выводы](https://github.com/AleksDEF/Predict_taxi_travel_time/blob/main/README.md#Выводы)



### Описание проекта 
Определить характеристики и с их помощью спрогнозировать длительность поездки на такси.

:arrow_up: [к оглавлению](https://github.com/AleksDEF/Predict_taxi_travel_time/blob/main/README.md#Оглавление)


### Какой кейс решаем?
Построить модель машинного обучения, которая на основе предложенных характеристик клиента будет предсказывать числовой признак — время поездки такси, то есть решить задачу регрессии.

### Краткая информация о данных

Данные о клиенте и таксопарке:

* id — уникальный идентификатор поездки;
* vendor_id — уникальный идентификатор поставщика услуг (таксопарка), связанного с записью поездки.

Временные характеристики:

* pickup_datetime — дата и время, когда был включён счётчик поездки;
* dropoff_datetime — дата и время, когда счётчик был отключён.
  
Географическая информация:

* pickup_longitude — долгота, на которой был включён счётчик;
* pickup_latitude — широта, на которой был включён счётчик;
* dropoff_longitude — долгота, на которой счётчик был отключён;
* dropoff_latitude — широта, на которой счётчик был отключён.

:arrow_up: [к оглавлению](https://github.com/AleksDEF/Predict_taxi_travel_time/blob/main/README.md#Оглавление)

### Этапы работы над проектом
1. #### Сформировать набор данных на основе нескольких источников информации.
2. #### Спроектировать новые признаки с помощью Feature Engineering и выявить наиболее значимые при построении модели.
3. #### Исследовать данные и выявить закономерности.
4. #### Построить несколько моделей и выбрать из них ту, которая показывает наилучший результат по заданной метрике.
5. #### Спроектировать процесс предсказания длительности поездки для новых данных.


:arrow_up: [к оглавлению](https://github.com/AleksDEF/Predict_taxi_travel_time/blob/main/README.md#Оглавление)

### Результат
[Ноутбук с решением](https://github.com/AleksDEF/Predict_taxi_travel_time/blob/main/Taxi_NY.ipynb)

:arrow_up: [к оглавлению](https://github.com/AleksDEF/Predict_taxi_travel_time/blob/main/README.md#Оглавление)

### Выводы
Лучший показатель RMSLE = 0.39 показал XGBRegressor, так же решающими для алгоритма признаки стали:
* время суток начала поездки
* широта и долгота начала поездки
* широта и долгота окончания поездки
* расстояние по формуле гаверсинуса


:arrow_up: [к оглавлению](https://github.com/AleksDEF/Predict_taxi_travel_time/blob/main/README.md#Оглавление)
