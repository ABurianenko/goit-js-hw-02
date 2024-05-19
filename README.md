# goit-js-hw-02

-----РОЗГАЛУЖЕННЯ-----

Інструкція if дозволяє виконати певний блок коду тільки в тому випадку, якщо задана умова істинна (тобто приймає значення true).
if (condition) {
// код, який виконується, якщо умова (condition) істинна
}

Синтаксис інструкції if можна доповнити блоком else для визначення альтернативних варіантів виконання коду.
if (condition) {
// код, який виконується, якщо умова істинна
} else {
// код, який виконується, якщо умова хибна
}

Конструкція else...if розширює конструкцію if...else і дозволяє перевірити та зреагувати на виконання або невиконання кількох умов.
if (condition_1) {
// код, який виконується, якщо умова (condition_1) істинна
} else if (condition_2) {
// код, який виконується, якщо умова (condition_2) істинна
} else if (condition_3) {
// код, який виконується, якщо умова (condition_3) істинна
} else {
// код, який виконується, якщо всі умови хибні
}

Тернарний оператор — це коротша синтаксична заміна інструкції if...else.
<condition> ? <expression if condition is true> : <expression if condition is false>

Оператор switch дозволяє виконувати різні дії залежно від значення виразу. Використання switch є більш компактним і зручним способом для порівняння виразів з кількома варіантами, ніж інструкції if...else та else...if.
switch (expression) {
case value1:
// код, що виконується, якщо вираз (expression) дорівнює value1
break;
case value2:
// код, що виконується, якщо вираз (expression) дорівнює value2
break;
// ...
default:
// код, що виконується, якщо вираз (expression) не відповідає жодному значенню
}
Після виконання коду в одному з випадків потрібно використовувати оператор break, щоб вийти з оператора switch.

Область видимості визначає, чи будуть змінні та функції доступними в певних областях коду. Під час оголошення змінної або функції, вона стає "видимою" тільки в певній частині коду. Це впливає на те, де і як можна використовувати ці змінні та функції в коді.
const globalVar = "Global";
console.log(globalVar); // Доступ до globalVar з глобальної області видимості
// Немає доступу до aVar, bVar і cVar
if(true) {
const aVar = "A";
console.log(globalVar); // Доступ до globalVariable з блоку A
console.log(aVar); // Доступ до aVar з блоку A
// Немає доступу до bVar і cVar
if(true) {
const bVar = "B";
console.log(globalVar); // Доступ до globalVariable з блоку B
console.log(aVar); // Доступ до aVar з блоку B
console.log(bVar); // Доступ до bVar з блоку B
// Немає доступу до cVar
}
}
console.log(globalVar); // Доступ до globalVar із глобальної області видимості
// Немає доступу до aVar, bVar і cVar
if(true) {
const cVar = "C";
console.log(globalVariable); // Доступ до globalVar з блоку C
console.log(cVar); // Доступ до cVar з блоку C
// Немає доступу до aVar і bVar
}
console.log(globalVar); // Доступ до globalVar із глобальної області видимості
// Немає доступу до aVar, bVar і cVar

-----ЛОГІЧНІ ОПЕРАТОРИ-----

Запам’ятай 6 випадків, які приводяться до false:

1. 0
2. ""
3. Nan
4. null
5. underfined
6. false

Усі інші числа та не пусті рядки перетворюються на true.

Оператор "І" (&&) наводить усі операнди до логічного типу (true або false) і повертає значення одного з них. Дозволяє перевірити, чи виконані всі умови у виразі.
expression1 && expression2
Оператор “І” зліва направо перевіряє почергово обидва операнди на істинність та повертає або значення останнього істинного (тільки правого) операнда, або першого хибного (лівого чи правого), на якому він запнувся.

Оператор "АБО" (||) перетворює всі операнди до логічного типу (true або false) і повертає значення одного з них.
expression1 || expression2
Якщо хоча б один із операндів можна перетворити на true, результатом логічного «АБО» буде цей операнд.
Як тільки логічний оператор “АБО” знайшов операнд, який перетворюється на true, він зупиняється та повертає його значення. Якщо до істини було перетворено перший операнд, то другий навіть не буде оцінюватися.
Якщо всі операнди перетворюються на false, результатом буде значення крайнього правого операнда.

Логічне «НІ» (!) — це унарний оператор — він виконує операцію над одним операндом праворуч.
!expression
Логічне «НІ» приводить операнд до логічного значення (true або false) і потім заперечує (інвертує) його, тобто заміняє на протилежне: true —> false, а false —> true.

---МЕТОДИ РЯДКІВ-----

Метод slice() використовується для створення копії частини або всього рядка без зміни оригінального рядка. Він дозволяє витягувати підрядок з вихідного рядка, вказуючи початковий та кінцевий індекси.
str.slice(startIndex, endIndex)
де:
str — вихідний рядок, з якого робитиметься копія.
startIndex — індекс, з якого починається копіювання елементів рядка.
endIndex — індекс, до якого (не включаючи) йде копіювання елементів рядка.

Метод toLowerCase() повертає новий рядок, у якому всі символи вихідного рядка перетворені в нижній регістр.

Метод toUpperCase() повертає новий рядок, у якому всі символи вихідного рядка перетворені у верхній регістр.

Метод рядків includes() використовується для перевірки наявності підрядка у рядку. Він повертає логічне значення true, якщо підрядок знайдено, і false, якщо підрядок відсутній.
str.includes(substring)
де:
str — вихідний рядок, у якому ми шукаємо підрядок;
substring — підрядок, який ми хочемо знайти у вихідному рядку.

Метод startsWith() перевіряє, чи починається рядок із зазначеного підрядка.
str.startsWith(substr)
substr — це рядок, з якого має починатися вихідний рядок.

Метод endsWith() перевіряє, чи закінчується рядок вказаним підрядком.
str.endsWith(substr)

Метод indexOf() використовується для пошуку першого входження підрядка в рядок. Він повертає:
індекс першого входження (індекс першого символу) підрядка, якщо він знайдений або
-1, якщо підрядок не виявлено
str.indexOf(substr)

Метод trim() використовується для видалення початкових і кінцевих пробілів із рядка.
str.trim()

-----ЦИКЛИ-----

Конструкція while створює цикл, який виконує блок коду в тілі циклу, поки умова для виходу оцінюється як true.
while (condition) {
statement // код, тіло циклу
}

Під час використання циклу do...while код у тілі циклу виконується принаймні один раз, навіть якщо умова не виконується з самого початку.
do {
statement // код, який буде виконуватися
} while (condition);

Цикл for також дозволяє виконувати код, що повторюється, багато разів. На відміну від циклів while і do…while, цикл for має змінну-лічильник. Змінна-лічильник оголошується за допомогою ключового слова let (оголошення через const видасть помилку). На кожній ітерації після виконання коду з тіла циклу вона змінює своє значення від заданого початкового до кінцевого з певним кроком.
for (initialization; condition; afterthought) {
statement // Тіло циклу
}

Префіксний інкремент (++value) спочатку збільшує значення змінної, а потім використовує нове значення у виразі.
Постфіксний інкремент (value++) спочатку використовує поточне значення змінної у виразі, а потім виконує збільшення значення.

Префіксний декремент (--value) спочатку зменшує значення змінної, а потім використовує нове значення у виразі.
Постфіксний декремент (value--) спочатку використовує поточне значення змінної у виразі, а потім виконує зменшення значення.

Оператор break використовується в циклі для переривання його виконання. Коли оператор break зустрічається всередині циклу, виконання циклу негайно припиняється, і керування передається до наступної інструкції після циклу. оператор break не припиняє виконання функції, а тільки перериває цикл. Для того щоб переривати виконання одразу циклу і функції і повернути результат у зовнішній код, є оператор return.
