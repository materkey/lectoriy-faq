# Рекомендации по съемке лекций на ФАЛТ МФТИ

## Перед съемкой
1. Полностью зарядить аккумулятор камеры.
2. Зарядить или убедиться в том что батарейка установленная в рекордер для записи с петличного микрофона проработала не больше ~5 часов. Если выработка заряда не известна то зарядить/купить новые пальчиковые(тип АА) батарейки (продаются в пятерочке). Индикатор встроенный в рекордер (ZOOM H1) не всегда показывает адекватную информацию о заряде.
3. Отформатировать/стереть все файлы с карт памяти камеры и рекордера. 1 гигабайта памяти камеры хватает приблизительно на 5 минут записи. 1 гигабайта памяти рекордера хватает примерно на 7 часов. Можно использовать переходник MicroSD->SD или провод USB-MiniUSB (не MicroUsb) для передачи файлов на компьютер. При подключении рекордера на экране начинает мелькать то надпись подключения для того чтобы файлы скинуть то подключения в режиме звуковой карты. В соответствующий момент нужно нажать кнопку записи. В данном случае она работает как кнопка выбора режима.
4. Научиться работать со штативом (попробовать установить камеру на штатив и настроить высоту и ориентацию штатива используя индикаторы уровня)
5. Убедиться что имеется в наличии удлиннитель для зарядки камеры во время лекции (желательно от 5 метров). Без зарядки камеры хватает лишь на 40-60 минут.
6. Смотать провода микрофона так чтобы было удобно положить рекордер в карман. 
7. Убедиться что провод от микрофона привязан изолентой к рекордеру (иначе в кармане преподавателя микрофон отключается). 
8. Узнать нужен ли на лекции кликер. (есть в деканате или у одного из операторов)
9. Узнать нужна ли запись экрана с компьютера преподавателя. (с помошью [OBS Studio](https://obsproject.com/ru))
### Настройка OBS
1. Формат mov, частота кадров - 25, качество - "То же, что у трансляции", битрейт видео - 10000.
2. Запись нужно начинать после подключения проектора. Если в процессе записи кабель проектора отошел или поменялся видео режим в ОС, необходимо проверить что все хорошо и возможно остановить запись, а после подключения проектора снова ее начать.
3. Если отображается черный экран, то необходимо попробовать запустить OBS с помощью другого видеоадаптера (выбор правой кнопкой по ярлыку/исполняемому файлу OBS)
4. Если не помогло, то стоит обновить видео драйвера.

## Съемка лекции
1. На лекцию нужно придти за ~10 минут до начала, чтобы успеть поставить камеру и повесить петличный микрофон на преподавателя до начала лекции.
2. Камера должна быть расположена по центральной линии, а не смотреть на доску сбоку. Если нет мест то попросить уступить его у одногрупников.
3. Начинать запись звука и видео следует за несколько минут до начала самой лекции.
4. Перед тем как дать микрофон преподавателю, следует:
   - проверить подключение провода микрофона
   - установить уровень громкости микрофона на 45 (для следующих лекций этого преподавателя можно будет изменять в завимости от громкости голоса)
   - Auto level: OFF
   - Low Cut: ON
   - Format: MP3
   - начать запись и **убедиться что она началась**
   - установить рекордер в режим HOLD
5. Необходимо помочь преподавателю с проводами от микрофона так чтобы они не болтались, не вываливались из кармана и чтобы **не нарушилось подключение микрофона к рекордеру**. Для надежности подключение микрофона к рекордеру можно укрепить изолентой.
6. В кадре рекомендуется держать 1-2 доски. Общий план следует использовать только если нет возможности вовремя поворачивать камеру так как когда в кадре 4 доски становится трудней различить то что на них изображено. Слишком крупный план тоже не рекомендуется, так как придется часто поворачивать камеру и потом такой материал труднее смотреть.
7. Преподавательские парты перед доской, провода, стулья можно подвинуть так чтобы кадр смотрелся аккуратнее.
8. Также не рекомендуется съемка с первой парты. Почти всегда чем дальше тем лучше. Оптический зум камеры Panasonic SD90 позволяет это делать.
9. При обнаружении бликов на доске можно поменять расположение камеры.
10. Если камера не включается даже во время зарядки, нужно вытащить аккумулятор камеры и вставить его обратно хлопком ладонью. Камера после этого может сразу включится сама.
11. В случае возникновения проблем с камерой следует снимать видео на свой телефон или попросить других студентов. 


## После съемки
1. Как можно раньше нужно скинуть файлы с камеры и рекордера на свой компьютер и уже после этого залить их на Google Drive. (заливать на свой компьютер нужно для повышения шансов на восстановление в случае утери файлов)
2. Удалять файлы со своего компьютера или памяти камеры/рекордера следует только после проверки того что они залиты на Google Drive.


## Монтаж
### Обработка звука
#### Настройка компрессора для звука с петличного микрофона
##### Threshold
- На 6db ниже среднего значения (обычно Threshold около -24db)
##### Output Gain
- Можно начать с +5db, но обычно не выше +16db
##### Ratio
- Отношение превышения входа над порогом к выходному сигналу компрессора.
Для голоса можно начать с 2, но обычно не выше чем 3.
##### Attack
- 2ms
##### Release
- 12ms

#### Настройка лимитера для звука с петличного микрофона
После компрессора следует применить лимитер с Threshold: 0db и Out Ceiling: -1.3db

## Рекомендуемая литература
А. Г. Соколов Монтаж: телевидение, кино, видео  - https://goo.gl/CQPtt7

По всем вопросам: [Ковалев Вячеслав](https://vk.com/materboy)
