# Прогнозирование заказов такси
Ноутбук проекта находится в файле [taxi_order_forecast.ipynb](https://github.com/ArtemV0ronin/taxi_order_forecast/blob/main/taxi_order_forecast.ipynb)  
Альтернативная [ссылка](https://colab.research.google.com/drive/1eS_EUisURtoWBPDb3xtdazwjBAV6n59g#offline=true&sandboxMode=true) на Google Collab.


## Задача проекта
Интернет-магазин «Стримчик», занимающийся продажей видеоигр игр по всему миру, предоставил исторические данные о продажах. Для планирования рекламных кампаний магазина на следующий год необходимо провести исследовательский анализ данных и выявить определяющие успешность игры закономерности, чтобы сделать ставку на потенциально популярный продукт.


## Используемый стек
![Static Badge](https://img.shields.io/badge/statsmodels-red)
![Static Badge](https://img.shields.io/badge/TimeSeriesSplit-red)
![Static Badge](https://img.shields.io/badge/adfuller-red)
![Static Badge](https://img.shields.io/badge/sklearn-red)
![Static Badge](https://img.shields.io/badge/os-red)
![Static Badge](https://img.shields.io/badge/time-red)
![Static Badge](https://img.shields.io/badge/CatBoostRegressor-red)
![Static Badge](https://img.shields.io/badge/LGBMRegressor-red)
![Static Badge](https://img.shields.io/badge/RandomForestRegressor-red)
![Static Badge](https://img.shields.io/badge/LinearRegression-red)
![Static Badge](https://img.shields.io/badge/GridSearchCV-red)
![Static Badge](https://img.shields.io/badge/pandas-red)
![Static Badge](https://img.shields.io/badge/numpy-red)
![Static Badge](https://img.shields.io/badge/matplotlib-red)
![Static Badge](https://img.shields.io/badge/seaborn-red)

---

## Итоги проекта

В ходе проведенной работы была разработана модель на базе модели RandomForest, прогнозирующая количество заказов такси на следующий час.

Метрика RMSE модели RandomForestRegression на тестовой выборке = **41.49**.

Гиперпараметры модели:

<table> 
<tr>
  <th>Параметр</th>
  <th>значение</th>
</tr>
<tr>
  <th>n_estimators</th>
  <td>69</td>
</tr> 
<tr>
  <th>max_depth</th>
  <td>18</td>
</tr>
<tr>
  <th>min_samples_leaf</th>
  <td>1</td>
</tr>    
<tr>
  <th>min_samples_split</th>
  <td>2</td>
</tr>
</table>

В ходе анализа данных было выявлено:

- со временем все больше и больше людей пользуется услугой заказа такси
- увеличение роста на спрос такси наблюдается с приходом летнего периода
- к концу недели и в середине идет увеличение заказов
- чаще всего такси заказывают 12 часов ночи
- реже всего такси заказывают в 6 утра
- в начале каждого дня идет пик на заказы, потом резкое падение, затем в течение дня количество заказов снова растет и к концу дня достигает нового пика

Всего в ходе работы было обучено 4 модели, подобраны для них гиперпараметры, проведен анализ метрик моделей:

<table>
<tr>
  <th>Модель</th>
  <th>RMSE</th>
  <th>Время обучения</th>
  <th>Время предсказания</th>
</tr>
<tr>
  <td>RandomForestRegressor</td>
  <td>25.179</td>
  <td>3.887</td>
  <td>0.016</td>
</tr>    
<tr>
  <td>CatBoostRegressor</td>
  <td>26.280</td>
  <td>0.628</td>
  <td>0.011</td>
</tr>   
<tr>
  <td>LinearRegression</td>
  <td>26.950</td>
  <td>0.018</td>
  <td>0.012</td>
</tr> 
<tr>
  <td>LGBMRegressor</td>
  <td>26.381</td>
  <td>0.031</td>
  <td>0.012</td>
</tr>
</table>



