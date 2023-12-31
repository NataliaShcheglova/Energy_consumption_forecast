# Энергетический оракул - Прогноз общего потребления электроэнергии за сутки
GlowByte Atumn Hack 2023. Прогнозирование суточного потребления электроэнергии Калининградской области.  

**Задача**

Разработка модели прогнозирования общегоэнергопотребления региона на сутки, в МВтч

**Цель**

Разработать надежную и точную модель прогнозирования объема энергопотребления на сутки для Калининградской области с использованием доступных исторических данных и соответствующих переменных.

**Описание задачи**

В данной задаче необходимо разработать предиктивную модель, которая позволит прогнозировать энергопотребление региона на основе имеющихся данных о потреблении электроэнергии в прошлом и соответствующих факторах, влияющих на потребление энергии. Модель должна быть способна учесть сезонные, временные и другие зависимости для более точного прогноза.
Модель должна предсказывать общее потребление региона на 1 сутки.

**Результат** 
- Обучены две бустинговые модели CatBoostRegressor и XGBRegressor, с прдбором гиперапараметров и кросс валидацией с применением GridSearchCV. 
- Обучена и протестирована на открытом тестовом датасете лучшая модель CatBoostRegressor с наилучшими параметрами {'depth': 6, 'iterations': 200, 'learning_rate': 0.1}. 
- Лучшая модель на тесте имеет следующие значения метрик: 
  - Значение MAE (Mean Absolute Error) равно 264 МВтч, то есть среднем модель делает ошибку в прогнозе потребления электроэнергии размером около 264 МВтч.

  - Значение MPAE равно 0.026, что означает в среднем модель ошибается на 2.6% относительно фактического потребления электроэнергии.

  - Значение R2 равно 0.803. Это означает, что ваша модель объясняет примерно 80.3% вариабельности в потреблении электроэнергии, измеренной в МВт*ч.
