# It's Mine!

## Задание:

Сделать игру про захват территории (territory acquisition) для 2-4 игроков, про захват территории. Должна присутсовать механика захвата территории в каком то виде.

Победа должна достигаться, либо:

1. Игрок захватывает все территории
2. После N ходов побеждает игрок с большей территорией

Как геймдизанеру, мне предстоит придумать тему, компоненты игры и механики.

А я пока думал, придумал игру про то как НЕ надо захватывать территорию

## Игра:

#### Флейвор

Вы обычный руководитель завода, птица невысокого полёта. От знакомого знакомого вам попадает информация, что через n месяцев примут новый закон и все заводы с черезмерным загрязнением среды будут закрыты, а руководители посажены. Вам конечно не хочется в тюрьму, поэтому вы решаете сосредоточиться на экологии. Но вот незадача, ваши боссы, если завод начнет производит меньше товара чем обычно рассердятся и уволят вас. Что же вам делать?

#### Правила

#### Цель
Игра кончается, когда все клетки будут заняты рекой, лесом, заводом или жетоном игрока. Игрок, с наименьшим количеством выложенных жетонов - побеждает.

#### Подготовка
Клетки поля раскладываются начиная с центральной по кругу, пока не кончатся все клетки и получится большой шестиугольник. Дальше происходит формирование рек и лесов.

Один из игроков берет фишки Исток, Устье и Поворот реки и подкидывает их над разложенным полем, если какая-то из фишек улетела за пределы поля, или пара фишек упали на одну клетку - перебрасываются. Следом, между этими фишками выкладываются фишки Реки. Направление течения реки, определяется по фишке Поворот реки - Исток и Устье переворачиваются таким образом, чтобы ему соответствовать.

Далее, подобным образом подбрасываются и выкладываются фишки леса, те фишки, которые: упали на одну и ту же клетку; выпали за пределы поля; упали на клетку с рекой - перебрасываются.

После игрокам раздаются планшеты, заводы, 3 жетона энерегии и жетоны игрока.

Игроки по часовой стрелке выставляют по 1-му заводу на поле и начинается игра.

#### Ход игры

В начале хода каждый игрок преводит всю свою потраченную мощность в активную, и берет 3 карты за каждый свой завод. Максимально в руке может находится 3 карты плюс 3 карты за каждый завод игрока.

В течении своеого хода игрок может либо разыграть карту с руки, либо пасануть, либо сбросить сколько угодно карт, потратив за каждую 1-у мощность и загрязнив 1-у клетку.

Загрязнять клетки можно либо рядом с заводом, либо рядом с своими жетонами загрязнения. Если такой возможности нет, то можно загрязнить любую клетку.

Реки и леса загрязняются по особым правилам. Реки положив жетон загрязнения на реку, перемещайте его до Устья, либо до другого жетона загрязнения. Вместо того чтобы положить жетон на лес, снимите лес и не загрязняйте клетку.

Ход кончается, когда все игроки пасанут. Если у кого-то осталось непотраченная мощность, тот игрок тратит столько Здровья сколько Мощности осталось.

#### Мелочи

Выставив завод игрок получает +3 карты и +3 мощности в начале хода.

Если у игрока кончилось здоровье, то он выбывает из игры, однако его фишки остаются на поле, но не учавствуют в выборе победителя.

## Заметки с процесса разработки

#### Сеттинг

Поле ~~либо премейд, либо ~~как в катане раскалдывается.

После игроки выставляют свои заводы. У каждого завода есть мощность, например 3.

Игроки **ОБЯЗАНЫ** разыграть карты с руки (у каждой карты есть цена в мощности) и потратить всю мощность своего завода, либо всю руку. (возможно давать больше карт, но игроки тратят мощность либо теряют хп)

Каждая карта делает разные вещи, но обязательно загрязняет окружающую среду. Кто меньше всего загрязнил среду к концу игры - победил.

Возможно стоит добавить "жизни" и дать возможность не тратить всю Мощность завода, а оставшуюся мощность тратить на жизни.

### Кусочки

#### По одному такому комплекту каждому игроку (всего 4 комплекта):

* 4 завода
* 20 знакчов владения
* 1 планшет для ресурсов

#### Общие:

* 24 значка реки
* 1 значок истока реки
* 1 значок устья реки
* 1 значок поворота реки
* 12 значков леса

### Карты

8 карт. Выговор от начальства - Стоимость: 3 мощности, 2 жизни.

8 карт. Вырубка лесов - Стоимость: вся мощность. Эффект: уберите лес и загрязните клетку под ним.

4 карты. Дочернее предприятие - Стоимость: вся мощность. Эффект: поставьте завод на любую незагрязненную пустую клетку.

4 карты. Взаимовыгодное сотрудничество - Стоимость: 2 мощности. Эффект: увеличьте прирост мощности себе и выбранному игроку на 1.

16 карт. Слив химикатов - Стоимость: 3 мощности. Эффект: загрязните 1 клетку реки.

8 карт. Производственные мощности - Стоимость: 3 мощности. Эффект: увеличьте прирост мощности себе на 1.

4 карты. Раскопки - Стоимость: 1 мощность. Эффект: загрязните 1 клетку, сбросьте n карт и возьмите n карт.

24 карт. Сброс отходов - Стоимость: 2 мощности. Эффект: загрязните 1 клетку.

4 карты. Восставший из пепла - Стоимость: вся мощность. Эффект: поставьте завод на своб загрязненную клетку, уберите с неё жетон загрязнения.

8 карт. Дружеский подарок - Стоимость: 1 жизнь. Эффект: помянейте свой жетон на загрязненной клетке, на жетон другого игрока.


8 карт. Боссы будут рады - Стоимость: 2 мощности. Эффект: Восстановите 2 жизни, загрязните 2 клетки, .

4 карты. Эффект: Увеличьте мощность на 1, восстановите 2 жизни.

4 карты. Бойкот зеленых (река) - Стоимость: 1 мощности за каждый чистый тайтл реки рядом с вами.

4 карты. Бойкот зеленых (лес) - Стоимость: 1 мощности за каждый чистый тайтл леса рядом с вами.

4 карты. Стоимость: 3 жизни. Эффект: уменьшите свою мощность на 1.

4 карты. Токсичная бомба - Стоимость: вся мощность. Эффект: загрязните 3 клетки.

#### Правила по добору и использованию

В начале раунда каждый завод игроку приносит 3 карты, в руке игрок может держать максимум 3*(количествоЗаводов+1) карт. Остальные карты он сбрасывает не используя никакого эффекта. В течении хода игрок может либо сыграть карту с руки, либо сбросить любое количество карт и за каждую сброшенную потратить 1 мощность и загрязнить 1 клетку. Вся неиспользованная мощность на конец раунда, снимает у Игрока столько жизней, сколько мощности осталось неиспользованной.


[Статья на медиуме](https://medium.com/@amatuer42/стольник-игра-2-big-green-brother-is-watching-d52d2c53e65c)