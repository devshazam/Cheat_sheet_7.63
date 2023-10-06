```js
_1
    let a = varOne || 6; // если varOne не существует, то будет 6, НО varOne должно быть задано undefined 

_1:
    setTimeout(function() {alert('!'); }, 3000); 

_2:
    let one = условие ? значение1 : значение2; 
    
_3:
    Spred - разбить массив (объект) на елементы
        - func(...[1, 2, 3, 4, 5]); //! func(1,2,3,4,5);
        - const newArray = [...oneArray + ...twoArray];
        - const newObject = {...oneObject, ...twoObject};
        - 
_4:
    Rest
        - func(a, b, ...rest);
        - const [one, two, ...rest] = oneArray;

- экранирование
        \' // экранирование ковычек в строке 
        \"  // 
        \n, \b, \f, \r, \t, \v  // специальные символы

- деструктуризация 
    - Массивы
        - const [one, two] = oneArray // в пременные one и two запишутся первые два елемента массива
        - const [, , one, two] = oneArray // в пременные one и two запишутся 3 и 4 елементы массива
        - const [one, two, ...rest] = oneArray // в пременные one и two запишутся первые два елемента массива, а остальные в переменную rest

    - Объекты
        - const {one, two} = oneObject // переменные только под темиже
        - const {one, two, outside} = oneObject // если имени outside нет в объекте, то outside = undefined
        - const {one: two} = oneObject // alias - меняет имя переменной при деструктуризации
            

- приоритет операторов 
    1. Высший приоритет () // Пример: (2+2)*2 = 8
    2. Второй приоритет +var  // Унарный плюс - преобразует в число
    3. Удаление, деление
    4. Сложение, вычитание, остаток (%)
    5. Присваивание


- JSON// https://www.w3schools.com/js/js_json_intro.asp
    var myJSON = JSON.stringify(myObj); // --> json
    var obj = JSON.parse('{"firstName":"John", "lastName":"Doe"}');


Here is a list of falsy values:
    false
    0, -0, 0n // zero
    "", '', `` // empty string
    null
    undefined
    NaN 

Check_type
    Array 
        letters instanceof Array // 
        Array.isArray() 
        array.length

    Number
        isNaN('we') // проверка на число
        Number.isInteger(+width) // проверка на целое число

    Object
        Object.keys(devices).length // Проверка массива на пустоту 

