# Проект 'Прогностическая модель рисков беременных'
###### Задача: создать прогностическую модель рисков беременных.
###### Метрика: f_beta score со значением beta = 2, "макро" взвешиванием.  
###### Особенности: В последних ячейках необходимо вывести метрики и матрицу ошибок на трейне и тесте.

###### Описание:  
__Age:__ _Age in years when a woman is pregnant._  

__SystolicBP:__  _Upper value of Blood Pressure in mmHg, another significant attribute during pregnancy._  

__DiastolicBP:__  _Lower value of Blood Pressure in mmHg, another significant attribute during pregnancy._  

__BS:__  _Blood glucose levels is in terms of a molar concentration, mmol/L._  

__HeartRate:__  _A normal resting heart rate in beats per minute._  

__Risk Level:__  _Predicted Risk Intensity Level during pregnancy considering the previous attribute._  

###### План исследования:   
1. Знакомство с датасетом  
    - Обзор
    - Корреляционный анализ
    - Попарное сравнение признаков
    - Визуализация признаков
2. Обработка
    - Генерация признаков: в соответствии с медицинскими номами для беременных и прочих
    - Подготовка данных к моделированию
3. Моделирование  
    - Перебор с помощью GridSearchCV моделей разных классов   
        + LogisticRegression, 
        + RandomForestClassifier, 
        + SVC, 
        + AdaBoostingClassifier на основе дерева решений.   
        и выбор лучших гиперпараметров для каждой модели
    - Применение техники стэкинга результатов этих моделей (финализирующий алгоритм - CatBoostClassifier).
    - Предсказание
4. Общий вывод
