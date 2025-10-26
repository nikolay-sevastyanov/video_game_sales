# Анализ продаж видеоигр 1980-2017 г.

## Датасет: [Video Game Sales](https://www.kaggle.com/datasets/gregorut/videogamesales)
### Инструменты: 
1. Python (как основной инструмент);
2. Numpy (для числовых массивов);
3. Pandas (для таблиц);
4. Seaborn (для визуализации);
5. Draw.io (для диаграммы данных). 

<img src="images/df_year_genre_global_dist.png" alt="df_year_genre_global_dist.png" width="320"/> <img src="images/df_vg_regions_year_2.png" alt="df_vg_regions_year_2.png" width="380"/>

## Краткое содержание

1. Рынок видеоигр уменьшается, продажи продолжают падать с 2009 года.
2. Наиболее успешными консолями за 1980-2017г. оказались PS2, XBOX360, PS3, WII, DS, PS за счет своей технологичности на момент выхода, а также аркадной составляющей.
3. Наиболее благоприятное время для выпуска игр на консоль - в первые 3-5 лет после ее выхода.
4. Для конечного потребителя самыми надежными и оптимальными по соотношению цена и качество за 1980-2017 г. оказались PS и Nintendo DS.
5. Рынок видеоигр крайне консолидирован. Издатель Nintendo занимает 20% рынка, а 5 самых успешных издателей - 51%.
6. В Северной Америке, Японии и Европе самый успешный издатель - Nintendo. В остальных регионах - Electronic Arts.
7. В Японии самый популярный жанр видеоигр - "RPG". В других регионах - "экшн"
8. Самые успешные жанры видеоигр в мире на данный момент - "шутер", "экшн", "спорт"
9. Самая успешная пара консоль-жанр - "PS3" - "экшн"
10. Самая продаваемая игра в мире по числу копий - Wii Sports. Феномен Wii и ее спортивных игр следуюет изучить получше, для извлечения коммерческой выгоды.
11. 3 из 10 самых продаваемых игр - франшиза Super Mario, 2 из 10 - франшиза Call of Duty. Франшизы сохраняют свою актуальность.
12. 6 из 10 самых продаваемых игр - игры издателя Nintendo. Nintendo - рынкоопределяющий игрок.
13. 3 из 10 самых продаваемых игр в Европе - франшиза FIFA.
14. 5 из 10 самых продаваемых игр в Европе - игры жанра "спорт". Спортивные игры представляют большой интерес длс европейской аудитории.
15. 5 из 10 самых продаваемых игр в Японии - фрашиза Pokemon.
16. 8 из 10 самых продаваемых игр в Японии - игры издателя Nintendo. Издатель Nintendo в Японии представляет особый интерес, так как является гордостью страны.
17. 2 из 10 самых продаваемых игр в остальных регионах 0 игры франшизы Grand Theft Auto.
18. 1 из 10 самых продаваемых игр в остальных регионах 0 игра жанра "гонки". Не считая Mario Kart, единственная игра жанра "гонки" в топах.
19. Американский рынок приносит более 49% всех продаж, представляю основную ценность для инвесторов, разработчиков и издателей.

## Выводы для бизнеса
1. Рынок платных видеоигр представляет в краткосрочной перспективе наименьший интерес. Инвесторам стоит присмотреться к играм типа Free-to-Play или мобильным играм.
2. Аркадные консоли наиболее успешно продают игры на них.
3. Nintendo, Ubisoft, Electronic Arts, Activision, Sony Computer Entertainment - рынкообразующие компании.
4. Наиболее успешные жанры игр - "шутер", "экшн", "спорт".
5. Самая продаваемая игра в мире по числу копий - Wii Sports. Феномен Wii и ее спортивных игр следуюет изучить получше, для извлечения коммерческой выгоды.
6. Игровые франшизы все еще сохраняют актуальность на рынке.
7. Американский рынок представляет наибольший потенциал возврата инвестиций (ROI) для разработчиков, издателей и инвесторов.
8. На японский рынок имеет крайне высокое влияние издатель Nintendo и жанр "RPG", в отличие от других аудиторий.

## Обзор
Прочитав много новостей про то, как рынок видеоигр является слишком дорогим по сравнению с удовольствием, которое эти игры приносят, я решил найти реальную информацию по продажам видеоигр и ответить на конкретные вопрсосы:

1. Что происходит с рынком видеоигр на данный момент?
2. Какие игровые консоли наиболее прибыльны? Каков общий тренд их актуальности на рынке?
3. В чем основные отличия целевых аудиторий разных стран? Какие жанры игр они предпочитают?
4. Какие игровые консоли наиболее ценны для потребителей с точки зрения цена-качество?
5. Какие издатели имеют наибольшее влияние на развитие рынка видеоигр?
6. Какие жанры имеют наибольшее влияние на развитие рынка видеоигр?
7. Какая целевая аудитория имеют наибольшее влияние на развитие рынка видеоигр?
8. Какие отдельные видеоигры оказали наибольшее влияние на рынок?

## Структура данных

Столбцы таблицы, с которыми была проделана работа:

1. `Rank` типа `int` (целое число) - порядковый номер в сортировки по продажам по убывающей
2. `Name` типа `str` (строка) - название игры
3. `Platform` типа `str` (строка) - название платформы (консоли), на которую вышла игра. В таблице пары игра-консоль учитывают игры, выходящие на несколько консолей.
4. `Year` типа `int` (целое число) - год выхода игры.
5. `Genre` типа `str` (строка) - жанр игры
6. `Publisher` типа `str` (строка) - название издателя
7. `NA_Sales` типа `float(2)` (число с двумя точками после запятой) - объем продаж игры в Северной Америке в миллионах копий.
8. `EU_Sales` типа `float(2)` (число с двумя точками после запятой)  - объем продаж игры в Европе в миллионах копий.
9. `JP_Sales` типа `float(2)` (число с двумя точками после запятой)  - объем продаж игры в Японии в миллионах копий.
10. `Other_Sales` типа `float(2)` (число с двумя точками после запятой)  - объем продаж игры в других регионах (совокупно) в миллионах копий.
11. `Global_Sales` типа `float(2)` (число с двумя точками после запятой)  - объем продаж игры в во всем мире в миллионах копий. Является прилагающимся к датасету столбцом, который является суммой по NA_Sales, EU_Sales, JP_Sales, Other_Sales.

## Диаграмма анализа

<img src="images/vg_data_structure.png" alt="vg_data_structure" height="320"/> 

### Код для подготовки данных:
1. Импортирование библиотек
   
```python
import pandas as pd # импортируем pandas с ключевым словом pd
import matplotlib.pyplot as plt # импортируем matplotlib.pyplot с ключевым словом plt (функции визуализации matplotlib, зависимость для других функций)
import matplotlib.ticker as mticker # импортируем matplotlib.ticker с ключевым словом mticker (функции визуализации matplotlib для осей графиков, зависимость для других функций)
from matplotlib.ticker import FuncFormatter # импортируем FuncFormatter (функции изменения отображаемого формата для данных осей графиков matplotlib, зависимость для других функций)
import numpy as np # импортируем numpy с ключевым словом np (числовые массивы, требующие меньше вычислительных мощностей)
import seaborn as sns # импортируем seaborn с ключевым словом sns (для визуализации)
```

2. Установка опций по умолчанию для pandas

```python
pd.set_option('display.max_columns', None) # при отображении таблицы макимальное кол-во столбцов отключено
pd.set_option('display.max_rows', None) # при отображении таблицы макимальное кол-во строк отключено
pd.set_option('display.width', 3000) # при отображении таблицы кол-во пикселей для отображения по ширине - 3000
```

3. Чтение данных из .csv - файла (таблицы)

```python
df_vg = pd.read_csv('vgsales.csv') # читаем .csv в папке проекта с помощью pandas, декларируем этот датафрейм (таблицу pandas) как "df_vg"
```

4. Проверка чтения таблицы 
```python
print(df_vg.head()) # выводим первые 5 строк таблицы "df_vg"
```
   Вывод должен выглядеть так:
```
   Rank                      Name Platform    Year         Genre Publisher  NA_Sales  EU_Sales  JP_Sales  Other_Sales  Global_Sales
0     1                Wii Sports      Wii  2006.0        Sports  Nintendo     41.49     29.02      3.77         8.46         82.74
1     2         Super Mario Bros.      NES  1985.0      Platform  Nintendo     29.08      3.58      6.81         0.77         40.24
2     3            Mario Kart Wii      Wii  2008.0        Racing  Nintendo     15.85     12.88      3.79         3.31         35.82
3     4         Wii Sports Resort      Wii  2009.0        Sports  Nintendo     15.75     11.01      3.28         2.96         33.00
4     5  Pokemon Red/Pokemon Blue       GB  1996.0  Role-Playing  Nintendo     11.27      8.89     10.22         1.00         31.37
```

5. Создание функций (мое предпочтение, необязательное действие)
```python
def dash():
    print('-' * 170) # Отдельный вывод черты из "-" длиной 170 символов. Использую при выводе нескольких датафреймов отдновременно при их отладке.

def millions_formatter(x, pos):
    return f'{x / 1000000:.0f} M ' # Текст формата отображения миллионов из "100 000 000" в "100 M", часто использую вместе с mticker для упрощения отображения числовых значений по осям.

single_color_green = ['green'] # Список с единственной строкой 'green'. Его принимает на вход функция покраски столбцов в столбчатой диаграмме для выделения только первого столбца зеленым.
```

6. Преобразование данных, обработка пропусков, удаление дубликатов.
   

   1. Обработка пропусков
   ```python
   # Столбцы 'Year' и 'Publisher' имели пустые ячейки. Заполняем их "0"
   
   df_vg['Year'] = df_vg['Year'].fillna(0)
   df_vg['Publisher'] = df_vg['Publisher'].fillna(0)
   ```
   2. Преобразование данных   
   ```python
   # Столбцы "NA_Sales", "EU_Sales", "JP_Sales", "Other_Sales", "Global_Sales" преобразуем из числа с 2 значениями после запятой в целочисленные значения,
   # помножив их на 1 000 000 и изменяя тип данных внутри таблицы на int (целочисленные значения)

   # Столбцу 'Year' изменим тип данных из float(1) в int
   
   df_vg['NA_Sales'] = (df_vg['NA_Sales'] * 1000000).astype(int)
   df_vg['EU_Sales'] = (df_vg['EU_Sales'] * 1000000).astype(int)
   df_vg['JP_Sales'] = (df_vg['JP_Sales'] * 1000000).astype(int)
   df_vg['Other_Sales'] = (df_vg['Other_Sales'] * 1000000).astype(int)
   df_vg['Global_Sales'] = (df_vg['Global_Sales'] * 1000000).astype(int)
   df_vg['Year'] = (df_vg['Year']).astype(int)
   ```

   3. Удаление дубликатов
   ```python
   # определяем на имя "df_vg" таблицу, которая берет данные из раннее существующей "df_vg", но без дубликатов
   
   df_vg = df_vg.drop_duplicates()
   ```
   При выводе таблицы ```df_vg.head()```, должен быть такой результат:
   ```
      Rank                      Name Platform  Year         Genre Publisher  NA_Sales  EU_Sales  JP_Sales  Other_Sales  Global_Sales
   0     1                Wii Sports      Wii  2006        Sports  Nintendo  41490000  29020000   3770000      8460000      82740000
   1     2         Super Mario Bros.      NES  1985      Platform  Nintendo  29080000   3580000   6810000       770000      40240000
   2     3            Mario Kart Wii      Wii  2008        Racing  Nintendo  15850000  12880000   3790000      3310000      35820000
   3     4         Wii Sports Resort      Wii  2009        Sports  Nintendo  15750000  11010000   3280000      2960000      33000000
   4     5  Pokemon Red/Pokemon Blue       GB  1996  Role-Playing  Nintendo  11270000   8890000  10220000      1000000      31370000
   ```
## 1. Что просходит с рынком видеоигр на данный момент?


На данный момент рынок платных видеоигр уменьшается. Основной пик продаж (выше 300 миллионов копий в год) пришелся на 2000-2014г.

<img src="images/df_year_2.png" alt="df_year_2.png" height="320"/> 

Блок кода: 
```python
# 1. Сгруппировать суммы 'NA_Sales','EU_Sales','JP_Sales','Other_Sales','Global_Sales' по значениям столбца 'Year' (продажи по годам)
# 2. Полученные данные задекларировать как датафрейм df_vg_year
# 3. Отсортировать полученную таблицу по 'Global_Sales' по убывающей
df_vg_year = (df_vg.groupby('Year', as_index=False)[['NA_Sales','EU_Sales','JP_Sales','Other_Sales','Global_Sales']].sum().sort_values(by='Global_Sales', ascending=False))

# Удалить нулевые значения "Year", так как здесь они бесполезны
df_vg_year = df_vg_year[df_vg_year['Year'] != 0]

# Создать вычисляемый столбец, который разделит большие значения "Global_Sales" от маленьких по признаку 'Above_Threshold' для больших, 'Below_Threshold' для меньших
df_vg_year['sales_threshold'] = np.where(df_vg_year['Global_Sales'] > 300000000, 'Above_Threshold', 'Below_Threshold')

# Создать палитру (словарь), которая будет указывать библиотеке seaborn условие покраски столбцов в зеленый или красный цвет по признаку
df_vg_year_palette = {'Above_Threshold' : 'green',
                      'Below_Threshold' : 'red'}

# Создать холст визуализации с шириной 900 и длиной 300 пикселей
fig4, ax4 = plt.subplots(figsize=(9,3))

# Задать тип и настройки визуализации:
# Тип - barplot (столбчатая диаграмма), ось x - "Year", ось y - "Global_Sales", покраска зависит от признака "sales_threshold",
# Палитра - df_vg_year_palette (красный и зеленый по признаку), легенда (описание цветов) - отключить
sns.barplot(df_vg_year, x="Year", y="Global_Sales", hue = "sales_threshold", palette = df_vg_year_palette, legend = False)

# Передать форматирование значений оси y как краткое форматирование (100 000 000 -> 100 M)
ax4.yaxis.set_major_formatter(FuncFormatter(millions_formatter))

# Обозначить алгоритм описания оси y. Передаем сюда массив numpy с начальным значением 0, конечным 37, шагом 5 (от первого до 37 столбца с шагом пять, столбцов 37, так как 2017 - 1980 = 37)
ax4.set_xticks(np.arange(0, 37,5))

# Установить параметры визуализации по умолчанию
plt.rcParams.update({'font.size': 10, # размер шрифта общий
                     'axes.titlesize': 15, # размер шрифта названия холста
                     'axes.labelsize': 10, # размер шрифта названий осей
                     'xtick.labelsize': 8, # размер шрифта описания оси x
                     'ytick.labelsize': 8}) # размер шрифта описания оси y.

ax4.set(xlabel = None) # Название оси x - отключить
ax4.set(ylabel = 'Копий продано') # Название оси y - "Копий продано"

# Передаем название холста ("\n" в строке python - перенос строки, fontsize - размер шрифта)
plt.title('Продажи видеоигр 1980-2017 г. \n \n Основной пик продаж игр пришелся на 2000-2014 год, \n далее рынок платных видеоигр пошел на спад. \n', fontsize=11)
```
## 2. Какие игровые консоли наиболее прибыльны? Каков общий тренд их актуальности на рынке?


PS2 - наиболее прибьльная консоль за все время. Аркадные, позволяющие играть в кооперативе, консоли собираюют больше продаж, чем остальные.

<img src="images/vg_platform_3.png" alt="vg_platform_3.png" width="320"/> <img src="images/vg_platform_4.png" alt="vg_platform_4.png" width="325"/>

Блок кода (1): 
```python
# Группируем значения сумм столбцов 'NA_Sales','EU_Sales','JP_Sales','Other_Sales','Global_Sales' по значения столбца 'Platform', затем сортируем по 'Global_Sales', по убывающей, назовем этот датафрейм "df_vg_platform"
df_vg_platform = (df_vg.groupby('Platform', as_index=False)[['NA_Sales','EU_Sales','JP_Sales','Other_Sales','Global_Sales']].sum().sort_values(by='Global_Sales', ascending=False))

# Оставляем строки, где в df_vg_platform значения 'Global_Sales' > 50000000, остальное удаляем. Называем датафрейм - "df_vg_platform_filtered"
df_vg_platform_filtered = df_vg_platform[df_vg_platform['Global_Sales']>50000000]

# Создаем холст с разрешением 500х500 пикселей
fig3, ax3 = plt.subplots(figsize=(5,5))

# Создаем столбчатую диаграмм (barplot), передаем в нее первые 10 строк df_vg_platform_filtered, ось x - "Global_Sales", ось y y="Platform", тип - горизонтальная стобчатая диаграмма (orient='h')
sns.barplot(df_vg_platform_filtered.head(10), x="Global_Sales", y="Platform", orient='h')

# Создаем функцию покраски столбцов: принимаем на вход список из названий цветов, красим столбцы по порядку. Если не передано достаточно названий цветов, красим в серый цвет.
# В этот график передаем только один зеленый цвет.
for i, patch in enumerate(ax3.patches):
    if i < len(single_color_green):
        patch.set_facecolor(single_color_green[i])
    else:
        patch.set_facecolor('gray')

# Форматируем ось x (100 000 000 -> 100 M)
ax3.xaxis.set_major_formatter(FuncFormatter(millions_formatter))

# Настраеваем график по умолчанию
plt.rcParams.update({'font.size': 10,        
                     'axes.titlesize': 8,   
                     'axes.labelsize': 8,   
                     'xtick.labelsize': 8,  
                     'ytick.labelsize': 8})

# Передаем названия осей x и y
ax3.set(xlabel = 'Копий продано')
ax3.set(ylabel = None)

# Передаем название холста
plt.title('Продажи видеоигр по платформам (консолям), 1980-2017 г. \n Самая успешная платформа (консоль) -  PS2. \n', fontsize=11)

# Показываем холст
plt.show()
```

Блок кода (2): 
```python
# Создаем холст с разрешением 500х500 пикселей
fig31, ax31 = plt.subplots(figsize=(5,5))

# Создаем визуализацию. Здесь используем раннее визуализированный датафрейм, просто на этом холсте он будет показан слегка по другому.
sns.barplot(df_vg_platform_filtered.head(10), x="Global_Sales", y="Platform", orient='h')

# Создаем уникальный список с 6 зелеными цветами, так как требуется покрасить первые 6 столбцов
six_colors_green = ['green','green','green','green','green','green']

# Создаем функцию покраски, передаем уникальный список
for i, patch in enumerate(ax31.patches):
    if i < len(six_colors_green):
        patch.set_facecolor(six_colors_green[i])
    else:
        patch.set_facecolor('gray')

# Форматируем ось x (100 000 000 -> 100 M)
ax31.xaxis.set_major_formatter(FuncFormatter(millions_formatter))

# Настраеваем график по умолчанию
plt.rcParams.update({'font.size': 10,          # General font size
                     'axes.titlesize': 8,    # Title font size
                     'axes.labelsize': 8,     # X and Y label font size
                     'xtick.labelsize': 8,    # X-axis tick label font size
                     'ytick.labelsize': 8})   # Y-axis tick label font size

# Передаем названия осей x и y
ax31.set(xlabel = 'Копий продано')
ax31.set(ylabel = None)

# Передаем название холста
plt.title('Продажи видеоигр по платформам (консолям), 1980-2017 г. \n \n Аркадные (социальные) консоли являются самыми успешными. \n', fontsize=11)

# Показываем холст
plt.show()
```

Пик продаж игр на консоль происходит в течение 5 лет после ее выхода на рынок.

<img src="images/df_year_platform_1.png" alt="df_year_platform_1.png" height="300"/>


Наиболее успешная пара "жанр - платформа" - "PS3 - "Экшн" "

<img src="images/df_platform_genre.png" alt="df_platform_genre.png" height="320"/>


## 3. В чем основные отличия целевых аудиторий разных стран? Какие жанры игр они предпочитают?

### Глобальные тренды 


В Японии самый популярный жанр видеоигр - "RPG". В остальном мире - "экшн"

<img src="images/df_vg_max_genre.png" alt="df_vg_max_genre.png" height="370"/>


### Жанры в регионах


В мировых масштабах преобладает и растет доля жанров игр: "экшн", "спорт", "головоломка". Снижается даля жанров "платформер", "стратегия", "головоломка".

<img src="images/df_year_genre_na_dist_1.png" alt="df_year_genre_na_dist_1.png" height="320"/>


### Тренды Северной Америки 


В Северной Америке тренды жанров схожи с глобальными.

<img src="images/df_year_genre_na_dist_1.png" alt="df_year_genre_na_dist_1.png" height="320"/>


### Тренды Европы  


В Европе тренды жанров схожи с глобальными, на слегка увеличен спрос на игры жанра "гонки".

<img src="images/df_year_genre_eu_dist_1.png" alt="df_year_genre_eu_dist_1.png" height="320"/>


### Тренды Японии


В Японии тренды жанров схожи с глобальными, но жанром топ-1 является "RPG".

<img src="images/df_year_genre_jp_dist_1.png" alt="df_year_genre_jp_dist_1.png" height="320"/>


### Тренды остальных регионов


В остальных регионах тренды жанров  схожи с глобальными.

<img src="images/df_year_genre_other_dist_1.png" alt="df_year_genre_other_dist_1.png" height="320"/>


## 4. Какие игровые консоли наиболее ценны для потребителей с точки зрения цена-качество?


Для геймеров наилучшее цена-качество у платформ Nintendo DS и PC.

<img src="images/df_platform_use_1.png" alt="df_platform_use_1.png" height="320"/>


## 5. Какие издатели имеют наибольшее влияние на развитие рынка видеоигр?


Самый успешный издатель всех времен - Nintendo

<img src="images/df_publishers_3.png" alt="df_publishers_3.png" height="305"/>

<img src="images/df_publishers_5.png" alt="df_publishers_5.png" height="320"/>

Рынок платных видеоигр сильно консолидирован.
5 самых успешных издателей имеют долю рынка 51%

<img src="images/df_publishers_4.png" alt="df_publishers_4.png" height="320"/>

<img src="images/df_publishers_6.png" alt="df_publishers_6.png" height="320"/>


В Северной Америке, Японии и Европе самый успешный издатель за 1980-2017 г. - Nintendo. В остальных регионах - Electronic Arts.

<img src="images/df_max_market_cap_1.png" alt="images/df_max_market_cap_1.png" height="320"/>


## 6. Какие жанры имеют наибольшее влияние на развитие рынка видеоигр?


Самый успешный жанр в мире - "экшн"

<img src="images/vg_genre_2.png" alt="vg_genre_2.png" height="320"/>


## 7. Какая целевая аудитория имеют наибольшее влияние на развитие рынка видеоигр?


За 1980-2017 г. наибольший объем продаж копий видеоигр произошел в Северной Америке.

<img src="images/df_vg_regions.png" alt="df_vg_regions.png" height="320"/>


## 8. Какие отдельные видеоигры оказали наибольшее влияние на рынок?

### Общие продажи


Самая продаваемая игра по числу копий - Wii Sports. Феномен Wii Sports нужно изучить глубже, чтобы исплользовать знания для продвижения и разработки игр в будущем. 

<img src="images/df_vg_game_global_0.png" alt="df_vg_game_global_0.png" height="320"/>



3 из 10 самых продаваемых игр по числу копий - эксклюзивы для Wii.

<img src="images/df_vg_game_global_1.png" alt="df_vg_game_global_1.png" height="320"/>


3 из 10 самых продаваемых игр по числу копий - игры по франшизе Super Mario.

<img src="images/df_vg_game_global_2.png" alt="df_vg_game_global_2.png" height="320"/>


2 из 10 самых продаваемых игр по числу копий - игры по франшизе Call of Duty.

<img src="images/df_vg_game_global_3.png" alt="df_vg_game_global_3.png" height="320"/>


6 из 10 самых продаваемых игр по числу копий - игры издателя Nintendo.

<img src="images/df_vg_game_global_4.png" alt="df_vg_game_global_4.png" height="320"/>


### Продажи в Северной Америке


Рынок Северной Америки почти не отличается от глабального.

<img src="images/df_vg_game_na_1.png" alt="df_vg_game_na_1.png" height="320"/>


### Продажи в Европе


3 из них - игры франшизы FIFA.

<img src="images/df_vg_game_eu_1.png" alt="df_vg_game_eu_1.png" height="320"/>


5 из них - игры жанра "спорт".

<img src="images/df_vg_game_eu_2.png" alt="df_vg_game_eu_2.png" height="320"/>


### Продажи в Японии


5 из них - игры франшизы Pokemon.

<img src="images/df_vg_game_jp_1.png" alt="df_vg_game_jp_1.png" height="320"/>


8 из них - игры издателя Nintendo.

<img src="images/df_vg_game_jp_2.png" alt="df_vg_game_jp_2.png" height="320"/>


## Продажи в остальных регионах


2 из них - игры серии Grand Theft Auto.

<img src="images/df_vg_game_other_1.png" alt="df_vg_game_other_1.png" height="320"/>


1 из них - Grand Turismo, игра жанра "гонки".

<img src="images/df_vg_game_other_2.png" alt="df_vg_game_other_2.png" height="320"/>

## Заключение

В этом анализе я попытался привнести ясности в события индустрии платных видеоигр. Он способен стать отправной точкой как и для исторического анализа, так и быть самостоятельным ресурсом с целью "держать руку на пульсе". 

Благодарю вас за внимание. :)
