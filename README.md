# MaxManko.github.io
My site
2
Урок 8. Масиви
У різних розділах математики та інших наук дані, що мають вигляд інформації, заданої як послідовність рядків і стовпчиків, називають порізному: матриці - у вищій алгебрі, таблиці - у розрахункових задачах, масиви - у програмуванні.

У задачах, які передбачають введення великої кількості довільних початкових даних, для задання інформації зручно використовувати генератор випадкових чисел.У задачах, які передбачають роботу з таблицями значень, результати для кращої читабельності зручно виводити у вигляді справжньої таблиці, розташовуючи рядок під рядком, а числа у стовпчиках одне під одним.

Масив - це великий простір чогось однорідного за типом. (Зі словника іноземних слів, 1954 р.)
Масив у програмуванні - це тип структури даних, що має складені значення. (З Оксфордського словника англійської мови, 1995 р.)
Масив - це впорядкований скінченний набір елементів (даних) одного типу. Зазвичай працюють з масивами, які містять числа.

Масивом називається скінченна послідовність змінних одного типу, які мають однакове ім'я та різняться порядковим номером.

Індексом називається порядковий номер елемента масиву.

Отже, введено новий тип — масив. Усі типи, які досі були вам відомі, називаються простими. Масив є прикладом структурованого типу, тобто він, у свою чергу, складається з елементів іншого типу.

Як звернутися до елементів цього масиву? Для цього необхідно вказати індекс.

Наприклад,

T[2], T[5], T[i], T[i + j].

Але в третьому і четвертому прикладах для визначення необхідного елемента масиву треба знати значення величин і та j. Така загальність визначення індексу масиву є дуже потужним засобом програмування, але разом з цим і провокує можливі помилки: отриманий результат обчислення індексу масиву може виходити за межі інтервалу, виділеного для індексів даного масиву.

I ще один важливий момент, яким у жодному разі не можна нехтувати. Масиви відносяться до структур з так званим прямим або довільним доступом: щоб визначити окремий елемент масиву, достатньо вказати його індекс.

Тепер зрозуміло, як у циклі перебирати різні значення елементів масиву: для цього достатньо змінювати їх індекси. А закон зміни індексів дуже простий - кожне наступне значення більше попереднього на одиницю. Дуже зручна закономірність!



Оскільки у мові Pascal усе з чим ми працюємо потрібно оголошувати, то масиви також потрібно оголосити. Це можна зробити кількома способами:

у полі const

const <ім'я змінної>=array[1 .. <клькість елементів>] of <тип> = (1,2,3, ... <значення>);

у полі type

type <ім'я типу>=array[1 .. <кількість елементів>] of <тип>;
var <ім'я змінної> : <ім'я типу>; 

у полі var

var <ім'я змінної> : array[1 .. <кількість елементів>] of <тип>;

Приклад:

type Mas = array[1 .. 5] of integer;
var a : Mas;
