# Fraud Detection with Random Forest

Модель для выявления мошеннических транзакций в кредитных картах с помощью **Random Forest Classifier**.  
Цель проекта — показать, как методы машинного обучения помогают банкам минимизировать финансовые потери.


## Датасет
[Credit Card Fraud Detection dataset](https://www.kaggle.com/mlg-ulb/creditcardfraud)  
- **284 807** транзакций  
- **30 признаков**  
- Доля мошеннических операций: всего **0.17%**  

## Модель
- Алгоритм: **Random Forest Classifier**  
- Балансировка классов: `class_weight='balanced'`  
- Сравнение результатов на:
  - полном датасете (оригинальное распределение классов)  
  - сбалансированном датасете (1:1 fraud / normal, по 492 записи каждого класса)  


## Результаты
### Полный датасет:
- Accuracy: **99.96%**  
- Обнаружено: **471 из 492 мошеннических транзакций** (95.73%)  
- Пропущено: **5.08%**  
- Ложные срабатывания: **0.002%**  
- Потенциальная экономия: **до 1 млрд ₽ в год** (при курсе 84.4 ₽/$)  

### Сбалансированный датасет:
- Accuracy: **97.46%**  

<p align="center">
  <img src="image/large.png" alt="Confusion Matrix (Full Dataset)" width="400"/>
  <img src="image/small.png" alt="Confusion Matrix (Balanced Dataset)" width="400"/>
</p>


## Производительность
Среднее время отклика: **~3.9 мс на транзакцию**  

## Технологии
- Python 3.10  
- pandas, numpy  
- scikit-learn  
- seaborn, matplotlib  
