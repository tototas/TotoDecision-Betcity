# TotoDecision — программа для расчета прибыльных комбинации тотализатора Betcity

Для почти всех игроков в тотализатор существует одна проблема, какие бы ставки вы не поставили, на дистанции вы будете в минусе. Все потому, что Вы изначально делаете ставки с минусовым математическим ожиданием.

Как известно тотализатор Betcity - это игра с полной информацией, нам еще до начала тиража известны следующие данные:
- нам заранее известны все 14 матчей, значит можно достаточно точно оценить вероятности исходов
- нам известны все поставленные ставки других игроков
- нам известен сумма пула на данный тираж

Зная все эти данные, мы можем найти комбинации с положительным математическим ожиданием.

## Скачать программу
 [Скачать по ссылке](https://github.com/tototas/TotoDecision/archive/master.zip)
 
## Как установить?
1. Разархивируйте архив
2. Вставьте ваш ключ доступа API в файл `apikey.txt`

### Вы можете получить ваш ключ доступа перейдя по ссылке или написав на почту `decision@totobrief.ru`

## Как работает программа?
Программа берет каждую из 4 782 969 (3^14) возможных комбинаций тотализатора Betcity. И высчитывает вероятность этой комбинации попасть в выигрышные категории (с 9-14). Для этого она использует более точные коэффициенты из букмекерской конторы Pinnacle и Betfair. Далее программа определяет какой коэффициент выплаты будет по категориям, если предположить, что все исходы в этой комбинации будут выигрышны, для этого она оценивает все поставленные комбинации других игроков. Наша задача же обыграть остальных=). 
И в итоге определяется мат. ожидание этой комбинации, если оно больше единицы, то комбинация сохраняется в отдельный файл. Прибыльные комбинации из файла сортируются и в начале фала вы видите максимально прибыльные комбинации.

### Это единственная, математически доказанная стратегия, которая позволяет вам регулярно выигрывать и быть в плюсе, играя в тотализаторе. 


## Как использовать программу?
Рекомендуем начинать работу за 15-5 минут до начала тиража.
1. Запустите файл программы `TotoDecision.exe`

2. Введите номер актуального тиража Betcity, нажмите `ENTER`

![screenshot_14](https://user-images.githubusercontent.com/47591655/52857125-056dd080-3148-11e9-82dc-ff834398cf08.png)


3. Введите коэффициент минимальной вероятности (от 0.0 до 0.35), нажмите `ENTER`

![screenshot_1](https://user-images.githubusercontent.com/47591655/52857262-71e8cf80-3148-11e9-8434-9ea6bbb92b7a.png)
Если вы работаете на ПК с современным железом введите 0. Для ноутбуков и слабых ПК введите 0.25-0.27.
Чем меньше значение Вы укажите, тем точнее будет результат. Для значения 0 — будет осуществлен перебор всех 4 782 969 (3^14) возможных комбинаций: 100% точный результат. 

`Внимание! Решение на слабом ПК может занимать длительное время: до 10 минут, если решение занимает много времени введите большее значение коэффициента (например 0.27) `


4. Результаты работы программы доступны в папке `tirazh`. Откройте файл `rmatrix_9mat_kat.csv`
![screenshot_3](https://user-images.githubusercontent.com/47591655/52857264-71e8cf80-3148-11e9-90d6-2e2bbcfa9893.png)

5. Рекомендуется разместить первые 30 комбинаций в тотализаторе Betcity. Для этого воспользуйтесь инструментом `Пакетная загрузка`.

![screenshot_4](https://user-images.githubusercontent.com/47591655/52875340-f1d95e80-3175-11e9-8e62-20601eca0af0.png)



