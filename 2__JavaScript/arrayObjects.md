```js
ARRAYS =================================================

Array.isArray() -  вернет true если это массив
        const fruits = ["Banana", "Orange", "Apple", "Mango"];
        let result = Array.isArray(fruits); // return true

LOOPS:
        map() - вернет новый массив преобразуя каждый его член ф-цией
                const numbers = [65, 44, 12, 4];
                const newArr = numbers.map(num => num * 10) // return [650, 440, 120, 40]

        reduce() - вернет результат 
                const numbers = [175, 50, 25];
                numbers.reduce((total, num) => total - num, 0); // return 100

        forEach() - цикл, который вернет результат использования всех елементов массива
                const fruits = ["apple", "orange", "cherry"];
                let text = '';
                fruits.forEach((item, index) => {
                text += index + ": " + item + "<br>";
                });

        for_of // цикл для массивов
                const cars = ["BMW", "Volvo", "Mini"];
                let text = "";
                for (let x of cars) {
                        text += x;
                } // return 
ADDING
        push
        unshift
        concat


CUTING
        splice(start, end) - вернет массив элементов от start до end
                const fruits = ["Banana", "Orange", "Lemon", "Apple", "Mango"];
                const citrus = fruits.slice(1, 3); // return ['Orange', 'Lemon']

FILTER
        every() - все елементы должны удовлетворять условию ф-ции =>(true/false)
                const ages = [32, 33, 16, 40];
                ages.every(age => age >18) // return false

        filter() - вернет массив только с елементами прошедшими тест
                const ages = [32, 33, 16, 40];
                ages.filter(age => age >= 18); // return [32, 33, 40]

        indexOf() - вернет индекс первого совпадения
                const fruits = ["Banana", "Orange", "Apple", "Mango"];
                let index = fruits.indexOf("Apple"); // return 2


OBJECTS =============================================

let obj = { 0: 'a', 1: 'b', 2: 'c' };
console.log(Object.keys(obj)); //  ['0', '1', '2']
console.log(Object.values(obj)); // ['a', 'b', 'c']
console.log(Object.entries(obj)); // [ ['0', 'a'], ['1', 'b'], ['2', 'c'] ]

// ForIn 
    const person = {fname:"John", lname:"Doe", age:25};
    let tXt = "";
    for (let x in person) {
        txt += person[x] + " ";
    } // return "John Doe 25 "