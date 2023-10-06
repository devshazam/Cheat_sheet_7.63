```js

let m0 = /.../; // границы регуларного выражения
let m1 = /.../g; // "g" - значит искать все совпадения

.       // любой символ
0...9   // числа значат сами себя
\d      // любое число
    \D  // не число
\w      // буква
    \W  // не буква
\s      // probel
    \S  // не пробел
\n      // перевд строки, не нужно экраниовать 

Повторить:
? // 0 или 1
    /a?/ // првторить 'a' 0 или 1 раз
* // 0 или много
+ // 1 или много
{x, y} // 
{x, y} //reapet from x to y times


ИЛИ
[zy] // z или y
[a-z] // one simbol form a to z
| // "or" - simbbol 

() // grupping for action simbols

\ // ekranirovanie
$ // first simbols
^ // last simbol


// ############################ METHODS ###################################

// Replace

'bab'.replace(/а/, '!'); 
// вернет 'b!b' - применяется к строке, первым параметром принимает 
// регулярное выражение, вторым - строку на которую нужно заменить 
// найденные в исходной строке части - возвращает строку с замененными частями

        // Pockets

        let res = str.replace(/([a-z]+)@([a-z]+)/g, '$2@$1');
        // При работе с методом replace, если мы что-то положим в карман в регулярке,
        //  то в строке замены мы можем вставить содержимое этого кармана написав 
        // знак доллара $ и номер кармана. Например, $1 - первый карман, 
        // $2 - второй карман и так далее.


        // Default pockets
        let res = str.replace(/\d+/g, '($&)');
        // В методе replace, помимо карманов с вашими номерами, 
        // всегда доступны также стандартные карманы: $& - всё найденное совпадение, 
        // $` и $' -часть строки до и после совпадения. 
        // Давайте посмотрим работу с ними на примерах. 
        // - [http://code.mu/ru/javascript/book/supreme/regular/replace-default-pockets/](http://code.mu/ru/javascript/book/supreme/regular/replace-default-pockets/)


    // Calback

    let result =  '2+3= 4+5= 6+7='.replace(/(\d+)\+(\d+)=/g, function(match0, match1, match2) {
    let sum = Number(match1) + Number(match2); //match1 is first match
    return match0 + sum; // match0 is a common match
    });
    console.log(result); - '2+3=5 4+5=9 6+7=13'


// Match

1. let res = str.match(/xa+x/);
// применяется к строке и возвращает все найденные ее части в массиве.
let str = 'sss xaaax zzz';
let res = str.match(/x(a+)x/);
console.log(res[0]); // выведет 'xaaax' - найденное
console.log(res[1]); // выведет 'aaa'   - карман
// !!! НО если регулярка глобальная let res = str.match(/xa+x/g);, 
// то в res будеть только массив совпадений, БЕЗ карманов.


// Search

Search - возвращает позицию первой найденной подстроки, а если она не найдена - то -1.
let str = 'a aa aaa aaaa aaaa';
let res = str.search(/aaa/);
```