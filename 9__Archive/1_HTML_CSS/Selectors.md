" " - селектор влоенности без ограничения уровня вложенности 
">" - селектор непосредственной вложенности 
"+" - селектор выбирает соседний елемент  - https://code.mu/ru/markup/book/prime/theory/adjacent-sibling-selector/
"~" - выбор всех родственников определенного елемента (елементы одного родителя), кроме самого елемента
"*" - выбор всех елементов в заданного родителя, если сам по себе приминяется ко всем елементам

Атрибуты: - http://htmlbook.ru/samcss/selektory-atributov
- [href]{...}
- [href="http://www.yandex.com"]{...}

Ссылки - https://code.mu/ru/markup/book/prime/theory/link-states/
a:link {...} - мтиль ссылки
a:visited {...} - стиль полсе клика
a:hover {...} - стиль под наведенной мышкой
a:active {...} -  стиль в момент нажатия

Псевдоклассы
li:not(:first-child)
    - li:first-child {} - первый потомок своего родителя
        - :first-of-type - по типу
    - li:last-child {} - последний потомок своего родителя
        - :last-of-type - по типу
    - li:nth-child(4) {} - n потомок родителя - https://code.mu/ru/markup/manual/css/pseudoclass/nth-child/
        - :nth-of-type(2) - по типу
    - li:nth-last-child(4) {}  n потомок родителя с конца - https://code.mu/ru/markup/manual/css/pseudoclass/nth-last-child/
        - :nth-last-of-type(2) - по типу
    - li:only-child {} - только если элемент является единственным потомком родителя
        - :only-of-type  - по типу
    - li:empty {} - относится к елементу без текста