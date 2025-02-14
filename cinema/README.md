**Условнй заказчик этого исследования — Министерство культуры Российской Федерации.**

**Задача**: изучить рынок российского кинопроката и выявить текущие тренды. Уделить внимание фильмам, которые получили государственную поддержку и ответить на вопрос, насколько такие фильмы интересны зрителю. 

**Навыки и инструменты**: Pandas, Python, визуализация данных, исследовательский анализ данных, предобработка данных

**Содержание исследования**
1. [Первичное ознакомление с данными](#start)
2. [Предобработка данных](#preprocessing)
    * [Проверка типов данных](#type) 
    * [Обработка пропущенных значений](#null)
    * [Обработка дубликатов](#duplicates)
    * [Обработка категориальных значений](#category)
    * [Проверка количественных значений](#number)
    * [Создание новых столбцов](#column) 
3. [Анализ данных](#analyses)
    * [Распределение данных по годам](#years)
    * [Динамика проката данных по годам](#rental)
    * [Возрастное ограничение аудитории и сборы в прокате](#age)
 
 4. [Исследование фильмов, которые получили государственную поддержку](#goverment)
     
 5. [Общий вывод](#conclusion)

Выводы: 
**1. Проанализров дубликаты по названию мы увидели, что есть много столбцов, в которых различаются***
1) Прокатные удостоверения

2) Дата премьеры фильма

3) Сборы в рублях

Один фильм может иметь несколько прокатных удостоверений, если прокатное удостоверение выдавалось в разные сроки и для разных прокатных целей. Фильм мог поменять правообладателя, название или даже быть немного изменён для каких-либо творческих или коммерческих целей. Поэтому в Минестерстве культуры стоит ввести единый идентификационный номер, которые может объединять такие фильмы, чтобы данные не дублировались при анализе.

**2. В категориальных значениях множество перечислений, поэтому достаточно сложно делать анализ про группам. Так как много вариаций, перечислений. Выделение категория главный или основной — это хороший способ проанализировать значения.

**3. Необходимо лучше проверять достоверность данных при анализе. Есть фильмы с нулевыми бюджетами, фильмы с одинаковыми прокатными удостоверениями и так далее. Источников данных много, но всё же их стоит проверять тщательнее.

**4. Данные до 2014 недостаточны для анализа** Плюс в этих периодах содержаться данные с очень странными кассовыми сборами (очень низкие). Поэтому в дальнейшей анализе используются только данные после 2015 года

**5.Анализ данных по категориям**
Самые низкие сборы и категории «0+».
Этого не видно на графике, но видно из таблицы (эти сборы резко снизилист после 2017)
В 2017 была просадка категории 12+ но потом она вновь пошла вверх.
В 2017 был пик для категории 16+ после этого у неё был спад.
Категории 6+ и 18 + практически повторяют траекторию роста друг друга.

**6. Средние и медианные значения сборов**
При анализе медианы и среднего значения видно, что были падения в 2016 и после пика в 2017. Хотя общая сумма продолжала сборов расти. В Медианных значениях скачки более заметны.

**7. Государственная поддержка**
Государственная поддержка работает только тогда, когда фильм полностью спонсируется государством, в обратных случаях фильмы чаще проваливаются в прокате, чем делают сборы.

По жанрам наилучшие сборы у исторических фильмов, спортивных и фантастики.
